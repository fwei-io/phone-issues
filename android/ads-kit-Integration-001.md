# Ads Kit Integration 001

We are having some difficulties integrating the Huawei Ads Kit into our map.

When we query an ad with the test ad slot id for native small ad (testb65czjivt9) we are not getting the image for that ad. The title and call to action texts are loaded, but the image (icon) is null. We are calling the NativeAd.getMediaContent() method. We are not able to find any documentation for this method in the class reference on 
Huawei Developers site - https://developer.huawei.com/consumer/en/doc/development/HMSCore-References/nativead-0000001050066855

We try to obtain it the same was as in the sample project here - https://github.com/HMS-Core/hms-ads-demo-java, but in the sample project it is returning proper image and in our project it is returning null.

Could you help us resolve this issue?

Another thing that we noticed is that on non-Huawei devices with installed AppGallery and HMS Core (latest version) the sample app is not working, it is returning error code 0 when we try to query an ad. Could you help us resolve this as well?

Device Model : Huawei Y5p -> DRA-LX9
Build Number : 10.1.0.163(C432E3R2P1)
EMUI version : 10.1.0
Android version : 10

AppGallery -> Country/Region is set to Bulgaria.

Device Log - https://raw.githubusercontent.com/fwei-io/phone-issues/main/logs/ads-kit-Integration-001/hwDeviceLogs.log

HiAdKitLog.log - https://raw.githubusercontent.com/fwei-io/phone-issues/main/logs/ads-kit-Integration-001/HiAdKitLog.log