# App Badge Number Issue

[Developer]
Thursday, July 9, 2020
I talked to one of our internal teams today and here is their feedback:
they would prefer that you adopts Android standard badging logic. If your team is planning to use a proprietary method to set the badge number, **we will maintain this as a backlog development item but do not currently have an ETA to fix it.**

[OEM]
Thu, Jul 9, 2020
One of our teams would like to know if you have any update on the badge number issue, can you check with your team? Thank you.

[Developer]
Monday, June 29, 2020 
Thank you for the update! Let me circulate this info within our internal teams!

[OEM]
Tue, Jun 30, 2020 
Please see the response from our team regarding your previous questions.
1. Facebook & Twitter already adapted our badge number icon, LinkedIn has not. After conformation, the following API can be used to display badge number icon on our device.
2. There is no universal solution because Google native has cancelled badge number icon. Currently all manufacturers independently developed badge number icon feature.
3. If the application has adapted our badge number icon, in theory, it can be displayed normally on all our mobile phones.
In addition, we found that this API has some typographical errors in the English interface, the the Chinese interface is normal. For details, please refer to:
Example:
![](https://raw.githubusercontent.com/fwei-io/phone-issues/main/images/app-badge-number-issue/example-code.png)

[Developer]
Monday, June 22, 2020 
Here are a few updates from our team:
1. We would like to know if your device shared the same API with Facebook, Linkedin and Twitter since from the screenshots you provided, the bading number feature is working on those Apps. Did other Apps which have badging number feature correctly working implement the badging number feature by using your API that mentioned in this link: https://developer.huawei.com/consumer/en/doc/system-Guides/20602?
2. Is it possible to have a common solution for enabling bading number on apps from system level instead of implementing it on every single App?
3. Are the badging number feature working on other devices except P40 and Honor Lite?

[Developer]
Thu, Jun 11, 2020
Here is the response regarding issue 1, thank you.
[OEM] Your app does not display the badge number on P40 mobile phones and Honor Lite Edition mobile phones
[Snap] This was analyzed by another team, we observed that the badging number is working fine on some of the other mobile brands. So we would like to know if there is any API that we need to use to enable this feature on Huawei devices. Please advise, thank you.
Please refer to this doc to configure badge with numbers: https://developer.huawei.com/consumer/en/doc/system-Guides/20602

[Developer]
Thursday, June 4, 2020 
Here is the quick update for your reported issues, please kindly help to circle back to your team to help get more information :)
[OEM]Your app does not display the badge number on P40 mobile phones and Honor Lite Edition mobile phones
[Developer]This was analyzed by another team, we observed that the badging number is working fine on some of the other mobile brands. So we would like to know if there is any API that we need to use to enable this feature on your devices. Please advise, thank you.

[Developer]
Regarding the badge number displaying, we tried to reproduce on P40 pro that you shipped to us. We didn't 100% reproduce the issue, but we got a small bubble on the icon rather than a number, see screenshot below,
![](https://raw.githubusercontent.com/fwei-io/phone-issues/main/images/app-badge-number-issue/screen-001.png)
FYI, here is the phone model name and the detailed system version that we used,
A: P40 Pro/ELS-NX9/10.81.5.74 Production(HMS)/Build number 10.1.0.102(SP6C900E102R1P3) System is up to date
B: Honor 10/COL-AL10/Android 8.1/10.81.5.74 Production(HMS)
We want to ensure that we are using the same testing devices and build version, so, could you please let us know the detailed system version (build version) that you reproduced the issue?

[OEM]
Hi, your app does not display the badge number on P40 mobile phones and Edition mobile phones. Please see the attached document. Thanks ~
Description: When a friend sends a new message, your app does not show icon badges Numbers.
Test Phones: P40, Honor10 lite
System Version: Android 10
Link to download the App: AppGallery
Test Steps:
1, Download from AppGallery
2, Launch your app
3, The auxiliary machine sends a message to the test machine
4, Observe whether of the test machine will show icon badges Numbers for your app.
Expected result: app will show icon badges Numbers.
Actual result: app will not show icon badges Numbers.
Occurrence Rate: 10/10 times
Analysis & Suggestion: From the log, can’t find the app in the log to make the phone display the log of the badges Numbers. Your app needs to adapt to the Numbers badge. Please check and modify it, thanks~
![](https://raw.githubusercontent.com/fwei-io/phone-issues/main/images/app-badge-number-issue/screen-002.jpg)
If you need further information, please do not hesitate and feel free to contact me.
Looking forward your kindly and promptly feedback!


