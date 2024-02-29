{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "EMLX - فرمت فایل ایمیل اپل",
  "description": "درباره فرمت فایل EMLX و APIهایی که می‌توانند فایل‌های EMLX را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "EMLX",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-eml-fax"
}
}،
  "lastmod": "2019-09-10"
}

## فایل EMLX چیست؟

فرمت فایل EMLX توسط اپل پیاده سازی و توسعه یافته است. برنامه Apple Mail از فرمت فایل EMLX برای صادرات ایمیل ها استفاده می کند. برنامه های دیگری نیز وجود دارند که می توانند فایل های EMLX را باز کرده و آنها را به فرمت های فایل دیگر تبدیل کنند.

## تاریخچه مختصر فرمت فایل EMLX

سیستم عامل Mac OS X برنامه ایمیل موجود، NeXTMail را که توسط NeXT به عنوان بخشی از سیستم عامل NeXTSTEP ایجاد شده بود، پذیرفت. اپل پس از خرید NeXT ویژگی‌های خود را ارتقا داد و اکنون به اپلیکیشن ایمیل اپل میل تبدیل شد که به عنوان سرویس گیرنده ایمیل پیش‌فرض استفاده می‌شود. ایمیل های صادر شده از طریق Apple Mail مستقیماً به عنوان فایل های EMLX ذخیره می شوند. علاوه بر این، زمانی که شخصی با دوبار کلیک کردن بر روی سیستم عامل مک، آن ها را باز می کند، سرویس گیرنده ایمیل پیش فرض برای فایل های EMLX است.

## فرمت فایل EMLX

فایل‌های EMLx فایل‌های مبتنی بر متن ساده هستند که می‌توانند در هر ویرایشگر متنی مانند Notepad باز شوند. ساختار فایل EMLX از سه بخش تشکیل شده است:

* تعداد بایت برای پیام - طول خود پیام، به صورت اعشاری با اسکی نوشته شده، با 0x0a خاتمه می یابد.

* خود پیام

* فراداده پیام در قالب XML plist


اینها را می توان با کمک نمونه ایمیل زیر استخراج شده از Apple Mail به عنوان EMLX و باز کردن در یک ویرایشگر متن، بهتر توضیح داد.

### مثال EMLX

```
875       
X-Spam-Checker-Version: SpamAssassin 3.3.2 (2011-06-06) on ******.*********.***
X-Spam-Level:
X-Spam-Status: No, score#-3.2 required#4.2 tests#BAYES_00,RP_MATCHES_RCVD,
        SPF_PASS,TVD_SPACE_RATIO autolearn#ham version#3.3.2
Received: from [127.0.0.1](******.*********.*** [***.**.**.**])
        by ******.*********.*** (8.14.5/8.14.5) with ESMTP id r2TN8m4U099571
        for <****@*********.***>; Fri, 29 Mar 2013 19:08:48 -0400 (EDT)
        (envelope-from ****@*********.***)
Subject: very simple
From: Sender <****@*********.***>
Content-Type: text/plain; charset#us-ascii
Message-Id: <4E83618E-BB56-404F-8595-87352648ADC7@*********.***>
Date: Fri, 29 Mar 2013 19:09:06 -0400
To: Reciever <****@*********.***>
Content-Transfer-Encoding: 7bit
Mime-Version: 1.0 (Apple Message framework v1283)
X-Mailer: Apple Mail (2.1283)

message Foo
--
Sender
http://www.la-grange.net/karl/

<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version#"1.0">
<dict>
        <key>date-sent</key>
        <real>1364598546</real>
        <key>flags</key>
        <integer>8590195713</integer>
        <key>original-mailbox</key>
        <string>imap://********@127.0.0.1:11143/mail/2013/03</string>
        <key>remote-id</key>
        <string>41147</string>
        <key>subject</key>
        <string>very simple</string>
</dict>
</plist>
```

در این مثال، 875 طول کل پیام را نشان می دهد. فراداده پیام در ضمیمه شده است<plist> برچسب ها و پرچم ها به شرح زیر است:

|فیلد|توضیحات|مقدار
---|---|---|
|0|خواندن|1 << 0
|1|حذف شده|1 << 1
|2|پاسخ|1 << 2
|3|رمزگذاری شده|1 << 3
|4|پرچم گذاری شده|1 << 4
|5|اخیرا|1 << 5
|6|پیش نویس|1 << 6
|7|اولیه (دیگر استفاده نمی شود)|1 << 7
|8|ارسال شده|1 << 8
|9|تغییر مسیر|1 << 9
|10-15|تعداد پیوست|3F << 10 (6 بیت)
|16-22|سطح اولویت|7F << 16 (7 بیت)
|23|امضا|1 << 23
|24|آشغال است|1 << 24
|25|آشغال نیست|1 << 25
|26-28|اندازه قلم دلتا|7 << 26 (3 بیت)
|29|سطح نامه های ناخواسته ثبت شد|1 << 29
|30|هایلایت کردن متن در تاک|1 << 30
|31|(استفاده نشده)|

## همچنین ببینید ##

* [EML](/email/eml/)

* [MSG](/email/msg/)


