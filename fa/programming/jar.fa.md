{
  "date": "2019-10-11",
  "keywords": [
"شیشه",
".شیشه",
"فایل jar چیست",
"نحوه باز کردن یک فایل jar",
"افزونه",
"فایل",
"فایل jar",
"فرمت فایل jar",
"پسوند .jar"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "JAR - فرمت فایل بایگانی جاوا",
  "description": "درباره فرمت فایل JAR و APIهایی که می توانند فایل JAR را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "JAR",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ja-far"
}
}،
  "lastmod": "2020-09-10"
}

## فایل JAR چیست؟

یک فایل با پسوند jar یک فایل بایگانی جاوا است که شامل بسیاری از فایل های مرتبط با برنامه های کاربردی مختلف به عنوان یک فایل است. این فرمت فایل برای کاهش سرعت بارگیری یک اپلت جاوا دانلود شده در مرورگر از طریق تراکنش HTTP، با اجتناب از ایجاد چندین اتصال HTTP ایجاد شده است. یک فایل JAR می‌تواند حاوی فایل‌های کلاس جاوا ([.class](/programming/class/))، [images](/image/) و [sounds](/audio/) باشد. موارد منفرد داخل یک فایل JAR را می توان به صورت دیجیتالی توسط توسعه دهنده برنامه امضا کرد تا مبدا آنها را احراز هویت کند. فایل های JAR به طور منظم برای ایجاد API های کاربردی که حاوی عملکردهای خاص مربوط به آن API هستند استفاده می شوند.

## فرمت فایل JAR

JAR files are based on the popular [ZIP file format](/compression/zip/) that archives its individual content files in a single file. JAR file format supports compressions, resulting in a smaller file size for downloading and hence further improves the download time. The [JAR file specifications](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) artilce by Oracle gives complete details about the internal specifications of JAR files.

### فایل Manifest

هنگامی که یک فایل JAR ایجاد می شود، یک فایل مانیفست به طور خودکار در داخل آن ایجاد می شود که حاوی اطلاعات فراداده در مورد محتوای فایل JAR است. این فایل محتویاتی را نشان می دهد که در داخل فایل JAR بسته بندی شده اند. یک فایل Manifest معمولی به شکل زیر است که پوشه ها و کلاس های موجود در فایل JAR را نشان می دهد.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### مشخصات مانیفست

مشخصات مانیفست توسط Oracle به صورت زیر تعریف شده است.

«manifest-file»: خط جدید بخش اصلی \*individual-section

«بخش اصلی»: خط جدید اطلاعات نسخه \*ویژگی اصلی

`version-info`: Manifest-Version: version-number

«نصر-شماره»: رقم+{.رقم+}*

main-attribute: (هر ویژگی اصلی قانونی) خط جدید

individual-section: نام: مقدار newline \*perentry-attribute

perentry-attribute: (هر ویژگی perentry مشروع) خط جدید

`خط جدید`: CR LF | LF | CR (به دنبال LF نیست)

رقم: {0-9}

### JAR قابل اجرا

فایل‌های JAR همچنین می‌توانند شامل برنامه‌ای باشند که می‌تواند توسط ماشین مجازی جاوا (JVM) مشابه هر برنامه دیگری در سیستم‌عامل ویندوز مایکروسافت اجرا شود. در این مورد، JVM باید در مورد نقطه ورودی برنامه که هر کلاسی با روش اصلی استاتیک استاتیک است، بداند. فایل مانیفست چنین کلاسی را با هدر «کلاس اصلی» در قالب زیر شناسایی می‌کند:

```
Main-Class: com.example.MyClassName
```



## منابع

 * [JAR File Overview](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
 * [فرمت فایل JAR](https://en.wikipedia.org/wiki/JAR_(file_format))

