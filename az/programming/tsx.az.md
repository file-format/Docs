{
  "date" : "2023-12-28",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TSX Faylı - React TypeScript Faylı - .tsx faylı nədir və onu necə açmaq olar?",
  "description":"TSX React TypeScript faylı və onun necə açılacağını öyrənin.",
  "linktitle" : "TSX",
  "menu" : {
    "docs" : {
      "identifier": "programming-tsx-az",
      "parent" : "programming"
}
},
  "lastmod" : "2023-12-28"
}

## TSX faylı nədir?

TSX faylı adətən **React** kodunu ehtiva edən TypeScript faylları ilə əlaqələndirilir. **TypeScript dilə statik yazmağı əlavə edən JavaScript-in super dəstidir** və **React istifadəçi interfeyslərinin qurulması üçün JavaScript kitabxanasıdır**. React və TypeScript ilə birlikdə işləyərkən tərtibatçılar tez-tez faylları üçün .tsx uzantısından istifadə edərək onların həm TypeScript, həm də JSX (JavaScript üçün React sintaksis genişlənməsi) olduğunu göstərirlər.

## TSX fayl nümunəsi

TypeScript sizə dəyişənlər, funksiya parametrləri və s. üçün növləri müəyyən etməyə imkan verir. Siz tez-tez TypeScript kodunu React komponentlərində istifadə olunan rekvizit növlərini, vəziyyəti və digər dəyişənləri göstərən .tsx faylında görəcəksiniz.

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

## JSX (Reaksiya Sintaksis Genişlənməsi)

JSX, React tərəfindən tövsiyə olunan JavaScript üçün sintaksis uzantısıdır. XML/HTML-ə bənzəyir və UI-nin necə görünməli olduğunu təsvir etmək üçün istifadə olunur.

```
// Example: JSX in a React component
const MyComponent: React.FC<MyComponentProps> = ({ name, age }) => {
  return <div>{name} is {age} years old.</div>;
};
```

.tsx faylı adətən funksional komponentlərdən və ya sinif komponentlərindən istifadə edən Reaksiya komponentinin tərifini ehtiva edir.

```
// Example: React component definition in a ".tsx" file
const MyComponent: React.FC = () => {
  return <div>Hello, React!</div>;
};
```

Siz tez-tez faylın əvvəlində zəruri asılılıqları və modulları gətirən idxal bəyanatlarını görəcəksiniz.

```
// Example: Import statements in a ".tsx" file
import React from 'react';
```

## TSX faylını necə açmaq olar?

TSX faylları düz mətn fayllarıdır ki, siz onları istənilən mətn redaktorunda, məsələn, Notepad-da aça bilərsiniz. Bununla belə, bunlar kodlaşdırma fayllarıdır və IDE tərəfindən açılmalıdır, məsələn, Visual Studio Code.

