{
  "date": "2023-06-12",
  "keywords": [
    "bak",
    "bak file",
    "Microsoft SQL Server Database Backup",
    "what is a bak file",
    "how to open bak file",
    "file",
    "bak file extension",
    "extension"
  ],
  "author": {
    "display_name": "Shakeel Faiz"
  },
  "draft": "false",
  "toc": true,
  "title": "BAK File Format - Microsoft SQL Server Database Backup",
  "description": "تعرف على تنسيق BAK SQL Server Backup وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات BAK وفتحها.",
  "linktitle": "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver",
      "parent": "database"
    }
  },
  "lastmod": "2023-06-12"
}

## ما هو ملف BAK؟

يعد الملف ".bak"، في سياق Microsoft SQL Server، بمثابة تنسيق ملف نسخ احتياطي يُستخدم لتخزين نسخ من قاعدة بيانات SQL Server. تحتوي هذه الملفات على لقطة من قاعدة البيانات في وقت محدد، بما في ذلك المخطط والبيانات والمعلومات الأخرى ذات الصلة. يتم إنشاؤها باستخدام وظيفة النسخ الاحتياطي والاستعادة المضمنة في SQL Server وتخدم العديد من الأغراض المهمة:

1. **استرداد البيانات:** توفر ملفات .bak وسيلة لاستعادة قاعدة البيانات في حالة فقدان البيانات أو تلفها أو مشكلات أخرى. من خلال استعادة قاعدة بيانات من ملف .bak، يمكنك إعادتها إلى حالتها السابقة، مما يقلل وقت التوقف عن العمل وفقدان البيانات.

2. **الترحيل والاستنساخ:** غالبًا ما تُستخدم ملفات النسخ الاحتياطي لترحيل قواعد البيانات بين الخوادم أو إنشاء نسخ من قواعد البيانات لأغراض الاختبار أو التطوير أو إعداد التقارير. أنها توفر طريقة متسقة وفعالة لنقل قواعد البيانات بين البيئات.

3. **الاسترداد في الوقت المناسب:** يسمح لك SQL Server بإجراء الاسترداد في الوقت المناسب باستخدام ملفات .bak. وهذا يعني أنه يمكنك استعادة قاعدة بيانات إلى لحظة زمنية محددة، وهو ما قد يكون حاسمًا للامتثال التنظيمي أو تدقيق البيانات.

4. **التعافي من الكوارث:** تعد ملفات .bak جزءًا مهمًا من التخطيط للتعافي من الكوارث. فهي تضمن أن بياناتك آمنة ويمكن استعادتها بسرعة في حالة فشل الأجهزة أو الكوارث الطبيعية أو غيرها من الأحداث الكارثية.

## قم بإنشاء ملف .BAK في SQL Server

لإنشاء ملف .bak في SQL Server، عادةً ما تستخدم أوامر SQL Server Management Studio (SSMS) أو Transact-SQL (T-SQL) مثل BACKUP DATABASE أو BACKUP LOG. فيما يلي مثال مبسط لكيفية إنشاء نسخة احتياطية لقاعدة البيانات باستخدام T-SQL:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## استعادة ملف .BAK في SQL Server

لاستعادة قاعدة بيانات من ملف .bak، يمكنك استخدام أمر RESTORE DATABASE:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## كيفية فتح ملف BAK في SQL Server؟

لفتح البيانات المخزنة في ملف ".bak" والوصول إليها، تحتاج عادةً إلى استعادتها إلى مثيل Microsoft SQL Server. فيما يلي الخطوات العامة لفتح ملف ".bak" باستخدام SQL Server Management Studio (SSMS):

1. ** إطلاق SQL Server Management Studio **: افتح SSMS على جهاز الكمبيوتر الخاص بك. يمكنك عادةً العثور عليه في قائمة ابدأ أو من خلال البحث عن "SQL Server Management Studio".

2. **الاتصال بمثيل SQL Server**: في SSMS، اتصل بمثيل SQL Server حيث تريد استعادة قاعدة البيانات. ستحتاج إلى الأذونات اللازمة لتنفيذ هذه العملية.

3. **استعادة قاعدة البيانات**:

    أ. في جزء مستكشف الكائنات الموجود على الجانب الأيسر، قم بتوسيع مثيل SQL Server.

    ب. قم بتوسيع عقدة "قواعد البيانات".

    ج. انقر بزر الماوس الأيمن على "قواعد البيانات" وحدد "استعادة قاعدة البيانات".

4. **حدد المصدر والوجهة**:

    أ. في الصفحة "عام" من مربع الحوار "استعادة قاعدة البيانات"، أدخل اسمًا لقاعدة البيانات الجديدة في الحقل "إلى قاعدة البيانات". سيكون هذا هو اسم قاعدة البيانات المستعادة.

    ب. في قسم "المصدر"، اختر "الجهاز" كنوع وسائط النسخ الاحتياطي.

    ج. انقر فوق الزر "..." بجوار حقل "الجهاز" لتصفح ملف ".bak" الذي تريد استعادته.

    د. حدد ملف ".bak" الذي ترغب في فتحه وانقر فوق "موافق".

5. **خيارات الاستعادة**: قم بمراجعة خيارات الاستعادة وتكوينها حسب الحاجة. يمكنك تحديد ما إذا كنت تريد الكتابة فوق قاعدة بيانات موجودة أم لا، وتعيين خيارات الاسترداد، والمزيد. تأكد من ضبط هذه الخيارات وفقًا لمتطلباتك.

6. **بدء الاستعادة**: بمجرد تكوين خيارات الاستعادة، انقر فوق الزر "موافق" في مربع الحوار "استعادة قاعدة البيانات". سيبدأ SQL Server عملية الاستعادة.

7. **الوصول إلى قاعدة البيانات المستعادة**: بعد نجاح الاستعادة، يمكنك الوصول إلى قاعدة البيانات المستعادة في SQL Server Management Studio تمامًا مثل أي قاعدة بيانات أخرى. يمكنك تشغيل الاستعلامات وعرض الجداول والعمل مع البيانات الموجودة في قاعدة البيانات.

## ملفات باك أخرى

فيما يلي أنواع الملفات الأخرى التي تستخدم امتداد الملف **.bak**.

**Database**
- [BAK - Database Backup File](/database/bak/)
- [BAK - Swiftpage Act! Database Backup](/database/bak-act/)

**Game**
- [BAK - Terraria World or Player Backup](/game/bak-terraria/)

**Misc**
- [BAK - Backup File](/misc/bak-backup/)
- [BAK - Chromium Bookmarks Backup](/misc/bak-chromium/)
- [BAK - Finale 2012 Score Backup](/misc/bak-finale/)
- [BAK - MobileTrans Backup](/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Backup](/misc/bak-vegas/)

**Settings**
- [BAK - Holo Launcher Backup](/settings/bak-holo/)

## مراجع
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)