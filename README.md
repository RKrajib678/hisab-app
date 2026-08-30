# আমার হিসাব — Amar Hisab

একটি offline-first Android হিসাব অ্যাপ। আপনার হিসাব ফোনের Room database-এ থাকে। কোনো Google Drive/Google Sheets/cloud sync নেই।

## কী আছে
- আয়, খরচ, পাওনা, দেনা
- তারিখ, ক্যাটাগরি, ব্যক্তি ও বিস্তারিত
- ড্যাশবোর্ডে মোট হিসাব
- হিসাবের তালিকা ও সার্চ
- হিসাব ডিলিট
- PDF রিপোর্ট
- JSON Backup / Restore
- সম্পূর্ণ offline local database

## Android Studio দিয়ে চালানো
1. Android Studio (সাম্প্রতিক stable version) খুলুন।
2. এই `AmarHisab` folder-টি Open করুন।
3. Gradle Sync শেষ হতে দিন।
4. USB debugging চালু করা Android ফোন/Emulator নির্বাচন করুন।
5. Run চাপুন।

## APK বানানো
Android Studio → Build → Generate App Bundles or APKs → Generate APKs

Debug APK সাধারণত:
`app/build/outputs/apk/debug/app-debug.apk`

## গুরুত্বপূর্ণ
বর্তমান PDF শেয়ারিং অংশটি Android 7+ এ FileProvider ব্যবহার না করে cache URI ব্যবহার করছে। Android-এর কঠোর URI policy অনুযায়ী প্রয়োজনে FileProvider যোগ করা উচিত। নিচের version-টি মূল হিসাব/অফলাইন ডাটাবেসের জন্য প্রস্তুত।
