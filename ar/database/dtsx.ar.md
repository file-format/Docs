{
  "date" : "2020-11-11",
  "keywords" :["DTSX" , "امتداد" , "ملف" , "تنسيق الملف" , "نوع ملف قاعدة البيانات" , "تنسيق ملف قاعدة البيانات" , "ملفات قاعدة البيانات"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description" :"تعرف على تنسيق ملف DTSX وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات DTSX وفتحها." ,
  "title" :"تنسيق ملف DTSX - ملف إعدادات SQL Server DTS" ,
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
} ,
  "lastmod" : "2020-08-12"
}

## ما هو ملف DTSX؟

الملف بامتداد dtsx (حزمة خدمات تحويل البيانات XML) هو ملف خدمات تحويل البيانات (DTS) الذي يستخدمه Microsoft SQL للإشارة إلى قواعد / خطوات ترحيل البيانات لنقل البيانات من قاعدة بيانات إلى أخرى. يتضمن ذلك عمليات التحويل وأي خطوات معالجة اختيارية قد تكون مطلوبة أثناء نقل البيانات بين نقطتي الإنشاء والوجهة. خدمات تكامل خادم SQL (SSIS) ، أحد مكونات Microsoft SQL Server ، تستخدم ملفات DTSX لتحديد خطوات معالجة البيانات بين خوادم قاعدة البيانات. يمكن فتح ملفات DTSX باستخدام Microsoft SQL Server 2019.

## تنسيق ملف DTSX

يتطلب نقل البيانات بين خوادم قاعدة البيانات قواعد وخطوات معالجة لضمان سلامة البيانات أثناء هذه العملية. يضمن SSIS أن جميع هذه الأنشطة ، لنقل البيانات ومطابقتها من مصادر مختلفة في المؤسسة ، تتم بشكل ملائم. هذا هو المكان الذي يأتي فيه DTSX الذي يحدد الهياكل التي سيتم استخدامها بواسطة SSIS لتحديد الخطوات حيث يمكن معالجة البيانات كما يلي من خلال هذه الخطوات.

تدفق البيانات الموصوف بواسطة DTSX كما هو موضح في الصورة التالية.

{{< figure src="../DataFlowDTSX.png" alt="تدفق البيانات DTSX" >}}

DTSX مستند إلى [XML](/ar/web/xml/) - وموثق في [MS-DTSX](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd). إعادة هيكلة DTSX XML المحسّنة هي DTSX 2.0 التي تتضمن سمات جديدة للهياكل ، واستبدال الخصائص المسماة كسمات XML الأصل ، وتحديد الإعدادات الافتراضية لمعظم قيم السمات ، ووضع العناصر المكررة داخل العنصر الأصل. يتم وصف هياكل DTSX باستخدام [مخططات XML](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc#Appendix_A_1) والتنسيق الهيكلي هو XML للنص celar.

## مراجع

* [تنسيق DTSX - Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [تنسيق DTSX 2 - بواسطة Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

