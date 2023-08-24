{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - קובץ תצורה",
  "description":"למד על פורמט קובץ CONFIG עם דוגמה CONFIG וממשקי API שיכולים ליצור ולפתוח קובצי CONFIG.",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## מהו קובץ CONFIG?
קובץ CONFIG ידוע כקובץ תצורה; משמש להגדרת הפרמטרים וההגדרות העיקריות עבור מספר תוכנות מחשב. תוכנות מסוימות קוראים רק את **קובצי התצורה** שלהן בעת ההפעלה. אחרים בודקים מעת לעת שינויים בקבצי התצורה.

## תבנית קובץ CONFIG
**פורמט הקובץ CONFIG** משמש לתהליכי שרת, יישומי תוכנה והגדרות מערכת הפעלה. מתכנת יכול לכתוב קוד כדי להורות לתוכנה לקרוא את קבצי התצורה שוב ושוב לאחר פרק זמן מסוים ולהחיל את השינויים על התהליך הנוכחי. אין סטנדרטים סופיים או מוסכמות חזקות עבור מערכת הקבצים CONFIG. לדוגמה, קובץ Web.config של מיקרוסופט שייך לפורמט הקובץ CONFIG, המורכב מערכי תגים מבוססי [XML](/web/xml/); ניתן לערוך עם Microsoft Visual Studio או כל עורך טקסט אחר.

## דוגמאות לקבצי תצורה:
מכיוון שקובצי התצורה אינם נוצרים על ידי ביצוע כללים, סטנדרטים או מוסכמות, ייתכן שקבצים אלה נכתבו באמצעות פורמטים שונים. קובץ .config עשוי להיות מבוסס על XML, [JSON](/web/json/) או כל פורמט אחר. להלן הדוגמאות לקובצי תצורה עבור מערכות הפעלה ותוכנות ידועות:

### קבצי תצורה בלינוקס
כל תוכנית לינוקס היא קובץ הפעלה ששומר על רשימת **קודי ההפעלה** שה-CPU מבצע כדי לבצע פעולות טיפוסיות. ניתן להתאים את הפעולות של כמעט כל תוכנית לדרישות שלך על ידי שינוי קבצי התצורה שלה. מספר קובצי תצורה במערכת לינוקס נמצאים בספריית /etc. ניתן לסווג את קבצי התצורה לקטגוריות הבאות:
|קטגוריה|דוגמה| הערות|
---|---|---|
|גישה לקבצים|/etc/host.conf|אומר לשרת תחום הרשת כיצד לחפש שמות מארחים.|
|אתחול והתחברות/יציאה|/etc/rc.d/rc.local|לא רשמי. ניתן לקרוא מ-rc, rc.sysinit או /etc/inittab.|
|מערכת קבצים|/etc/mtools.conf|תצורה של כל הפעולות (mkdir, העתקה, פורמט וכו') במערכת קבצים מסוג DOS.|
|ניהול מערכת|/etc/shells|מחזיק את רשימת ה"פגזים" האפשריים הזמינים למערכת.|
|רשתות|/etc/gated.conf|תצורה עבור gated. בשימוש רק על ידי הדמון הסגור.|
|פקודות מערכת|/etc/logrotate.conf|תצורה עבור המקשר הדינמי.|
|Daemons|/etc/httpd.conf|קובץ התצורה של Apache, שרת האינטרנט. קובץ זה בדרך כלל אינו ב-/etc.|
|תוכניות משתמש| /etc/lynx.cfg| הגדרות פרוקסי|
### דוגמה לקובץ AWS CONFIG
ניתן לשמור את הגדרות התצורה והאישורים הנפוצים בקבצי CONFIG שמתוחזקים על ידי AWS CLI. קובץ CONFIG חייב להיות קובץ טקסט רגיל המשתמש בפורמט הבא:
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
### דוגמה לקובץ SSH CONFIG
קובץ התצורה בצד הלקוח של OpenSSH נקרא CONFIG, והוא מאוחסן בספריית .ssh. קובץ SSH CONFIG מורכב מהמבנה הבא:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### דוגמה לקובץ Python CONFIG
קובץ Python CONFIG יכול להיראות כך:

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



## הפניות

* [הבנת קובצי התצורה של לינוקס](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [הגדרות תצורה וקובץ פרטי כניסה](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [קבצי תצורה ב-Python](https://martin-thoma.com/configuration-files-in-python/)

