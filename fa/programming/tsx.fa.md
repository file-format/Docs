{
  "date" : "2023-12-28",
  "author" : {
    "display_name" : "Shakeel Faiz"
}،
  "draft" : "false",
  "toc" : true,
  "title" : "فایل TSX - فایل React TypeScript - فایل .tsx چیست و چگونه آن را باز کنیم؟",
  "description":"با فایل TSX React TypeScript و نحوه باز کردن آن آشنا شوید.",
  "linktitle" : "TSX",
  "menu" : {
    "docs" : {
      "identifier": "programming-tsx-fa",
      "parent" : "programming"
}
}،
  "lastmod" : "2023-12-28"
}

## فایل TSX چیست؟

فایل TSX معمولاً با فایل‌های TypeScript که حاوی کد **React** هستند مرتبط است. **TypeScript ابرمجموعه ای از جاوا اسکریپت** است که تایپ استاتیک را به زبان اضافه می کند و **React یک کتابخانه جاوا اسکریپت برای ساخت رابط های کاربری است**. هنگام کار با React و TypeScript، توسعه دهندگان اغلب از پسوند .tsx برای فایل های خود استفاده می کنند تا نشان دهند که آنها حاوی TypeScript و JSX (پسوند نحوی React برای جاوا اسکریپت) هستند.

## نمونه فایل TSX

TypeScript به شما این امکان را می دهد که انواع متغیرها، پارامترهای تابع و موارد دیگر را تعریف کنید. شما اغلب کد TypeScript را در یک فایل .tsx می بینید که انواع props، state و سایر متغیرهای مورد استفاده در اجزای React را مشخص می کند.

```
// Example: TypeScript code in a React component
interface MyComponentProps {
  name: string;
  age: number;
}

const MyComponent: React.FC<MyComponentProps> = ({ name, age }) => {
  // Component logic here
  return <div>{name} is {age} years old.</div>;
};

```

## JSX (برنامه افزودنی React Syntax)

JSX یک پسوند نحوی برای جاوا اسکریپت است که توسط React توصیه شده است. به نظر می رسد شبیه به XML/HTML است و برای توصیف ظاهر رابط کاربری استفاده می شود.

```
// Example: JSX in a React component
const MyComponent: React.FC<MyComponentProps> = ({ name, age }) => {
  return <div>{name} is {age} years old.</div>;
};
```

فایل .tsx معمولاً حاوی تعریف یک مؤلفه React با استفاده از مؤلفه های تابعی یا مؤلفه های کلاس است.

```
// Example: React component definition in a ".tsx" file
const MyComponent: React.FC = () => {
  return <div>Hello, React!</div>;
};
```

اغلب در ابتدای فایل، دستورهای import را مشاهده می‌کنید که وابستگی‌ها و ماژول‌های لازم را وارد می‌کنند.

```
// Example: Import statements in a ".tsx" file
import React from 'react';
```

## چگونه یک فایل TSX را باز کنیم؟

فایل‌های TSX فایل‌های متنی ساده هستند، بنابراین می‌توانید آنها را در هر ویرایشگر متنی مانند Notepad باز کنید. با این حال، این فایل‌های کدنویسی هستند و باید توسط IDE باز شوند، مثلا کد ویژوال استودیو.

