{
  "date": "2022-09-14",
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "فایل PEM - فرمت فایل گواهی نامه ایمیل تقویت شده حریم خصوصی",
  "description": "درباره فرمت فایل PEM و APIهایی که می‌توانند فایل‌های PEM را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "PEM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-pe-fam"
}
}،
  "lastmod": "2022-09-14"
}

## فایل PEM چیست؟

فایل PEM یک فایل گواهی امنیتی است که برای ایجاد یک کانال ارتباطی امن بین وب سرور و مرورگر استفاده می شود. این کد Base64 است و ممکن است حاوی یک کلید خصوصی، گواهی سرور و/یا ترکیبی از گواهی‌های دیگر باشد. فایل‌های PEM از نظر کاربرد مشابه فایل‌های گواهی .der هستند، اما به‌جای داده‌های باینری، به‌عنوان متن کدگذاری‌شده با Base64 ذخیره می‌شوند. سایر قالب‌های فایل گواهی مشابه شامل فایل‌های [.cer](/web/cer/) و [.crt](/web/crt/) هستند.

برنامه هایی که می توانند **فایل های PEM را باز کنند** شامل ویرایشگرهای متنی مانند Microsoft Notepad و Apple TextEdit هستند.

## فرمت فایل PEM

PEM یک فرمت فایل کانتینری است که ساختار و نوع رمزگذاری فایل مورد استفاده برای ذخیره داده ها را تعریف می کند. فایل‌های PEM به عنوان فرمت فایل کدگذاری شده با Base64 روی دیسک ذخیره می‌شوند که توسط انسان قابل خواندن نیست. استاندارد تعریف می کند که یک فایل PEM با:

```
-----BEGIN <type>-----
```
و به پایان می رسد:
```
-----END <type>-----
```

تمام محتوای دیگر داخل این کد base64 (حروف بزرگ و کوچک، اعداد، + و /) است. یک فایل PEM می تواند از چندین بلوک تشکیل شده باشد که می تواند توسط برنامه های دیگر استفاده شود. اگر یک فایل PEM حاوی چندین گواهی باشد، هر گواهی با بلوک های جداگانه به صورت زیر جدا می شود:

```
-----BEGIN CERTIFICATE-----
  //end-user
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //intermediate
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //root
-----END CERTIFICATE-----
```

### مثال فایل PEM

یک فایل PEM با بلوک CERTIFICATE معمولاً به شکل زیر است:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

یک فایل PEM با RSA مانند زیر شروع می شود.

```
-----BEGIN RSA PRIVATE KEY-----
```

## منابع ##

* [رمزگذاری کلید عمومی](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [چگونه فایل P7C ایجاد کنیم؟](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


