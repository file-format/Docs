{
  "date": "2019-10-11",
  "keywords": [
"فایل mf",
"mf",
"افزونه",
"قالب",
"فرمت فایل mf"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "MF - فرمت فایل مانیفست جاوا",
  "description": "درباره فرمت فایل MF و API هایی که می توانند فایل های MF را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "MF",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-m-faf"
}
}،
  "lastmod": "2020-09-10"
}

## فایل MF چیست؟

فایلی با پسوند mf. یک فایل مانیفست جاوا است که حاوی اطلاعاتی در مورد ورودی های فایل [JAR](/programming/jar/) منفرد است. خود فایل MF در داخل فایل JAR قرار دارد و تمام پسوندها و تعریف های مربوط به بسته را ارائه می کند. فایل های JAR را می توان برای استفاده به عنوان یک فایل اجرایی تولید کرد. در چنین حالتی، فایل mainfest کلاس اصلی برنامه را مشخص می کند که حاوی دستور **`public static void main`** است. فایل‌های مانیفست با نام MANIFEST.MF نامگذاری می‌شوند و می‌توانند با هر ویرایشگر متنی در سیستم‌عامل‌های Windows، MacOS و Linux باز شوند.

## مشخصات فرمت فایل مانیفست

[Manifest file format specifications](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) are available by Oracle in their guide for JAR file format. A Manifest file comprises of main sections that are followed by a list of sections for individual JAR file entries. Each section follows some rules and restrictions.

### بخش های اصلی

یک بخش اصلی:

* حاوی اطلاعاتی در مورد امنیت و پیکربندی فایل JAR است

* حاوی اطلاعاتی در مورد برنامه یا پسوندی است که فایل JAR بخشی از آن است

* ویژگی های اصلی را برای هر آیتم مانیفست فردی تعریف می کند


**نکته**: هیچ ویژگی در این بخش را نمی توان Name نامید.

### بخش های فردی

یک بخش جداگانه ویژگی های مختلفی را برای بسته ها یا فایل های یک فایل JAR تعریف می کند. هر بخش باید با یک ویژگی به نام Name شروع شود که مقدار آن باید یک مسیر نسبی به فایل یا یک URL مطلق ارجاع دهنده داده های خارج از بایگانی باشد.

### مشخصات مانیفست

|توضیحات|توضیحات|
---|---|
|manifest-file|خط جدید بخش اصلی *individual-section|
|بخش اصلی|خط جدید اطلاعات نسخه *ویژگی اصلی|
|version-info|Manifest-Version : نسخه-شماره|
|version-number|digit+{.digit+}*|
|main-attribute|(هر ویژگی اصلی قانونی) newline|
|individual-section|Name : value newline *perentry-attribute|
|perentry-attribute|(هر ویژگی perentry قانونی) newline|
|newline|CR LF | LF | CR (بدون LF)|
| رقم|{0-9}|

## منابع

 * [Oracle - JAR File Format](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
 * [فرمت فایل JAR](https://en.wikipedia.org/wiki/JAR_(file_format))

