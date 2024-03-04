{
  "date" : "2023-12-28",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TSX File - React TypeScript File - Kas yra .tsx failas ir kaip jį atidaryti?",
  "description":"Sužinokite apie TSX React TypeScript failą ir kaip jį atidaryti.",
  "linktitle" : "TSX",
  "menu" : {
    "docs" : {
      "identifier": "programming-tsx-lt",
      "parent" : "programming"
}
},
  "lastmod" : "2023-12-28"
}

## Kas yra TSX failas?

TSX failas dažniausiai siejamas su TypeScript failais, kuriuose yra **React** kodas. **TypeScript yra JavaScript** superrinkinys, kuris prideda prie kalbos statinį rašymą, o **React yra JavaScript biblioteka, skirta kurti vartotojo sąsajas**. Dirbdami kartu su React ir TypeScript, kūrėjai savo failams dažnai naudoja plėtinį .tsx, kad nurodytų, jog juose yra ir TypeScript, ir JSX (React sintaksės plėtinys, skirtas JavaScript).

## TSX failo pavyzdys

TypeScript leidžia apibrėžti kintamųjų, funkcijų parametrų ir kt. tipus. .tsx faile dažnai matysite TypeScript kodą, nurodantį React komponentuose naudojamų rekvizitų, būsenų ir kitų kintamųjų tipus.

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

## JSX (React Sintaksės plėtinys)

JSX yra React rekomenduojamas JavaScript sintaksės plėtinys. Jis atrodo panašus į XML / HTML ir yra naudojamas apibūdinti, kaip turėtų atrodyti vartotojo sąsaja.

```
// Example: JSX in a React component
const MyComponent: React.FC<MyComponentProps> = ({ name, age }) => {
  return <div>{name} is {age} years old.</div>;
};
```

.tsx faile paprastai yra React komponento apibrėžimas, naudojant funkcinius komponentus arba klasės komponentus.

```
// Example: React component definition in a ".tsx" file
const MyComponent: React.FC = () => {
  return <div>Hello, React!</div>;
};
```

Failo pradžioje dažnai matysite importavimo teiginius, kuriuose pateikiamos būtinos priklausomybės ir moduliai.

```
// Example: Import statements in a ".tsx" file
import React from 'react';
```

## Kaip atidaryti TSX failą?

TSX failai yra paprasto teksto failai, todėl galite juos atidaryti bet kuriame teksto rengyklėje, pvz., Notepad. Tačiau tai yra kodavimo failai ir skirti atidaryti IDE, pvz., Visual Studio Code.

