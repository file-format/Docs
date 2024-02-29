{
  "date": "2019-10-11",
  "keywords": [
"فایل mpkg",
"فرمت فایل mpkg",
"فایل mpkg چیست",
"فایل",
"نمونه mpkg",
"پسوند فایل mpkg",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل MPKG - فایل Meta Package",
  "description": "درباره فرمت فایل MPKG و API هایی که می توانند فایل های MPKG را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "MPKG",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-mpk-fag"
}
},
  "lastmod": "2021-04-02"
}

## فایل MPKG چیست؟

یک فایل با پسوند .mpkg یک فایل نصب کننده بایگانی است که بیشتر در سیستم عامل های MacOS یافت می شود. این شامل تمام فایل های نصب مورد نیاز برنامه بدون نیاز به نگه داشتن فایل های مرتبط به طور جداگانه است. یک فایل MPKG می‌تواند شامل فایل‌های بسته [PKG](/compression/pkg/) به عنوان یکی از فایل‌های نصب و سایر فایل‌ها باشد. فایل های MPKG را نمی توان با هیچ نرم افزار عمومی باز کرد و به طور خودکار در MacOS با استفاده از Apple Installer اجرا می شود.

## فرمت فایل MPKG

یک فایل MPKG حاوی انواع مختلفی از فایل‌ها است که برای نصب بسته‌های متعددی که در آن وجود دارد، مورد نیاز است. این را می توان از تصویر زیر مشاهده کرد که ساختار درختی یک فایل MPKG نمونه است. این ساختار درختی با استفاده از دستور درخت در ترمینال MacOS صادر می شود.

{{< figure src="../mpkg.png" alt="فرمت فایل MPKG" >}}

The description of different elements in the image is as follow.

«دایرکتوری بسته‌ها» - فهرستی از فایل‌های pkg، یعنی فهرستی از بسته‌های فرعی را ذخیره می‌کند.
دایرکتوری منابع - منابع مورد استفاده توسط pkg را ذخیره می کند، مانند منابع محلی و تصاویر، اسناد Rtf، اسناد pdf و غیره.
فایل Distribution.dist - یک سند xml حاوی اطلاعاتی مانند بسته های فرعی که باید نصب شوند و اسکریپت های زمان اجرا

نمونه فایل XML برای یک فایل MPKG بسته به بسته های فرعی مرتبط می تواند به شکل زیر باشد.

```
<?xml version="1.0" encoding="utf-8" standalone="no"?>
<installer-script minSpecVersion="1.000000" authoringTool="com.apple.PackageMaker" authoringToolVersion="3.0.6" authoringToolBuild="201">
    <title>myframework installer</title>
    <options customize="never" allow-external-scripts="no" rootVolumeOnly="false"/>
    <installation-check script="pm_install_check();"/>
    <volume-check script="pm_volume_check();"/>
    <script>function pm_volume_check() {
  if(!(my.target.systemVersion &amp;&amp; /* &gt;= */ system.compareVersions(my.target.systemVersion.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}

function pm_install_check() {
  if(!(/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}
</script>
    <choices-outline>
        <line choice="choice0"/>
    </choices-outline>
    <choice id="choice0" title="app">
        <pkg-ref id="com.macbook.myframeworkInstaller.pkg"/>
    </choice>
    <pkg-ref id="com.macbook.myframeworkInstaller.pkg" installKBytes="108" version="1.0" auth="Root">file:./Contents/Packages/app.pkg</pkg-ref>
</installer-script>
```
app.pkg - بسته فرعی است که باید نصب شود. این دایرکتوری از ساختار Bundle با فرمت pkg است. این شامل یک زیرشاخه Contents است.

## منابع

* [بسته‌های مسطح OSX](https://matthew-brett.github.io/docosx/flat_packages.html)

* [C++ MPKG Package Manager](https://github.com/puellavulnerata/mpkg)


