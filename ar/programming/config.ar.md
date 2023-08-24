{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - ملف التكوين" ,
  "description":"تعرف على تنسيق ملف CONFIG باستخدام مثال CONFIG وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات CONFIG وفتحها." ,
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2021-04-23"
}

## ما هو ملف CONFIG؟
يُعرف ملف CONFIG باسم ملف التكوين ؛ تستخدم لتكوين المعلمات والإعدادات الأساسية للعديد من برامج الكمبيوتر. تقرأ بعض البرامج فقط ** ملفات التكوين ** الخاصة بها عند بدء التشغيل. يقوم الآخرون بفحص ملفات التكوين بحثًا عن التغييرات بشكل دوري.

## تنسيق ملف CONFIG
يُستخدم ** تنسيق ملف CONFIG ** لعمليات الخادم وتطبيقات البرامج وإعدادات نظام التشغيل. يمكن للمبرمج كتابة رمز لإرشاد البرنامج لقراءة ملفات التكوين مرارًا وتكرارًا بعد فترة زمنية معينة وتطبيق التغييرات على العملية الحالية. لا توجد معايير محددة أو اصطلاحات قوية لـ CONFIG file sysntax. على سبيل المثال ، ينتمي ملف Web.config الخاص بـ Microsoft إلى تنسيق ملف CONFIG ، والذي يتكون من مجموعات علامات تستند إلى [XML](/web/xml/) ؛ يمكن تحريره باستخدام Microsoft Visual Studio أو أي محرر نصوص آخر.

## أمثلة على ملفات التكوين:
نظرًا لأن ملفات التكوين لا يتم إنشاؤها باتباع أي قواعد أو قواعد أو اصطلاحات ، فقد تكون هذه الملفات مكتوبة باستخدام تنسيقات مختلفة. قد يعتمد ملف .config على XML ، [JSON](/web/json/) أو أي تنسيق آخر. فيما يلي أمثلة لملفات التكوين لأنظمة التشغيل والبرامج المعروفة:

### ملفات التكوين في Linux
كل برنامج Linux هو ملف قابل للتنفيذ يحتفظ بقائمة ** رموز التشغيل ** التي تنفذها وحدة المعالجة المركزية لإنجاز العمليات النموذجية. يمكن تخصيص عمليات كل برنامج تقريبًا وفقًا لمتطلباتك عن طريق تغيير ملفات التكوين الخاصة به. توجد العديد من ملفات التكوين في نظام Linux في الدليل / etc. يمكن تصنيف ملفات التكوين إلى الفئات التالية:
| الفئة | مثال | التعليقات |
---|---|---|
| الوصول إلى الملفات | /etc/host.conf | يخبر خادم مجال الشبكة بكيفية البحث عن أسماء المضيفين.
| التمهيد وتسجيل الدخول / تسجيل الخروج | /etc/rc.d/rc.local | غير رسمي. قد يتم استدعاؤها من rc أو rc.sysinit أو / etc / inittab. |
| نظام الملفات | /etc/mtools.conf | تكوين لكافة العمليات (mkdir ، نسخ ، تنسيق ، إلخ) على نظام ملفات من نوع DOS.
| إدارة النظام | / etc / shells | يحتفظ بقائمة "القذائف" المتاحة للنظام. |
| الشبكات | /etc/gated.conf | التكوين لبوابات. يستخدم فقط من قبل البرنامج الخفي ذي البوابات. |
| أوامر النظام | /etc/logrotate.conf | تكوين الرابط الديناميكي. |
| Daemons | /etc/httpd.conf | ملف التكوين لخادم الويب Apache. هذا الملف ليس عادةً في / etc. |
| برامج المستخدم | /etc/lynx.cfg | إعدادات الوكيل |
### مثال على ملف AWS CONFIG
يمكن حفظ إعدادات التكوين وبيانات الاعتماد المستخدمة بشكل متكرر في ملفات CONFIG التي يتم صيانتها بواسطة AWS CLI. يجب أن يكون ملف CONFIG ملف نص عادي يستخدم التنسيق التالي:
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
### مثال ملف SSH CONFIG
يُطلق على ملف التكوين من جانب العميل OpenSSH اسم CONFIG ، ويتم تخزينه في دليل .ssh. يتكون ملف SSH CONFIG من البنية التالية:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### مثال ملف Python CONFIG
يمكن أن يبدو ملف Python CONFIG بالشكل التالي:

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



## مراجع

* [فهم ملفات تكوين Linux](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [إعدادات ملف التكوين والاعتماد](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [ملفات التكوين في Python](https://martin-thoma.com/configuration-files-in-python/)

