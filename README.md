# أناقة أون لاين — Anaqa Online

تطبيق متجر إلكتروني للملابس، مبني باستخدام **Expo + React Native** ويدعم Android وiOS.

## محتويات النسخة

- الصفحة الرئيسية
- الأقسام
- البحث
- تفاصيل المنتج
- المفضلة
- السلة وتعديل الكمية
- إتمام الطلب
- الطلبات ومراحل التوصيل
- الحساب الشخصي
- شعار التطبيق والهوية البصرية داخل `assets/`
- بيانات منتجات تجريبية قابلة للاستبدال لاحقًا

> هذه النسخة هي واجهة/نموذج أولي للتطوير. المنتجات والأسعار ووسائل الدفع والبيانات الحقيقية تضاف لاحقًا.

## المتطلبات

- Node.js LTS
- npm
- Expo CLI عبر `npx`
- Android Studio أو جهاز Android للتجربة
- Xcode على macOS لتجربة iOS محليًا

## التشغيل محليًا

```bash
npm install
npx expo start
```

بعدها يمكن تشغيل التطبيق عبر Expo Go أو المحاكي المناسب.

## بناء Android / iOS

يمكن استخدام EAS Build بعد تسجيل الدخول إلى Expo:

```bash
npx eas login
npx eas build:configure
npx eas build --platform android
npx eas build --platform ios
```

> لا تضع مفاتيح التوقيع أو كلمات المرور أو أسرار API داخل GitHub. استخدم GitHub Secrets أو EAS Secrets عند ربط الخدمات الحقيقية.

## الهوية والشعار

- `assets/logo-original.png` — الشعار الأصلي المستخدم في المشروع.
- `assets/logo.png` — نسخة الشعار المستخدمة داخل التطبيق.
- `assets/icon.png` — نسخة مربعة لأيقونة التطبيق.

## رفع المشروع إلى GitHub

1. أنشئ مستودعًا جديدًا باسم مثل `anaqa-online`.
2. فك ضغط هذا المشروع.
3. ارفع **محتويات مجلد المشروع** إلى المستودع، وليس ملف ZIP نفسه.
4. تأكد أن `package.json` و`App.js` و`app.json` و`assets/` موجودة في جذر المستودع.

أو عبر Git:

```bash
git init
git add .
git commit -m "Initial Anaqa Online app"
git branch -M main
git remote add origin YOUR_GITHUB_REPOSITORY_URL
git push -u origin main
```

## هوية التطبيق

اسم العرض: **أناقة أون لاين**  
Slug: `anaqa-online`  
Android package: `com.anaqaonline.store`  
iOS bundle identifier: `com.anaqaonline.store`

يمكن تغيير اسم العرض لاحقًا، بينما يفضّل تثبيت معرّفات Android وiOS بعد النشر.
