{
  "date": "2022-06-24",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل SY_ - فایل SYS فشرده",
  "description": "درباره قالب فایل SY_ و APIهایی که می‌توانند فایل‌های SY_ را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "SY_",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-sy-fa_"
}
},
  "lastmod": "2022-06-24"
}

## فایل SY_ چیست؟

یک فایل SY_ یک فایل .sys فشرده است که توسط نصب کنندگان نرم افزار برای کاهش حجم فایل های نصب بسته بندی شده در داخل نصب کننده استفاده می شود. این باعث کاهش اندازه کلی نصب کننده می شود. فایل های SY_ را می توان با استفاده از ابزار خط فرمان Microsoft Expand که یک یا چند فایل فشرده را گسترش می دهد، گسترش داد.

## فرمت فایل SY_ - اطلاعات بیشتر

فایل های SY_ به عنوان فایل های باینری فشرده روی دیسک ذخیره می شوند. با این حال، فرمت فایل داخلی آنها به صورت عمومی در دسترس نیست. ابزار Microsoft Expand خط فرمان می‌تواند فایل‌های SY_ را با استفاده از یکی از خطوط فرمان زیر گسترش دهد.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
پس از گسترش، فایل‌های SY_ به فایل [SYS](/system/sys/) تبدیل می‌شوند.

فایل های SY_ شبیه فایل های EX_ و DL_ هستند.

## منابع

 * [StuffIt - توسط ویکی پدیا](https://en.wikipedia.org/wiki/StuffIt)
 * [Microsoft Expand](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

