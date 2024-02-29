{
  "date": "2023-10-26",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فایل CJS - فایل کد CommonJS",
  "description": "فایل cjs چیست و چگونه آن را باز کنیم؟",
  "linktitle": "CJS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cj-fas"
}
},
  "lastmod": "2023-10-26"
}

## فایل CJS چیست؟

یک فایل CommonJS (CJS) فایلی است که حاوی کد جاوا اسکریپت نوشته شده در دستور CommonJS است. CommonJS یک سیستم ماژول است که برای کار در محیط‌هایی فراتر از مرورگرهای وب frontend طراحی شده است و اغلب در محیط‌های جاوا اسکریپت سمت سرور مانند Node.js استفاده می‌شود.

## فرمت فایل CJS - اطلاعات بیشتر

فایل‌های CJS با نحو CommonJS نوشته می‌شوند و می‌توانند در هر ویرایشگر متنی مانند Microsoft Notepad یا Apple TextEdit ویرایش شوند. ماژول‌های CommonJS معمولاً در فایل‌های جداگانه ذخیره می‌شوند و برای کپسوله‌سازی و مدولار کردن کد برای سازماندهی و نگهداری بهتر در نظر گرفته شده‌اند. این ماژول‌ها از تابع require برای وارد کردن وابستگی‌ها استفاده می‌کنند و module.exports یا exports در معرض نمایش مقادیر و توابعی هستند که می‌توانند توسط بخش‌های دیگر کد استفاده شوند.

### مثال کد CJS

ماژول های CommonJS دارای یک نحو و ساختار خاص هستند که شامل ویژگی هایی مانند تابع نیاز برای وارد کردن ماژول های دیگر و module.exports یا صادرات اشیاء برای صادرات مقادیر، توابع یا اشیاء از یک ماژول است. این ماژول‌ها برای کپسوله‌سازی و جداسازی قطعات کد استفاده می‌شوند و مدیریت و نگهداری پایگاه‌های کد بزرگ جاوا اسکریپت را آسان‌تر می‌کنند. در اینجا یک مثال اساسی از یک ماژول CommonJS آورده شده است:

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

## منابع

* [کلاس های طراحی در ویژوال استودیو] (https://en.wikipedia.org/wiki/CommonJS)


