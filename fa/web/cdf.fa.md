{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CDF - قالب تعریف کانال",
  "description": "در مورد اینکه یک فایل CDF چیست و APIهایی که می توانند فایل های CDF را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "CDF",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cd-faf"
}
},
  "lastmod": "2021-08-18"
}

## فایل CDF چیست؟

یک فایل با پسوند cdf. یک قالب فایل توزیع اطلاعات مبتنی بر XLM است که برای انتشار به‌روزرسانی‌های مکرر به‌عنوان «کانال» استفاده می‌شود. اطلاعات از هر سرور وب منتشر می شود و به طور خودکار به رایانه هایی با برنامه های دریافت کننده سازگار مانند مرورگرهای وب تحویل داده می شود. کاربران در کانال‌های فعال مشترک می‌شوند و به‌روزرسانی‌های برنامه‌ریزی‌شده را به دسکتاپ تحویل می‌دهند.
فایل‌های CDF قبلاً همراه با فناوری‌های Active Channel، Active Desktop و Smart Offline Favorites مایکروسافت استفاده می‌شدند.

## فرمت فایل CDF

فایل های CDF به عنوان فایل های XML ذخیره می شوند که یک فرمت فایل وب عمومی برای تبادل اطلاعات است. فرمت فایل CDF اکنون یک فرمت قدیمی است و هرگز به طور گسترده مورد استفاده قرار نگرفت. در مقایسه با این، RSS نت اسکیپ مشهورتر و پرکاربردتر بود.

### نمونه فرمت فایل CDF

در زیر یک مثال کلی از فرمت فایل CDF آورده شده است.

```
<?xml version=1.0 encoding=UTF-8?>
<CHANNEL HREF=http://domain/folder/pageOne.extension
BASE=http://domain/folder/
LASTMOD=1998-11-05T22:12
PRECACHE=بله
LEVEL=0>
<TITLE>عنوان کانال</TITLE>
<ABSTRACT>خلاصه مطالب کانال.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY=14/>
</SCHEDULE>
<LOGO HREF=wideChannelLogo.gif STYLE=IMAGE-WIDE/>
<LOGO HREF=imageChannelLogo.gif STYLE=IMAGE/>
<LOGO HREF=iconChannelLogo.gif STYLE=ICON/>
<ITEM HREF=pageTwo.extension
    LASTMOD=1998-11-05T22:12
    PRECACHE=بله
LEVEL=1>
<TITLE>عنوان صفحه دو</TITLE>
<ABSTRACT>خلاصه مطالب صفحه دو.</ABSTRACT>
<LOGO HREF=pageTwoLogo.gif STYLE=IMAGE/>
<LOGO HREF=pageTwoLogo.gif STYLE=ICON/>
</ITEM>
</CHANNEL>
```

## منابع

* [قالب تعریف کانال - توسط ویکی پدیا](https://en.wikipedia.org/wiki/Channel_Definition_Format)


