# App crashed after sign in submission

Based on the logs, our analysis is as the following, hope it helps:

It's a crash inside Android. When [CameraCharacteristics.get](https://developer.android.com/reference/android/hardware/camera2/CameraCharacteristics#get(android.hardware.camera2.CameraCharacteristics.Key%3CT%3E)) is called, it should throw `IllegalArgumentException` when the property does not exist.

```
06-28 14:13:25.875 27614 19790 E AndroidRuntime:  at android.hardware.camera2.CameraCharacteristics.get(CameraCharacteristics.java:238)
```

The Range<T> throws internally the IllegalArgumentException("lower must be less than or equal to upper").

[https://cs.android.com/android/platform/superproject/+/master:frameworks/base/core/java/android/util/Range.java;l=60?q=range.java&ss=android](https://cs.android.com/android/platform/superproject/+/master:frameworks/base/core/java/android/util/Range.java;l=60?q=range.java&ss=android)

In the stack trace, IllegalArgumentException is got wrapped as assert exception by

```
06-28 14:13:25.875 27614 19790 E AndroidRuntime:  at android.hardware.camera2.marshal.impl.MarshalQueryableRange$MarshalerRange.unmarshal(MarshalQueryableRange.java:95)
```

Suggestions to OEM:

1. Do not intercept the IllegalArgumentException and allow it to populate the app level (Our app should handle it already)
2. Log which key caused the issue. 
3. OEM can double check on the camera HAL implementation for CameraCharacteristics, especially for Range type like

```
CONTROL_AE_AVAILABLE_TARGET_FPS_RANGES
CONTROL_AE_COMPENSATION_RANGE
CameraCharacteristics.SENSOR_INFO_EXPOSURE_TIME_RANGE
```