{
  "date": "2021-06-28",
  "keywords": [
"فایل cgi",
"فایل cgi چیست",
"فایل",
"نمونه cgi",
"پسوند فایل cgi",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل CGI و API هایی که می توانند فایل های CGI را ایجاد و باز کنند، بیاموزید.",
  "title": "CGI - فایل اسکریپت رابط دروازه مشترک",
  "linktitle": "CGI",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-cg-fai"
}
},
  "lastmod": "2021-06-28"
}

## فایل CGI چیست؟
یک فایل CGI به عنوان یک اسکریپت Common Gateway Interface شناخته می شود که توسط یک وب سرور برای اجرای یک برنامه خارجی برای پردازش درخواست های کاربر استفاده می شود. اسکریپتی که در فایلی با پسوند cgi. ذخیره می شود معمولاً به زبان های برنامه نویسی C یا Perl نوشته می شود. از روزهای اولیه وب، زمانی که توسعه دهندگان وب می خواستند پایگاه های داده را به سرورهای وب خود متصل کنند، معرفی شده بود. سروری که از یک دروازه مشترک بین وب سرور و پایگاه داده پشتیبانی می کند، برای اجرای کد CGI مناسب است.

## فرمت فایل CGI
اسکریپت‌های CGI توسط وب سرور استفاده می‌شوند تا مالک را در پیکربندی نحوه مدیریت URL استفاده کند. این رویه معمولاً با علامت گذاری یک فهرست جدید (جایی که اسناد عمدتاً در آن قرار دارند) به عنوان حاوی اسکریپت های CGI انجام می شود. نام رایج آن cgi-bin است. به عنوان مثال، /usr/local/apache/htdocs/cgi-bin را می توان به عنوان دایرکتوری CGI در سرور وب انتخاب کرد. هنگامی که یک مرورگر وب یک URL را درخواست می کند که به فایلی در دایرکتوری CGI اشاره می کند، به جای ارسال ساده آن فایل (/usr/local/apache/htdocs/cgi-bin/printenv.pl) به مرورگر وب، HTTP سرور اسکریپت مشخص شده را اجرا می کند و خروجی اسکریپت را به مرورگر وب برمی گرداند. به طور خلاصه، هر چیزی که اسکریپت CGI به خروجی استاندارد ارسال شود، به جای نمایش در پایانه پنجره، به سرویس گیرنده وب منتقل می شود.

### مثال CGI

اسکریپت زیر CGI نوشته شده در پرل که تمام متغیرهای محیطی را که توسط وب سرور ارسال می شود نشان می دهد:
```
#!/usr/bin/env perl

=head1 DESCRIPTION

printenv — a CGI program that just prints its environment

=cut
print "Content-Type: text/plain\n\n";

for my $var ( sort keys %ENV ) {
    printf "%s=\"%s\"\n", $var, $ENV{$var};
}
```

خروجی به صورت زیر خواهد بود:
```
COMSPEC="C:\Windows\system32\cmd.exe"
DOCUMENT_ROOT="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/htdocs"
GATEWAY_INTERFACE="CGI/1.1"
HOME="/home/SYSTEM"
HTTP_ACCEPT="text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8"
HTTP_ACCEPT_CHARSET="ISO-8859-1,utf-8;q=0.7,*;q=0.7"
HTTP_ACCEPT_ENCODING="gzip, deflate, br"
HTTP_ACCEPT_LANGUAGE="en-us,en;q=0.5"
HTTP_CONNECTION="keep-alive"
HTTP_HOST="example.com"
HTTP_USER_AGENT="Mozilla/5.0 (Windows NT 6.1; WOW64; rv:67.0) Gecko/20100101 Firefox/67.0"
PATH="/home/SYSTEM/bin:/bin:/cygdrive/c/progra~2/php:/cygdrive/c/windows/system32:..."
PATHEXT=".COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC"
PATH_INFO="/foo/bar"
PATH_TRANSLATED="C:\Program Files (x86)\Apache Software Foundation\Apache2.4\htdocs\foo\bar"
QUERY_STRING="var1=value1&var2=with%20percent%20encoding"
REMOTE_ADDR="127.0.0.1"
REMOTE_PORT="63555"
REQUEST_METHOD="GET"
REQUEST_URI="/cgi-bin/printenv.pl/foo/bar?var1=value1&var2=with%20percent%20encoding"
SCRIPT_FILENAME="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/cgi-bin/printenv.pl"
SCRIPT_NAME="/cgi-bin/printenv.pl"
SERVER_ADDR="127.0.0.1"
SERVER_ADMIN="(server admin's email address)"
SERVER_NAME="127.0.0.1"
SERVER_PORT="80"
SERVER_PROTOCOL="HTTP/1.1"
SERVER_SIGNATURE=""
SERVER_SOFTWARE="Apache/2.4.39 (Win32) PHP/7.3.7"
SYSTEMROOT="C:\Windows"
TERM="cygwin"
WINDIR="C:\Windows"
```
## استفاده از اسکریپت های CGI
فایل‌های CGI حاوی اسکریپت‌های CGI معمولاً برای پردازش داده‌های ورودی از کاربر و تولید داده‌های خروجی مربوطه استفاده می‌شوند. پیاده سازی ویکی یکی از نمونه های برنامه CGI است. اگر عامل کاربر درخواستی برای نام ورودی ارسال کند، وب سرور برنامه CGI را اجرا می کند. برنامه CGI منبع صفحه ورودی را دریافت می کند، آن را به HTML تبدیل می کند و نتیجه را چاپ می کند. وب سرور خروجی برنامه CGI را دریافت کرده و آن را به کاربر کاربر باز می گرداند. سپس، اگر عامل کاربر با کلیک کردن روی دکمه ویرایش صفحه تابع ویرایش را فراخوانی کند، برنامه CGI یک ناحیه متنی HTML یا سایر کنترل های ویرایش را با محتویات صفحه نشان می دهد. در نهایت، اگر عامل کاربر روی دکمه انتشار صفحه کلیک کند، برنامه CGI HTML به روز شده را به منبع صفحه آن ورودی تبدیل کرده و آن را ذخیره می کند.



## منابع 

* [رابط دروازه مشترک - توسط Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)


