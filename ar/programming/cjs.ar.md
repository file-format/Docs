{
  "date" : "2023-10-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ไฟล์ CJS - ไฟล์รหัส CommonJS",
  "description":"ไฟล์ .cjs คืออะไร และจะเปิดได้อย่างไร",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-29"
}


## ما هو ملف CJS؟
ملف CommonJS (CJS) هو ملف يحتوي على تعليمات برمجية JavaScript مكتوبة في بناء جملة CommonJS. CommonJS هو نظام وحدات مصمم للعمل في بيئات خارج متصفحات الويب الأمامية، وغالبًا ما يستخدم في بيئات JavaScript من جانب الخادم، مثل Node.js.

## تنسيق ملف CJS - مزيد من المعلومات
تتم كتابة ملفات CJS بلغة CommonJS ويمكن تحريرها في أي محرر نصوص مثل Microsoft Notepad أو Apple TextEdit. عادةً ما يتم تخزين وحدات CommonJS في ملفات منفصلة وتهدف إلى تغليف التعليمات البرمجية وتعديلها لتحسين التنظيم وقابلية الصيانة. تستخدم هذه الوحدات الدالة المطلوبة لاستيراد التبعيات والكائن Module.exports أو الصادرات لكشف القيم والوظائف التي يمكن استخدامها بواسطة أجزاء أخرى من التعليمات البرمجية.

## مثال على كود CJS
تحتوي وحدات CommonJS على بناء جملة وبنية محددة تتضمن ميزات مثل الوظيفة المطلوبة لاستيراد وحدات أخرى وmodule.exports أو تصدير الكائنات لتصدير القيم أو الوظائف أو الكائنات من وحدة نمطية. تُستخدم هذه الوحدات لتغليف وفصل أجزاء من التعليمات البرمجية، مما يسهل إدارة وصيانة قواعد تعليمات JavaScript الكبيرة. فيما يلي مثال أساسي لوحدة CommonJS:

```
// Module definition in a file named "myModule.js"
const someValue = 42;

function add(a, b) {
  return a + b;
}

module.exports = {
  someValue,
  add,
};

// Using the module in another file
const myModule = require('./myModule');
console.log(myModule.someValue); // 42
console.log(myModule.add(10, 20)); // 30
```

## مراجع

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)
