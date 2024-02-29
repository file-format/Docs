{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "فایل گواهی P7C - PKCS 7",
  "description": "درباره فرمت فایل P7C و APIهایی که می‌توانند فایل‌های P7C را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "P7C",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-p7-fac"
}
}،
  "lastmod": "2019-09-10"
}

## فایل P7C چیست؟

فایل P7C، مانند سایر فایل‌های گواهی امنیتی، یک گواهی دیجیتال است که برای احراز هویت از طریق شبکه استفاده می‌شود. برنامه‌هایی که از گواهی‌ها استفاده می‌کنند هویت را با استفاده از کلید عمومی موجود در این فایل‌های گواهی احراز هویت می‌کنند. رمزنگاری با کلید عمومی یا رمزنگاری نامتقارن از جفت کلید استفاده می کند که یکی کلید عمومی و دیگری به عنوان کلید خصوصی شناخته می شود. کلید خصوصی برای امنیت موثر ایمن نگه داشته می شود، در حالی که کلید عمومی را می توان با دیگران به اشتراک گذاشت. سایر قالب‌های رایج فایل گواهی عبارتند از [CRT](/web/crt/)، DER و PEM.

## فرمت فایل P7C - اطلاعات بیشتر

فایل‌های P7C به‌عنوان فایل‌های باینری روی دیسک ذخیره می‌شوند و شامل اطلاعات کلید عمومی تولید شده با استفاده از الگوریتم‌های رمزنگاری بر اساس مسائل ریاضی می‌شوند. اینها را می توان در هر ویرایشگر متنی باز کرد اما محتوای آنها به شکل قابل خواندن توسط انسان نیست. برخی از برنامه هایی که می توانند فایل های P7C را باز کنند عبارتند از Apple Keychain Access، Adobe Acrobat Reader DC، Microsoft Certificate Manager و Microsoft Windows Contacts.

### نمونه فرمت فایل P7C

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## منابع ##

* [رمزگذاری کلید عمومی](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [چگونه فایل P7C ایجاد کنیم؟](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


