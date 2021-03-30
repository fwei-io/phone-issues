### Issues:

1. **Sound notification issues** 
2. **The Dots badge disappear when new messages**

### Response 1

This report includes 2 issues:

**Issue 1:** **No sound notification when new messages coming except the first time**

This issue is reproducible yet I think it is **expected behavior.** I asked the QA from the related team to double confirm. Will correct it if I am wrong. Precondition: All the notification permissions are granted

A: Pixel 4XL/Android 11/11.20.0.36 production

B: iPhone 12 Prom Max/iOS 14.4/11.23.0.1 Gold

Steps to reproduce:

1. B sends a text message to friend A -> A could receive the push notification with the sound heard (A does not view the text message)
2. B sends a new text message to friend A -> A could receive the push notification, but the sound is not heard.
3. A views all the text messages and background the app. B sends a new text message to friend A -> A could receive the push notification with the sound heard.

**Issue 2:** **no messages banner Pop-up when app in the background sometimes**

I have no luck to reproduce this issue. Try to send the test device 20 messages. The test device could receive the push notification every time. I asked the QA from the related team if it was a known issue for us. Will let you know for any updates.

----

### Response 2

Test on Huawei Mate 30/TAS-L29/Android/EMUI version 10.0.0 on 11.18.0.30 production

**Scenario 1:** 

1. `Device Settings > App icon badges > Badge display mode > Numbers`
2. `Auxiliary device sends the test device a text message`

Actual result: The test device could receive the push notification. However, there is no number badge to the top right of the app logo. As for the question "**Could I confirm if you app does not support the Numbers badge display?**" The latest update that I can search from the previous emails. This matches with the latest info from the email.

**Scenario 2:**

- `Device Settings > App icon badges > Badge display mode > Dots`
- `Auxiliary device sends the test device a text message`

Actual result: The test device could receive the push notification, and there is a dot badge to the top right of the app logo. However, I have no luck to reproduce "The Dots badge disappear when new messages coming**".