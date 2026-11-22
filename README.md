# LIC Agent App (Android, Jetpack Compose)

Built from the 10-screen UI mockup: Login, Agent Dashboard, Customers, Customer Details,
Pay Premium, Add Customer, Add Policy, Payment History, Payment Receipt, Policy Reminders
(+ Reports, Quick Pay, More, all-payments list).

## Build the APK
1. Install Android Studio (Koala or newer, JDK 17+).
2. File > Open > select this `LICAgent` folder, let Gradle sync finish.
3. Debug APK: Build > Build Bundle(s) / APK(s) > Build APK(s)
   -> app/build/outputs/apk/debug/app-debug.apk
   (or run `./gradlew assembleDebug` after Android Studio generates the wrapper)
4. Release APK: Build > Generate Signed Bundle / APK.

## Notes
- minSdk 29 (Android 10+). Data is stored on-device (SharedPreferences/JSON); no backend.
- First launch is seeded with the 5 sample customers from the mockup (delete them in-app).
- Login accepts any Agent ID + password (local demo). Fingerprint login works after one normal login.
- "Pay Securely" records the payment + generates a receipt; no real payment gateway is wired in.
- Receipts: WhatsApp (wa.me), PDF saved to Downloads, share sheet.
