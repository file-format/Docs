{
  "date" : "2021-08-02",
  "keywords" :["reg file", "reg file format", "what is a reg file", "file", "reg example", "reg file extension", "extension", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف REG وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات REG وفتحها." ,
  "title" :"REG - ملف تسجيل Windows" ,
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
} ,
  "lastmod" : "2021-08-02"
}

## ما هو ملف REG؟
ملف REG هو ببساطة ملف نصي بامتداد .reg. يتم إنشاء هذه الملفات عادةً عن طريق تصدير مفاتيح نموذجية من السجل. يمكن أيضًا استخدام هذه الملفات كنسخة احتياطية من السجل (هذه الخطوة مهمة بشكل خاص قبل إجراء التغييرات!). يمكنك أن ترى أن بعضها جعلها متاحة كملفات قابلة للتنزيل على نفس المواقع التي توضح لك كيفية تنفيذ اختراق السجل. يعد ملف REG مفيدًا في إجراء تغييرات يدوية على السجل وتصدير هذه التغييرات. ما عليك سوى تنظيف الملف قليلاً ثم مشاركته مع الآخرين.

## تنسيق ملف REG
تم تصميم تنسيق ملف REG لتصدير واستيراد أجزاء من سجل Windows باستخدام بناء جملة يستند إلى INI. سجل Windows هو قاعدة بيانات علائقية أو هرمية تحافظ على إعدادات المستوى المنخفض لنظام التشغيل Microsoft Windows والتطبيقات الأخرى التي تستخدم سجل Windows. البديل ، يمكننا القول ، يتكون السجل أو سجل Windows من معلومات وخيارات وإعدادات وقيم أخرى للبرامج والأجهزة المثبتة على جميع إصدارات أنظمة تشغيل Microsoft Windows.
### صيغة ملف REG
فيما يلي بعض العناصر الأساسية كجزء من بناء جملة ملف REG:
- ** RegistryEditorVersion **: على سبيل المثال "محرر تسجيل Windows الإصدار 5.00" لأنظمة التشغيل Windows 2000 و Windows XP و Windows Server 2003.
- ** سطر فارغ **: يحدد بداية مسار تسجيل جديد.
- ** RegistryPathx **: مسار المفتاح الفرعي الذي يحمل القيمة الأولى التي تقوم باستيرادها.
- ** DataItemNamex **: اسم عنصر البيانات الذي تريد استيراده.
- ** DataTypex **: نوع البيانات لقيمة التسجيل.

يتم تخزين المفاتيح في ملفات .reg باستخدام البنية التالية:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
يمكنك تعديل القيمة الافتراضية لمفتاح باستخدام "@" بدلاً من "اسم القيمة":
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### مثال
هنا مثال على ملف REG
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## مراجع

* [سجل Windows- بواسطة Wikipedia] (https://en.wikipedia.org/wiki/Windows_Registry)
* [كيفية إضافة أو تعديل أو حذف مفاتيح التسجيل الفرعية والقيم باستخدام ملف .reg] (https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete- مفاتيح التسجيل الفرعية والقيم باستخدام a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)


