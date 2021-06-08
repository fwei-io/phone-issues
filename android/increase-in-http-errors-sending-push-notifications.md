# Increase in http errors sending push notifications

You are recommended to give feedback using the following model for problem-solving.
1. Your device information and SDK version: N/A
(1) Phone model (Settings > About phone): N/A
(2) EMUI version (Settings > About phone): N/A
(3) HMS Core version number (Settings > Apps > Apps > HMS Core): ?
(4) SDK version number (app-level build.gradle document): 30

2. Basic information about your problem
(1) What problem do you have?
HMS push calls were degraded with high failure rate on 6/4/2021, starting at 9:36am UTC jumping at 10am UTC, peaking at 10:27am and falling sharply at 10:36am UTC.
(2) Which API did you call when the problem occurred?
https://push-api.cloud.huawei.com/v1/<appId>/messages:send
(3) What result did you expect to see?
Success
(4) What result did you actually get?
Network Error
(5) Please upload a screenshot or video of your problem.
Answer: Starting 9:36am UTC, we saw an elevation in errors calling HMS PushKit. At 10:02am the error incident spiked further from 6k per minute to > 60k per minute.
The failure rate for push sends climbed from 5% to ~ 60%, briefly peaked to nearly 100% failure at 3:27am, which is also when HMS error code 80300002 (forbidden) peaked.

![01](https://raw.githubusercontent.com/fwei-io/phone-issues/main/images/increase-in-http-errors-sending-push-notifications/001.png)

![02](https://raw.githubusercontent.com/fwei-io/phone-issues/main/images/increase-in-http-errors-sending-push-notifications/002.png)

![03](https://raw.githubusercontent.com/fwei-io/phone-issues/main/images/increase-in-http-errors-sending-push-notifications/003.png)

3. Information of the test phone and Push SDK when you have a problem
(1) Version number of Push Service (Settings > Apps > Apps > Push Service): ?
(2) Enter *#*#258#*#* in the dialing keypad and upload the status query screenshot.
N/A

4. Basic information about your app
(1) AppID: 
(2) Data storage country selected in AppGallery Connect (China/Germany/Russia/Singapore):
Answer: Data storage location：Germany

5. If your message is delayed or not received, please provide the following information.
(1) Token of your device: n/a
(2) In which way did you send the message? (By configurations in AppGallery Connect or by calling the server API.)
Calling the server API
(3) When did you send the message?
9:36am UTC - 10:40am UTC
(4) When did you receive a message? (Skip the question if you did not receive a message.)
(5) requestId returned by your app:
(6) What condition did you use to send the message (token/topic/audience)?
token
(7) Type of your message (notification bar message/data message):
data message

(8) Upload your phone log within 10 minutes of you sending the message (a Push log document under the path: /sdcard/android/data/com.huawei.hwid/files/log. If there is no item under the path, obtain the log through the adb logcat command.)
Answer: n/a

6. Other information you want to give feedback about:
Answer: Is there a real-time support mechanism for us to check to see if Huawei is seeing issues.
How do we call attention to an ongoing issue with our application / projectID when it happens again?