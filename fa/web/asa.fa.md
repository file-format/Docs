{
  "date": "2021-12-09",
  "keywords": [
"آسا",
".asa",
"فرمت فایل",
"نوع فایل",
"فایل .asa چیست؟"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASA - فایل پیکربندی ASP",
  "description": "در مورد اینکه فایل ASA چیست و APIهایی که می توانند فایل های ASA را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "ASA",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-as-faa"
}
},
  "lastmod": "2021-12-09"
}

## فایل ASA چیست؟

یک فایل ASA یک فایل پیکربندی است که برای پروژه های [ASP](/web/asp/)/ASP.NET ایجاد شده است. این شامل اعلامیه هایی از متغیرها، حاوی و توابع است که قرار است در سطح جهانی در برنامه قابل دسترسی باشند. همه صفحات در پروژه می توانند به این متغیرها و توابع دسترسی داشته باشند، بنابراین نیازی به بازنویسی آنها نیست. یکی از این نمونه ها صفحه Global.asa است که در دایرکتوری ریشه ذخیره می شود تا توسط سایر صفحات وب سایت ASP قابل دسترسی باشد. فایل های Global.asa اختیاری هستند، اما در صورت استفاده، هر برنامه می تواند تنها یک فایل Global.asa داشته باشد.

## فرمت فایل ASA - اطلاعات بیشتر

فایل های ASA فایل های متنی ساده با اطلاعات زیر هستند.

 * رویدادهای برنامه
 * رویدادهای جلسه
 * \<object> اعلامیه ها
 * اعلان های TypeLibrary
 * بخشنامه #شامل

## نمونه فایل ASA

یک فایل Global.asa می تواند چیزی شبیه به این باشد.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## منابع

* [فایل ASP Global.asa - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)


