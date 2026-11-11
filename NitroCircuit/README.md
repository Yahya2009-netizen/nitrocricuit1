# Nitro Circuit - تطبيق أندرويد

لعبة سباق 3D داخل WebView، تخدم بدون إنترنت (الخط فقط يحتاج إنترنت أول مرة، وإلا يستعمل خط النظام).
تقدّمك (عملات، تطويرات، ألوان) يتحفظ في التطبيق.

## الطريقة 1: من الهاتف بلا كمبيوتر (GitHub)
1. افتح حساب GitHub مجاني وأنشئ مستودع جديد (New repository).
2. ارفع كل محتوى هذا المجلد للمستودع (Add file > Upload files)، مع مجلد `.github`.
3. روح لتبويب **Actions** > **Build APK** > **Run workflow**.
4. بعد حوالي 3 دقائق ادخل على التشغيل وحمّل `nitro-circuit-apk` (ملف zip فيه `app-debug.apk`).
5. فك الضغط وثبّت الـ APK (اسمح بـ "تثبيت من مصدر غير معروف").

## الطريقة 2: Android Studio
1. افتح Android Studio > Open > اختار هذا المجلد، واستنى Sync.
2. Build > Build Bundle(s) / APK(s) > Build APK(s).
3. الملف يطلع في `app/build/outputs/apk/debug/app-debug.apk`.
   (من الأوامر: `./gradlew assembleDebug`)

## تعديلات سريعة
- اللعبة كلها في `app/src/main/assets/index.html`.
- الاتجاه: في `AndroidManifest.xml` بدّل `sensorLandscape` إلى `fullSensor` إذا تحب تدور في كل الاتجاهات.
- الاسم: `android:label` في `AndroidManifest.xml`. الأيقونة: `res/drawable/ic_launcher_foreground.xml`.
- زر الرجوع: يوقف السباق مؤقتاً أو يرجّعك للشاشة السابقة، وفي الشاشة الرئيسية يقفل التطبيق.
- الـ APK هذا موقّع بمفتاح debug وهو للاستعمال الشخصي. للنشر في Google Play لازم توقيع release.
