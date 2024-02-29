{
  "date": "2021-04-23",
  "keywords": [
"فایل پیکربندی",
"فایل های پیکربندی",
"پیکربندی فرمت فایل",
"افزونه",
"قالب",
"فایل پیکربندی git",
"فایل های پیکربندی در لینوکس",
"فایل کانفیگ چیست",
"فایل کانفیگ php",
"نمونه فایل پیکربندی ssh",
"نمونه فایل پیکربندی aws",
"نمونه فایل پیکربندی پایتون"
]،
  "author": {
    "display_name": "Muhammad Umar"
}،
  "draft": "false",
  "toc": true,
  "title": "CONFIG - فایل پیکربندی",
  "description": "با مثال CONFIG و APIهایی که می توانند فایل های CONFIG را ایجاد و باز کنند، با فرمت فایل CONFIG آشنا شوید.",
  "linktitle": "CONFIG",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-confi-fag"
}
}،
  "lastmod": "2021-04-23"
}

## فایل CONFIG چیست؟
یک فایل CONFIG به عنوان فایل پیکربندی شناخته می شود. برای پیکربندی پارامترها و تنظیمات اولیه برای چندین نرم افزار کامپیوتری استفاده می شود. برخی از نرم افزارها فقط **فایل های پیکربندی** خود را هنگام راه اندازی می خوانند. برخی دیگر فایل های پیکربندی را برای تغییرات دوره ای بررسی می کنند.

## فرمت فایل CONFIG
فرمت **CONFIG File** برای فرآیندهای سرور، برنامه های نرم افزاری و تنظیمات سیستم عامل استفاده می شود. یک برنامه نویس می تواند کد بنویسد تا به یک نرم افزار دستور دهد تا فایل های پیکربندی را بعد از مدت زمان معینی دوباره و دوباره بخواند و تغییرات را در روند فعلی اعمال کند. هیچ استاندارد قطعی یا قرارداد قوی برای سیستم فایل CONFIG وجود ندارد. برای مثال، فایل Web.config مایکروسافت متعلق به فرمت فایل CONFIG است که از مجموعه برچسب‌های مبتنی بر [XML](/web/xml/) تشکیل شده است. را می توان با Microsoft Visual Studio یا هر ویرایشگر متن دیگری ویرایش کرد.

## نمونه هایی از فایل های پیکربندی:
از آنجایی که فایل های پیکربندی با پیروی از هیچ قانون، استاندارد یا قراردادی ایجاد نمی شوند، ممکن است این فایل ها با استفاده از فرمت های مختلف نوشته شده باشند. یک فایل .config ممکن است بر اساس XML، [JSON](/web/json/) یا هر قالب دیگری باشد. در زیر نمونه هایی از فایل های پیکربندی برای سیستم عامل ها و نرم افزارهای معروف آورده شده است:

### فایل های پیکربندی در لینوکس
 Every Linux program is an executable file keeping the list of **opcodes** the CPU executes to accomplish typical operations. The operations of almost every program can be customized to your requirements by changing its configuration files. Several configuration files in the Linux system are in the /etc directory. The configuration files can be classified into the following categories:
|دسته|مثال| نظرات|
---|---|---|
|دسترسی به فایل‌ها|/etc/host.conf|به سرور دامنه شبکه می‌گوید چگونه نام میزبان را جستجو کند.|
|راه اندازی و ورود/logout|/etc/rc.d/rc.local| رسمی نیست. ممکن است از rc، rc.sysinit یا /etc/inittab فراخوانی شود.|
|سیستم فایل|/etc/mtools.conf|پیکربندی برای تمام عملیات (mkdir، کپی، فرمت، و غیره) در یک سیستم فایل نوع DOS.|
|System Administration|/etc/shells|لیست پوسته های احتمالی موجود در سیستم را نگه می دارد.|
|شبکه|/etc/gated.conf|پیکربندی برای gated. فقط توسط دیمون دروازه ای استفاده می شود.|
|دستورات سیستم|/etc/logrotate.conf|پیکربندی برای پیوند دهنده پویا.|
|Daemons|/etc/httpd.conf|فایل پیکربندی آپاچی، سرور وب. این فایل معمولاً در /etc.| نیست
|برنامه های کاربری| /etc/lynx.cfg| تنظیمات پروکسی|
### مثال فایل AWS CONFIG
تنظیمات پیکربندی و اعتبارنامه‌های پرکاربرد را می‌توان در فایل‌های CONFIG که توسط AWS CLI نگهداری می‌شوند، ذخیره کرد. فایل CONFIG باید یک فایل متنی ساده باشد که از فرمت زیر استفاده کند:
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### مثال فایل SSH CONFIG
فایل پیکربندی سمت کلاینت OpenSSH CONFIG نام دارد و در پوشه .ssh ذخیره می شود. فایل SSH CONFIG از ساختار زیر تشکیل شده است:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### مثال فایل CONFIG پایتون
یک فایل CONFIG پایتون می تواند به شکل زیر باشد:

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## منابع

 * [آشنایی با فایل های پیکربندی لینوکس](https://developer.ibm.com/technologies/linux/articles/l-config/)
 * [Configuration and credential file settings](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
 * [فایل های پیکربندی در پایتون](https://martin-thoma.com/configuration-files-in-python/)

