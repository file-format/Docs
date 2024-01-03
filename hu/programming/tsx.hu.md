{
  "date" : "2023-12-28",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "TSX File - React TypeScript File - Mi az .tsx fájl és hogyan nyitható meg?",
  "description":"Ismerje meg a TSX React TypeScript fájlt és annak megnyitását.",
  "linktitle" : "TSX",
  "menu" : {
    "docs" : {
      "identifier": "programming-hu-tsx",
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-12-28"
}

## Mi az a TSX fájl?

A „.tsx” fájlkiterjesztés általában olyan TypeScript fájlokhoz kapcsolódik, amelyek **React** kódot tartalmaznak. A **TypeScript a JavaScript szuperkészlete**, amely statikus gépelést ad a nyelvhez, a **React pedig egy JavaScript-könyvtár a felhasználói felületek létrehozásához**. Amikor együtt dolgoznak a React és a TypeScript használatával, a fejlesztők gyakran a „.tsx” kiterjesztést használják fájljaikhoz annak jelzésére, hogy a fájlok tartalmazzák a TypeScriptet és a JSX-et is (a React JavaScript szintaktikai kiterjesztése).

## TSX fájl példa

A TypeScript lehetővé teszi a változók, függvényparaméterek és egyebek típusainak meghatározását. Gyakran látni TypeScript-kódot egy „.tsx” fájlban, amely meghatározza a React összetevőiben használt kellékek, állapotok és egyéb változók típusát.

```
// Példa: TypeScript kód egy React komponensben
interfész MyComponentProps {
   név: string;
   életkor: szám;
}
const MyComponent: React.FC<MyComponentProps> = ({ név, életkor }) => {
   // Itt a komponens logika
   return <div>{name} {age} éves.</div>;
};
```

## JSX (React Syntax Extension)

A JSX a React által ajánlott szintaxis-kiterjesztés a JavaScripthez. Az XML/HTML-hez hasonlít, és a felhasználói felület leírására szolgál.

```
// Példa: JSX egy React komponensben
const MyComponent: React.FC<MyComponentProps> = ({ név, életkor }) => {
   return <div>{name} {age} éves.</div>;
};
```

A „.tsx” fájl jellemzően tartalmazza a React összetevő definícióját funkcionális összetevők vagy osztályösszetevők használatával.

```
// Példa: A komponens definíciójának reagálása ".tsx" fájlban
const MyComponent: React.FC = () => {
   return <div>Helló, reagálj!</div>;
};
```

A fájl elején gyakran látni importálási utasításokat, amelyek behozzák a szükséges függőségeket és modulokat.

```
// Példa: Importál utasításokat ".tsx" fájlba
import React from 'react';
```

## TSX fájl megnyitása

A TSX fájlok egyszerű szöveges fájlok, így bármelyik szövegszerkesztőben megnyithatja őket, pl. Jegyzettömb. Ezek azonban kódolási fájlok, és az IDE általi megnyitásra szánták pl. Visual Studio kód.