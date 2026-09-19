# بناء APK لتطبيق أناقة أون لاين

هذا المشروع مجهز لبناء ملف APK قابل للتثبيت على أجهزة Android باستخدام Expo EAS Build.

## 1) المتطلبات

- حساب Expo مجاني أو مدفوع.
- Node.js LTS.
- Git (إذا كان المشروع على GitHub).

## 2) من مجلد المشروع

```bash
npm install
npx eas login
```

تحقق من تسجيل الدخول:

```bash
npx eas whoami
```

## 3) بناء APK تجريبي قابل للتثبيت

استخدم:

```bash
npx eas build --platform android --profile apk
```

أو:

```bash
npx eas build -p android -e apk
```

سيتم رفع المشروع إلى EAS، ثم يظهر رابط/صفحة البناء بعد اكتماله. من صفحة البناء يمكن تنزيل APK وتثبيته على الهاتف.

## 4) إذا طلب EAS إنشاء مفتاح التوقيع

وافق على إنشاء Android keystore جديد إذا لم يكن للتطبيق مفتاح سابق. EAS يستطيع إدارة بيانات توقيع Android نيابة عنك.

**لا ترفع keystore أو كلمات المرور أو مفاتيح API إلى GitHub.**

## 5) مهم: APK أم Google Play؟

- `apk` مخصص للتثبيت المباشر والاختبار على الهاتف.
- عند تجهيز النسخة النهائية للنشر على Google Play استخدم ملف AAB عبر:

```bash
npx eas build --platform android --profile production
```

## بيانات التطبيق الحالية

- الاسم: أناقة أون لاين
- Slug: anaqa-online
- Android package: com.anaqaonline.store
- الإصدار: 2.0.0
- Version Code: 2

## في حال كان المشروع على GitHub

بعد رفع الملفات إلى GitHub، يمكنك تنزيل المستودع ثم تنفيذ الأوامر السابقة من داخل مجلد المشروع.

> هذه الحزمة تجهز عملية بناء APK، لكن عملية البناء الفعلية تحتاج تسجيل الدخول إلى حساب Expo وإرسال البناء إلى EAS.
