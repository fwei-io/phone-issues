### Issues:

1. **Need to upgrade app using OTA.**

The app currently has remaining 400K+ DAU who are still using version 11.16.x.x and older version, looks like these users won’t upgrade to 11.17. These apps use the old expired key signature, it cannot be upgraded to future APK/App Bundle (new key) without breaking the key signature verification.

Here is the situation:

1. App 11.16 and older has the old/expired key.
2. App 11.17 (current) has old/expired key and allowed signing keys (debug, new). However the developer made a mistake by putting a debug key in the allowed key sets; they should have use the same old key.
3. Now developer cannot ask user to upgrade to 11.18+ with the old or debug keys. If they use new key,     11.16 and older app users must go through AG warming prompts.

![upgrade-app-to-new-key](https://raw.githubusercontent.com/fwei-io/phone-issues/main/images/upgrade-app-to-new-key.jpg)

To upgrade to 11.18 (new & debug keys only), user must:

- **Install 11.17.0.36 version first** (but there are 400K users who don’t turn on AG auto update and willing to update, there is no guarantee if most of them would upgrade even if AG sent the push notification).
- **Directly upgrade from 11.16 (and older) to 11.18 through AG with warning prompts.** This will cause user confusion, bad user experience, require customer support resources, create PR issues for developer and AG, etc.

Developer is requesting HOTA to force update all current AG installed apps (preload or regular app) to version 11.17 in the background. Per developer’s engineer manager, they know this can be done through OEM OS if configured correctly, if OEM has no issue with such upgrade policies. They are willing to be the request party and sign legal approval to perform such OTA update.

Once 95-99% of their users have installed the app with new key signature, they can launch 11.18 app(s) and then App Bundle, which will increase user acquisition and engagement, benefiting both companies.