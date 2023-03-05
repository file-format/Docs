{
  "date" : "2019-10-11",
  "keywords" :["class", ".class", "what is a class file", "how to open a class file", "extension", "file", "class file", "class file format", ".class extension "," class file in java "],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"Class - Java Class File Format" ,
  "description":"تعرف على تنسيق ملف الفصل وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات الفصل الدراسي وفتحها." ,
  "linktitle" : "Class",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2020-09-10"
}

## ما هو ملف الفصل؟

** ملف الفصل في Java ** هو الناتج المترجم لفئة [.java](/ar/ البرمجة / java /) التي يتم تنفيذها فعليًا بواسطة Java Virtual Machine (JVM). يمكن تنفيذ ملفات الفصل بشكل فردي وكذلك يمكن أن تكون جزءًا من ملف [JAR](/ar/ برمجة / jar /) كحزمة مع ملفات حزم أخرى. يمكن إنشاء هذه باستخدام الأمر ** `javac` ** من واجهة سطر الأوامر. توفر بعض Java IDEs مثل [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) و NetBeans إنشاء ملفات إخراج فئة من المشروع جافا. الملفات.

## تنسيق ملف الفصل الدراسي

يتكون ملف فئة Java من كود بايت وهو كود وسيط ليتم تشغيله بواسطة JVM. يتكون ملف فئة من دفق من 8 بت بايت وعناصر البيانات متعددة البايت يتم تخزينها دائمًا بترتيب كبير.

### الفئة بنية الملف

هيكل ملف الفصل كما هو موضح أدناه.
```
ClassFile {
    u4             magic;
    u2             minor_version;
    u2             major_version;
    u2             constant_pool_count;
    cp_info        constant_pool[constant_pool_count-1];
    u2             access_flags;
    u2             this_class;
    u2             super_class;
    u2             interfaces_count;
    u2             interfaces[interfaces_count];
    u2             fields_count;
    field_info     fields[fields_count];
    u2             methods_count;
    method_info    methods[methods_count];
    u2             attributes_count;
    attribute_info attributes[attributes_count];
}
```
أين:

* u1 = كمية أحادية البايت غير موقعة
* u2 = كمية ثنائية البايت بدون إشارة
* u4 = كمية أربعة بايت بدون إشارة

تم توضيح تفاصيل بنية ملف .class أيضًا في Oracle [تنسيق ملف الفئة](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) ويمكن الرجوع إليها بواسطة مطورين كمرجع. ملخص لهذه الحقول على النحو التالي.

* "السحر" - يوفر العنصر السحري الرقم السحري الذي يحدد تنسيق ملف الفئة ؛ لها قيمة 0xCAFEBABE.
* `Secondary_version`،` major_version` - إن قيم العناصر الثانوية و main_version هي أرقام الإصدارات الثانوية والرئيسية لملف الفئة هذا.
* "Constant_pool_count" - قيمة عنصر Constant_pool_count تساوي عدد الإدخالات في جدول Constant_pool مضافًا إليه واحد. يعتبر فهرس المجموعة الثابتة صالحًا إذا كان أكبر من الصفر وأقل من عدد ثابت ، باستثناء الثوابت من النوع الطويل والمزدوج.
* `Constant_pool []` - الثابت هو جدول الهياكل (§4.4) يمثل ثوابت سلسلة متنوعة ، وأسماء فئة وواجهة ، وأسماء الحقول ، وثوابت أخرى يشار إليها داخل بنية ClassFile وبنيتها الفرعية. تتم الإشارة إلى تنسيق كل إدخال في جدول Constant_pool بواسطة بايت "العلامة" الأول الخاص به.
* `access_flags` - قيمة عنصر access_flags هي قناع من العلامات المستخدمة للإشارة إلى أذونات الوصول إلى وخصائص هذه الفئة أو الواجهة.
* `this_class` - يجب أن تكون قيمة عنصر فئة this_class فهرسًا صالحًا في جدول المجموعة الثابتة.
* `super_class` - بالنسبة للفئة ، يجب أن تكون قيمة عنصر الفئة super_class إما صفرًا أو يجب أن تكون فهرسًا صالحًا في جدول ثابت_جمع.
* "interfaces_count" - تعطي قيمة عنصر عدد الواجهات عدد الواجهات الفائقة المباشرة من هذه الفئة أو نوع الواجهة.
* `واجهات []` - يجب أن تكون كل قيمة في مصفوفة الواجهات فهرسًا صالحًا في جدول المجموعة الثابتة.
* `field_count` - تعطي قيمة عنصر field_count عدد بنيات معلومات_الحقل في جدول الحقول.
* `الحقول []` - يجب أن تكون كل قيمة في جدول الحقول عبارة عن بنية معلومات_حقول تعطي وصفاً كاملاً لحقل في هذه الفئة أو الواجهة.
* `method_count` - تعطي قيمة عنصر method_count عدد بنى معلومات_الطريقة في جدول الأساليب.
* `طرق []` - يجب أن تكون كل قيمة في جدول الأساليب عبارة عن بنية معلومات_مُنهجية تعطي وصفاً كاملاً لطريقة في هذه الفئة أو الواجهة. إذا لم يتم تعيين أي من علامتي ACC_NATIVE و ACC_ABSTRACT في عنصر access_flags الخاص ببنية method_info ، يتم أيضًا توفير إرشادات Java Virtual Machine التي تنفذ الطريقة.
* `attributes_count` - تعطي قيمة عنصر attributes_count عدد السمات (§4.7) في جدول السمات الخاص بهذه الفئة.
* `سمات []` - يجب أن تكون كل قيمة لجدول السمات عبارة عن بنية معلومات_سمات.




## مراجع

* [تنسيق ملف الفصل](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

