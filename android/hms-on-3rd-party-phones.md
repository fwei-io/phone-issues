# HMS support on 3rd-party phones

Other than AppGallery, we have shared HMS apk via our file server, we noticed user download and side-loaded it on non-Huawei devices. We installed and tested this apk on non-Huawei Android phones, we found out that it actually worked if we side-load HMS Core app, but with minor issues like Push kit crashes (sometimes). We try to make our HMS app as compatible as possible on other OEM phones, our questions are:

1. What is Huawei’s position on supporting HMS Core and side-loaded HMS apps on non-Huawei devices? Is it encouraged and officially supported by HMS Core?
2. We see crashes due to Push service on non-Huawei devices, our Push kit process name is "push service" and we noticed there is another process using the exact same process name (especially Xiaomi's Mi push, Realme), we think this crash our app. Our questions are:
    a. What is the root cause for this crashes?
    b. Can we use Push kit and HMS Core on Xiaomi phone in situation like this? We try to make our HMS app compatible with other OEM Push services.
    c. Can Huawei Push kit use Xiaomi Mi Push service instead? If yes, is there any document?
    d. Do HMS Push work with other push services like Mi Push, Baidu Push? If yes, can you share any developer doc or best practice?
3. What is the best practice on using HMS app on non-Huawei devices?
4. What are the common issues that we need to be aware of when supporting HMS app on non-Huawei devices?
