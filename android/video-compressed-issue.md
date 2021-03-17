Issue: 
1. Download the app from AppGallery.
2. Slide down the notification bar to open the screen recorder.
3. Open app and send the screen recorder to friend and send to you a screen recorder from other account.
4. Play the received video on Pixel/Huawei P40 and it is virtically compressed.

Response:
This issue appears on P30 and newer devices but not on P20.
Android API "android.content.ContentResolver" is used to fetch media source meta-data for Camera roll content. In this case, the most important information is width, height, and rotation angle.
Huawei engineers can use this android api to compare the difference between P30 and other devices, e.g. we know there is no such problem from Huawei P20.
On Huawei P30, it returns 1280x590, rotation angle is 0. It would be Huawei updating a media content database to support this api.
Please check what's the reason of the ContentResolver returning different results on P20 and P30.
