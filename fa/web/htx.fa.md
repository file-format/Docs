{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "فایل HTX - فرمت فایل پسوند HTML",
  "description": "راهنمای فرمت فایل شما برای یادگیری فایل HTX و APIهایی که می توانند فایل HTX را ایجاد و باز کنند.",
  "linktitle": "HTX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ht-fax"
}
}،
  "lastmod": "2019-09-10"
}

## فایل HTX چیست؟

یک فایل HTX در واقع یک فایل HTML است که حاوی متغیرهای داده برای نمایش نتایج جستجوی پایگاه داده به عنوان یک صفحه وب است. فایل‌های HTX که عمدتاً با نرم‌افزار توسعه وب مایکروسافت فرانت‌پیج ایجاد می‌شوند، ذخیره می‌شوند تا در همان پوشه‌ای که فایل اتصال دهنده پایگاه داده اینترنت (.IDC) مربوطه ذخیره شوند.

فایل های HTX را می توان با برنامه هایی مانند Microsoft FrontPage و هر ویرایشگر متنی مانند Notepad، TextEdit یا Atom باز کرد.

## فرمت فایل HTX

فایل های HTX به عنوان فایل متنی ساده با کد برای بازیابی داده ها از پایگاه داده و ذخیره در متغیرها برای نمایش ذخیره می شوند.


### مثال فایل HTX

نمونه ای از فایل HTX به شرح زیر است که یک هدر صفحه برای نمایش محدودیت پرس و جو و اسناد نمایش داده شده در صفحه برای نمایش به کاربر تعریف می کند.

```
<H4>
<%if CiMatchedRecordCount eq 0%>
No documents matched the query "<%EscapeHTMLCiRestriction%>".</H4>
<%else%>
<H4>Documents <%CiFirstRecordNumber%> to <%CiLastRecordNumber%> of
<%if CiMatchedRecordCount eq CiMaxRecordsInResultSet%>
the first
<%endif%>
<%CiMatchedRecordCount%> matching the query
"<%EscapeHTMLCiRestriction%>".
<%endif%>
</H4>
```

خروجی این نمونه کد به صورت زیر است.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

همانطور که مشاهده می شود، فایل HTX قالبی است که نحوه بازگشت و نمایش نتایج را به کاربران نهایی فرمت می کند. این در قالب HTML با برخی پسوندهای IIS و خدمات نمایه سازی نوشته شده است. این پسوندها شامل نام متغیرها و کدهای دیگر برای پردازش نتایج هستند.

## منابع

* [قالب‌بندی نتایج در فایل Htx.](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)


