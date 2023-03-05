{
  "date" : "2021-07-20",
  "keywords" :["MJS", "File", "Extension", "File Format", "File Extension", "Node.js ES Module File"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"MJS - Node.js ES Module Javascript File" ,
  "description" :"تعرف على ما هو ملف MJS وواجهات برمجة التطبيقات التي يمكنها إنشاء ملف MJS وفتحه." ,
  "linktitle" : "MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2021-07-20"
}

## ما هو ملف MJS؟

الملف ذو الامتداد .mjs هو ملف شفرة مصدر JavaScript يُستخدم كوحدة ECMA Module (ECMAScript Module) في تطبيقات Node.js. نظام الوحدة النمطية natvie الخاص بـ Node.js هو CommonJS الذي يتم استخدامه لتقسيم الشفرة في ملفات مختلفة للحفاظ على تنظيم كود [JS](/ar/ web / js /). MJS هي الطريقة الوحيدة التي يستخدمها Node.js لتحديد ما إذا كانت الوحدة هي CommonJS أو ES6. وحدات ECMAScript هي صيغة قياسية لتعبئة كود JavaScript لإعادة الاستخدام. يمكن فتح ملفات MJS في برامج تحرير النصوص مثل Atom و Vim و Apple xCode و Microsoft Visual Studio و Notepad.

## تنسيق ملف MJS - مزيد من المعلومات

يتم حفظ ملفات MJS على القرص بتنسيق نص عادي في بناء جملة JavaScript. يمكن فتحها في أي محرر نصوص ويمكن قراءتها من قبل الإنسان. منذ عام 2018 ، تدعم جميع المتصفحات الرئيسية تقريبًا وحدات ES.

## الاختلافات بين وحدات ES و CommonJS

إذن ما الذي يجعل ملفات MJS مختلفة عن ملفات JS العادية؟ يمكن تلخيص الفرق بين وحدات ES و CommonJS على النحو التالي:

* لا يتطلب أو تصدير أو تصدير وحدة
* No \ __ filename أو \ __ dirname
* لا يتم تحميل وحدة JSON
* لا يتم تحميل الوحدة الأصلية
* لا يتطلب حل
* لا يوجد NODE_PATH
* لا تتطلب ملحقات
* لا تتطلب ذاكرة التخزين المؤقت

## مراجع

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [الفرق بين JS و MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

