{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "MSG - فرمت ایمیل Microsoft Outlook",
  "description": "درباره فرمت فایل MSG و APIهایی که می‌توانند فایل‌های MSG را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "MSG",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ms-fag"
}
}،
  "lastmod": "2019-09-10"
}

## فایل MSG چیست؟

MSG is a file format used by [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) and Exchange to store email messages, contact, appointment, or other tasks. Such messages may contain one or more email fields, with the sender, recipient, subject, date, and message body, or contact information, appointment particulars, and one or more task specifications. The properties that constitute the Message object, including are also a part of the MSG file.  MSG file has headers, main message body, and hyperlinks as plain ASCII text. MSG files are also suitable with the programs that need Microsoft's Messaging Applications Programming Interface (MAPI).

## ساختار فایل MSG

فرمت CFB_3 پایه فایل MSG است. این پارادایم مبتنی بر مفاهیم ذخیره‌سازی و جریان است که کاملاً به فهرست‌ها و فایل‌ها نزدیک است. بنابراین یک تفاوت عمده در اولی کل سلسله مراتب است که در یک فایل مجزا به نام فایل ترکیبی بسته بندی شده است. اشیاء فایل های پیام را تشکیل می دهند و از یک ویژگی یا مجموعه های آن تشکیل شده اند. این توانایی برنامه ها را برای ذخیره داده های پیچیده و ساختار یافته در یک فایل تسهیل می کند. این فرمت همچنین چندین ذخیره سازی را مشخص می کند، هر ذخیره سازی نشان دهنده شی Message به عنوان یک جزء اصلی است. این ذخیره‌سازی‌ها حاوی تعدادی جریان هستند که ویژگی آن جزء را نشان می‌دهند. تودرتو ذخیره سازی نیز امکان پذیر است.

## ویژگی های Mapi

در سطح بالای فایل .msg، ذخیره‌سازی‌ها حاوی جریان‌هایی هستند که ویژگی‌ها را در آنها ذخیره می‌کنند. خواص را می توان به صورت زیر دسته بندی کرد:

* خواص طول ثابت

* ویژگی های طول متغیر

* خواص چند ارزش


صرف نظر از دسته بندی، یک ویژگی یا برچسب گذاری شده یا نامگذاری شده است. با این حال، اطلاعات نگاشت مناسب برای ویژگی‌های نام‌گذاری شده، همانطور که توسط ذخیره‌سازی نگاشت آنها مشخص شده است، مورد نیاز است.

## انبارها

فضای ذخیره‌سازی اجزای کلیدی شیء پیام را تشکیل می‌دهد. فرمت فایل MSG حافظه های زیر را نشان می دهد:

## ساختار سطح بالا

شیء پیام کل سطح بالای فرمت فایل MSG را نشان می دهد. بسته به نوع، ویژگی‌ها، تعداد گیرنده و اشیاء پیوست، یک شیء پیام می‌تواند ذخیره‌سازی جریانی متفاوتی در فایل MSG مربوطه خود داشته باشد.

### رابطه با سایر ساختارها

فرمت فایل Msg دارای روابط زیر با ساختارهای دیگر است:

* اساس msg فرمت فایل باینری فایل مرکب است.

* ویژگی های استفاده شده توسط پیام و پروتکل شیء پیوست توسط این فرمت استفاده می شود.


## سناریوهایی برای جلوگیری از فرمت های MSG

شیء پیام را می توان بین مشتریان یا فروشگاه های پیام که از سیستم فایل .msg استفاده می کنند به اشتراک گذاشت. شرایط کمی وجود دارد که در آن ذخیره یک شیء پیام در قالب فایل msg مناسب نباشد. مثلا:

* در صورت نگهداری از یک آرشیو بزرگ مستقل، بهتر است از قالبی با امکانات کامل استفاده کنید که در آن نماها با دقت بیشتری رندر شوند.

* اگر گیرنده ناشناخته باشد، ممکن است فرمت توسط گیرنده پشتیبانی نشود و خصوصی یا نامربوط تحویل داده شود.


## نمونه فایل MSG

To get an idea of how a MSG file looks like, you can download a [sample MSG file](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) and open on your computer to view its contents.

## منابع

* [[MS-OXMSG]: فرمت فایل MSG Outlook](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)


