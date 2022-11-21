{
  "date" : "2021-06-28",
  "keywords" :["ملف cgi" , "ما هو ملف cgi" , "ملف" , "مثال cgi" , "امتداد ملف cgi" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Muhammad Umar"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف CGI وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات CGI وفتحها." ,
  "title" :"CGI - ملف البرنامج النصي لواجهة البوابة العامة" ,
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
} ,
  "lastmod" : "2021-06-28"
}

## ما هو ملف CGI؟
يُعرف ملف CGI باسم البرنامج النصي Common Gateway Interface الذي يستخدمه خادم الويب لتشغيل برنامج خارجي لمعالجة طلبات المستخدم. النص الذي يتم حفظه في ملف بامتداد .cgi عادة ما يكتب بلغات البرمجة C أو Perl. تم تقديم هذا منذ الأيام الأولى للويب ، عندما أراد مطورو الويب ربط قواعد البيانات بخوادم الويب الخاصة بهم. كان الخادم الذي يدعم بوابة مشتركة بين خادم الويب وقواعد البيانات مناسبًا تمامًا لتنفيذ كود CGI.

## تنسيق ملف CGI
يتم استخدام البرامج النصية CGI بواسطة خادم الويب لتسهيل قيام المالك بتكوين كيفية معالجة عنوان URL. يتم هذا الإجراء عادةً عن طريق تعليم دليل جديد (حيث توجد المستندات بشكل أساسي) على أنه يحتوي على نصوص CGI ؛ اسمها الشائع هو cgi-bin. على سبيل المثال ، يمكن اختيار / usr / local / apache / htdocs / cgi-bin كدليل CGI على خادم الويب. عندما يطلب مستعرض الويب عنوان URL يشير إلى ملف داخل دليل CGI ، فبدلاً من إرسال هذا الملف ببساطة (/ar/usr/local/apache/htdocs/cgi-bin/printenv.pl) إلى متصفح الويب ، فإن HTTP ينفذ الخادم البرنامج النصي المحدد ويعيد إخراج البرنامج النصي إلى مستعرض الويب. باختصار ، أي شيء يتم إرساله من نص CGI إلى الإخراج القياسي يتم نقله إلى عميل الويب بدلاً من عرضه في نافذة طرفية.

### مثال CGI

اتباع نص CGI المكتوب بلغة Perl والذي يعرض جميع متغيرات البيئة التي يمر بها خادم الويب:
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

سيكون الإخراج كالتالي:
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
## استخدامات نصوص CGI
عادةً ما تُستخدم ملفات CGI التي تحتوي على نصوص CGI لمعالجة بيانات الإدخال من المستخدم وإنتاج بيانات الإخراج ذات الصلة. يعد تطبيق wiki أحد أمثلة برنامج CGI. إذا أرسل وكيل المستخدم طلبًا لاسم الإدخال ، يقوم خادم الويب بتشغيل برنامج CGI. يحصل برنامج CGI على مصدر صفحة الإدخال ، ويحولها إلى HTML ، ويطبع النتيجة. يتلقى خادم الويب الإخراج من برنامج CGI وإعادته إلى وكيل المستخدم. بعد ذلك ، إذا قام وكيل المستخدم باستدعاء وظيفة التحرير بالنقر فوق الزر "تحرير الصفحة" ، فإن برنامج CGI يعرض منطقة نصية بتنسيق HTML أو عنصر تحكم آخر في التحرير بمحتويات الصفحة. أخيرًا ، إذا نقر وكيل المستخدم على زر "نشر الصفحة" ، فإن برنامج CGI يحول HTML المحدث إلى مصدر صفحة ذلك الإدخال ويحفظه.



## مراجع

* [واجهة البوابة العامة - بواسطة Wikipewdia] (https://en.wikipedia.org/wiki/Common_Gateway_Interface)

