{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "MBOX - فایل صندوق پستی ایمیل",
  "description": "درباره فرمت فایل MBOX و APIهایی که می‌توانند فایل‌های MBOX را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "MBOX",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-mbo-fax"
}
}،
  "lastmod": "2019-09-10"
}

## فایل MBOX چیست؟

فرمت فایل MBox یک اصطلاح عمومی است که محفظه ای برای جمع آوری پیام های پست الکترونیکی را نشان می دهد. پیام‌ها به همراه پیوست‌هایشان در داخل ظرف ذخیره می‌شوند. پیام‌های کل پوشه در یک فایل پایگاه داده ذخیره می‌شوند و پیام‌های جدید به انتهای فایل اضافه می‌شوند. برنامه های کاربردی و API متعددی از فرمت فایل MBox مانند Apple Mail و Mozilla Thunderbird پشتیبانی می کنند.

## فرمت فایل MBOX ##

The MBox file format remained non-standardized for quite long time until 2005 when the application/mbox  was standardized as [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Messages, in RFC 2822 format, are concatenated inside MBox file format one after another. Each message begins with a separator line that identifies the message sender, and also identifies the date and time at which the message was received by the final recipient (either the last-hop system in the transfer path, or the system which serves as the recipient's mailstore). Each message is typically terminated by an empty line. The end of the database is usually recognized by either the absence of any additional data, or by the presence of an explicit end-of-file marker.

## خواندن پیام از فایل MBox ##

خواننده یک فایل mbox را به دنبال خطوط From_ اسکن می کند. هر خط From_ شروع یک پیام را نشان می دهد. خواننده نباید سعی کند از این واقعیت استفاده کند که هر خط From_ (از ابتدای فایل گذشته) خط خالی است. هنگامی که خواننده پیامی را پیدا کرد، یک فرستنده پاکت نامه (احتمالاً خراب) و تاریخ تحویل را از خط From_ استخراج می کند. سپس تا خط بعدی From_ یا انتهای فایل، هر کدام که اول باشد، خوانده می شود. خط خالی نهایی را حذف می کند و نقل قول از خطوط >From_ و >>From_ و غیره را حذف می کند. نتیجه یک پیام RFC 822 است.

## ملاحظات رمزگذاری ##

محتویات یک فایل MBox زمانی که ایمیل دریافتی حاوی یک فایل Mbox به عنوان ضمیمه است و در فایل Mbox دیگری ذخیره می شود، می تواند به طور غیر قابل برگشتی در هم آمیخته شود. برای جلوگیری از این امر، سیستم‌های پیام‌رسان باید پایگاه داده mbox را با رمزگذاری انتقال غیرشفاف (مانند BASE64 یا Quoted-Printable) هر زمان که چنین شیئی از طریق پروتکل‌های پیام منتقل می‌شود، رمزگذاری کنند. پیاده‌کننده‌ها همچنین باید آماده باشند تا در صورت دریافت داده‌های ناسازگار، داده‌های mbox را به صورت محلی رمزگذاری کنند.

## منابع ##

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)

* [Mbox - Wikipedia](https://en.wikipedia.org/wiki/Mbox)


