{
  "date": "2019-10-11",
  "keywords": [
"crt",
"فایل crt",
"فرمت فایل crt",
"نوع فایل crt",
"فایل",
"نوع",
"فایل crt چیست"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "CRT - فرمت فایل گواهی امنیتی",
  "description": "درباره فرمت فایل CRT و APIهایی که می‌توانند فایل‌های CRT را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "CRT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cr-fat"
}
}،
  "lastmod": "2019-09-10"
}

## فایل CRT چیست؟

یک فایل با پسوند crt. یک فایل گواهی امنیتی است که توسط وب سایت های امن برای ایجاد اتصالات امن از سرور وب به مرورگر استفاده می شود. وب‌سایت‌های ایمن این امکان را فراهم می‌کنند که انتقال داده‌ها، ورود به سیستم، تراکنش‌های کارت پرداخت، و مرور محافظت شده در سایت را ایمن کنند. اگر یک وب سایت امن باز کنید، نماد قفل را در نوار آدرس می بینید. اگر روی آن کلیک کنید، می توانید جزئیات گواهی نصب شده را مشاهده کنید. شرکت های بین المللی مانند Verisign و Thawte این گواهینامه های SSL را توزیع می کنند.

## فرمت فایل CRT

فایل های CRT در فرمت ASCII هستند و می توانند در هر ویرایشگر متنی برای مشاهده محتویات فایل گواهی باز شوند. این استاندارد از استاندارد گواهی X.509 پیروی می کند که ساختار گواهی را تعریف می کند. فیلدهای داده ای را که باید در گواهی SSL گنجانده شود را مشخص می کند. CRT متعلق به فرمت PEM گواهینامه ها است که فایل های کدگذاری شده ASCII Base64 هستند.

### ساختار فایل PEM

یک فایل PEM می تواند چندین گواهی داشته باشد. در چنین حالتی، هر گواهی در فایل PEM از ساختار زیر پیروی می کند.

```
---- BEGIN CERTIFICATE----
...
...
...
Encoded string for encryption of data
...
...
...
----END CERTIFICATE----
```

### نمونه فرمت فایل CRT

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## منابع ##

* [Public Keys, Private Keys, and Certificates](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

