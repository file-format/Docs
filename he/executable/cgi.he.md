{
  "date" : "2021-06-28",
  "keywords" :[ "קובץ cgi", "מהו קובץ cgi", "קובץ", "דוגמה ל-cgi", "סיומת קובץ cgi","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ CGI וממשקי API שיכולים ליצור ולפתוח קובצי CGI.",
  "title" :"CGI - Common Gateway Interface Script File",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## מהו קובץ CGI?
קובץ CGI ידוע כסקריפט Common Gateway Interface המשמש שרת אינטרנט להפעלת תוכנית חיצונית לעיבוד בקשות משתמשים. הסקריפט שנשמר בקובץ עם סיומת .cgi נכתב בדרך כלל בשפות תכנות C או Perl. זה הוצג עוד מהימים הראשונים של האינטרנט, כאשר מפתחי אינטרנט רצו לחבר מסדי נתונים לשרתי האינטרנט שלהם. שרת שתמך בשער משותף בין שרת אינטרנט ומסדי נתונים היה מתאים לביצוע קוד CGI.

## פורמט קובץ CGI
סקריפטים של CGI משמשים את שרת האינטרנט כדי להקל על הבעלים להגדיר את אופן הטיפול בכתובת URL. ההליך נעשה בדרך כלל על ידי סימון ספרייה חדשה (בה נמצאים המסמכים בעיקר) כמכילה סקריפטים של CGI; שמו הנפוץ הוא cgi-bin. לדוגמה, /usr/local/apache/htdocs/cgi-bin יכול להיבחר כספריית CGI בשרת האינטרנט. כאשר דפדפן אינטרנט מבקש כתובת URL שמפנה לקובץ בתוך ספריית CGI, אז, במקום פשוט לשלוח את הקובץ הזה (/he/usr/local/apache/htdocs/cgi-bin/printenv.pl) לדפדפן האינטרנט, ה-HTTP שרת מבצע את הסקריפט שצוין ומחזיר את הפלט של הסקריפט לדפדפן האינטרנט. בקיצור, כל מה שסקריפט ה-CGI נשלח לפלט סטנדרטי מועבר ללקוח האינטרנט במקום להיות מוצג במסוף של חלון.

### דוגמה ל-CGI

בעקבות סקריפט CGI שנכתב ב-Perl המציג את כל משתני הסביבה המועברים על ידי שרת האינטרנט:
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

הפלט יהיה כמו הבא:
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
## שימושים בסקריפטים של CGI
קבצי ה-CGI המכילים את סקריפטי ה-CGI משמשים בדרך כלל לעיבוד נתוני קלט מהמשתמש ולייצר את נתוני הפלט הרלוונטיים. הטמעת ויקי היא אחת הדוגמאות לתוכנית CGI. אם סוכן המשתמש שולח בקשה לשם של ערך, שרת האינטרנט מפעיל את תוכנית CGI. תוכנית CGI מקבלת את המקור של הדף של אותו ערך, ממירה אותו ל-HTML ומדפיסה את התוצאה. שרת האינטרנט מקבל את הפלט מתוכנת CGI ומחזיר אותו לסוכן המשתמש. לאחר מכן, אם סוכן המשתמש קורא לפונקציית העריכה על ידי לחיצה על כפתור "ערוך עמוד", תוכנית CGI מציגה אזור טקסט HTML או פקד עריכה אחר עם תוכן העמוד. לבסוף, אם סוכן המשתמש לוחץ על כפתור "פרסם עמוד", תוכנית CGI ממירה את ה-HTML המעודכן למקור של עמוד הערך הזה ותשמור אותו.



## הפניות

* [ממשק שער משותף - מאת Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

