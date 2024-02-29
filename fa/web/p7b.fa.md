{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "P7B - فایل گواهی PKCS 7",
  "description": "درباره فرمت فایل P7C و APIهایی که می‌توانند فایل‌های P7C را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "P7B",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-p7-fab"
}
}،
  "lastmod": "2019-09-10"
}

## فایل P7B چیست؟

یک فایل P7B یک فایل گواهی امنیتی است که حاوی گواهی دیجیتال امن برای احراز هویت یک شخص یا یک دستگاه است. مانند فایل گواهی [.cer](/web/cer/)، یک فایل P7B را می توان با استفاده از گزینه Install Certificate با کلیک راست روی فایل نصب کرد. P7B از گزینه قالب بندی متفاوتی نسبت به فرمت فایل CER استفاده می کند. این شامل یک یا چند فایل گواهی دیجیتال X.509 است که از رمزگذاری base64 (ASCII) استفاده می کنند. فایل‌های P7B به‌عنوان یک فایل [ZIP](/compression/zip/) دریافت می‌شوند یا از مرجع صدور گواهی دریافت می‌شوند.

## فرمت فایل P7B

فایل‌های P7B به‌عنوان فایل‌های ASCII ساده ذخیره می‌شوند که می‌توانند در هر ویرایشگر متنی باز شوند. این شامل کلید عمومی است که یک رشته رمزگذاری شده است که از نظر خوانایی بی معنی است.

### نمونه فرمت فایل P7B

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## منابع ##

* [رمزگذاری کلید عمومی](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [چگونه فایل P7C ایجاد کنیم؟](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


