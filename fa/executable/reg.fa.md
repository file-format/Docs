{
  "date": "2021-08-02",
  "keywords": [
"فایل reg",
"فرمت فایل reg",
"فایل reg چیست",
"فایل",
"مثال reg",
"پسوند فایل reg",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "با فرمت فایل REG و APIهایی که می توانند فایل های REG را ایجاد و باز کنند آشنا شوید.",
  "title": "REG - فایل رجیستری ویندوز",
  "linktitle": "REG",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-re-fag"
}
},
  "lastmod": "2021-08-02"
}

## فایل REG چیست؟

یک فایل REG به سادگی یک فایل متنی با پسوند reg است. این فایل ها معمولاً با صادر کردن کلیدهای معمولی از رجیستری ایجاد می شوند. این فایل ها همچنین می توانند به عنوان یک نسخه پشتیبان از رجیستری استفاده شوند (به خصوص این مرحله قبل از ایجاد تغییرات مهم است!). می بینید که برخی آنها را به عنوان فایل های قابل دانلود در همان سایت هایی که به شما نشان می دهد چگونه هک رجیستری را انجام دهید در دسترس قرار داده اند. یک فایل REG برای ایجاد تغییرات دستی در رجیستری و صادرات آن تغییرات مفید است. فقط فایل را کمی پاک کنید و سپس آن را با دیگران به اشتراک بگذارید.

## فرمت فایل REG

فرمت فایل REG برای صادرات و وارد کردن بخش‌هایی از رجیستری ویندوز با استفاده از نحو مبتنی بر INI طراحی شده است. رجیستری ویندوز یک پایگاه داده رابطه ای یا سلسله مراتبی است که تنظیمات سطح پایین را برای سیستم عامل مایکروسافت ویندوز و سایر برنامه هایی که از رجیستری ویندوز استفاده می کنند نگه می دارد. به عنوان روش دیگر، می توان گفت رجیستری یا رجیستری ویندوز متشکل از اطلاعات، گزینه ها، تنظیمات و سایر مقادیر برای برنامه ها و سخت افزارهای نصب شده بر روی تمام نسخه های سیستم عامل مایکروسافت ویندوز است.

### نحو فایل REG
در اینجا برخی از عناصر کلیدی به عنوان بخشی از نحو فایل REG آورده شده است:
- **RegistryEditorVersion**: به عنوان مثال Windows Registry Editor Version 5.00 برای Windows 2000، Windows XP و Windows Server 2003.
- **خط خالی**: شروع یک مسیر رجیستری جدید را مشخص می کند.
- **RegistryPathx**: مسیر کلید فرعی که اولین مقداری که وارد می کنید را در خود نگه می دارد.
- **DataItemNamex**: نام مورد داده ای که می خواهید وارد کنید.
- **DataTypex**: نوع داده برای مقدار رجیستری.

کلیدها در فایل های reg. با استفاده از نحو زیر ذخیره می شوند:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
می توانید مقدار پیش فرض یک کلید را با استفاده از @ به جای Value Name ویرایش کنید:
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### مثال

در اینجا یک نمونه از فایل REG است
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## منابع

* [رجیستری ویندوز- توسط ویکی پدیا] (https://en.wikipedia.org/wiki/Windows_Registry)

* [نحوه افزودن، تغییر یا حذف کلیدهای فرعی و مقادیر رجیستری با استفاده از یک فایل reg.](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete- registry-subkeys-and-values-by-using-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)


