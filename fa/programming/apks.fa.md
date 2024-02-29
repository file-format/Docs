
{
  "date": "2022-02-06",
  "keywords": [
"فایل apks",
"افزونه",
"قالب",
"بایگانی مجموعه APK",
"نحوه باز کردن فایل apks",
"فرمت فایل apks"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "فایل APKS - بایگانی مجموعه APK",
  "description": "در مورد اینکه فایل APKS چیست بدانید؟",
  "linktitle": "APKS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-apk-fas"
}
}،
  "lastmod": "2022-02-06"
}

## فایل APKS چیست؟

فایل با پسوند apks. یک فایل آرشیو است که مجموعه ای از فایل های بسته اندروید **APK** است. هر فایل APK مجزا در فایل APKS با در نظر گرفتن جنبه های مختلف دستگاه تولید می شود. اینها شامل معماری، زبان، تراکم صفحه نمایش و سایر ویژگی های دستگاه است. فایل‌های APKS توسط **bundletool** تولید می‌شوند. برای ساخت Android App Bundle و تبدیل بسته نرم افزاری به APK های مختلف برای استقرار در دستگاه ها استفاده می شود.

## فرمت فایل APKS - اطلاعات بیشتر

فایل‌های APKS به‌عنوان فایل‌های فشرده با استفاده از قالب فایل [ZIP](/compression/zip/) ذخیره می‌شوند.

## چگونه یک فایل APKS تولید کنیم؟

هنگامی که Android App Bundle (AAB) آماده است، رفتار آن در فروشگاه Google Play را می توان برای استقرار در یک دستگاه آزمایش کرد. برای این منظور می‌توان فایل‌های APKS را از فایل‌های AAB تولید کرد و با استفاده از Android Google [bundletool](https://developer.android.com/tools/bundletool) روی دستگاه‌های آزمایشی نصب کرد. ابزارهای خط فرمان را برای ایجاد فایل بایگانی APKS از APK با استفاده از دستور زیر فراهم می کند.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

به منظور استقرار APKها در یک دستگاه، فایل APKS را می توان با اطلاعات امضای دستگاه به صورت زیر امضا کرد.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## منابع

 * [bundletool - commandline](https://developer.android.com/tools/bundletool)

