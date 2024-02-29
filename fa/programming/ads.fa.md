
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
}،
  "draft" : "false",
  "toc" : true,
  "title" : "فایل ADS - فرمت فایل مشخصات Ada",
  "description":"با مثال و APIهایی که می توانند فایل های ADS را ایجاد و باز کنند، با فرمت فایل ADS آشنا شوید.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads-fa",
      "parent" : "programming"
}
}،
  "lastmod" : "2022-10-30"
}

## فایل ADS چیست؟

یک فایل ADS یک فایل مشخصات برای پروژه برنامه نویسی Ada است. این شبیه به یک کلاس برای جاوا یا جفت هدر و پیاده سازی در مورد C++ است. مشخصات عمومی و خصوصی بسته Ada در فایل .ads ذخیره می شود. در مقابل، فایل adb. شامل پیاده سازی یا بدنه های Ada است. مانند [C++](/programming/cpp/)، Ada جداسازی بین مشخصات و پیاده سازی ها را مستقل از OOP ارائه می دهد.

فایل های ADS را می توان در هر ویرایشگر متنی مانند Microsoft Notepad، Notepad++ و Atom باز کرد.

## فرمت فایل ADS

فایل‌های ADS در قالب فایل متنی ساده هستند و با هر ویرایشگر متنی قابل باز کردن/ویرایش هستند. بسته های Ada را می توان در سلسله مراتب سازماندهی کرد. واحد فرزند را می توان به روش زیر اعلام کرد:

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## منابع

 * [بسته‌های Ada](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

