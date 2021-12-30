# Video editor UI not downloading effects and other components

[Developer]
You can use the following template to facilitate ticket handling.
1. What were you doing when you ran into the problem?
Answer: I integrated video editor UI kit but when i click on any effects it does not bring any video effects. seems like download problem

2. At which step did the problem occur?
Answer: Animations and Filters

3. What were you expecting to happen?
Answer: i wanted to change the video filter

4. What actually happened?
Answer: no filter appeared in bottom nav.

5. What is the model and OS version of the device you were using?
Answer: Android 10 and Samsung S9

6. Which version is the SDK of your kit? If the AR Engine is used, provide the AR Engine version number.
Answer: 

7. Paste a screenshot of what you saw when the problem occurred.
Answer:

Logs:
```
E/ImageEngine: Unsupported: /data/user/0/com.huawei.mvideoeditor/files/hms_video_editor_kit/project/4bb05e7d3d744c0c932ca425170c22e9/1640731284089cover.png 2021-12-28 17:41:24.197 30273-654/com.huawei.mvideoeditor E/CountryCodeBean: getVendorCountry=UNKNOWN 2021-12-28 17:41:24.200 30273-654/com.huawei.mvideoeditor E/CountryCodeBean: getSimCountryCode by not enableNetwork, countryCode=us 2021-12-28 17:41:24.208 30273-654/com.huawei.mvideoeditor E/CountryCodeBean: getVendorCountry=UNKNOWN 2021-12-28 17:41:24.211 30273-654/com.huawei.mvideoeditor E/CountryCodeBean: getSimCountryCode by not enableNetwork, countryCode=us
```

[Support]
Thank you for contacting us, can you confirm your HMS Core version number, and are you using the sample code here - https://github.com/HMS-Core/hms-video-editor-demo?

[Developer]
I am using the latest libraries and i used both demo and my custom project but unable to download video materials, if i click on filter or animation, spinner is spinning but no result. is this because of no material is allocated? i tried to allocate material but i could not do that. if allocating material is the issue then please share the steps or tutorial how to do that. Thank you 
```
classpath "com.android.tools.build:gradle:7.0.2"
classpath "com.huawei.agconnect:agcp:1.6.0.300"
implementation 'com.huawei.agconnect:agconnect-core:1.6.0.300'
implementation 'com.huawei.hms:video-editor-ui:1.1.0.302'
```