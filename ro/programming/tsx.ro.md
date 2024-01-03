{
  "date" : "2023-12-28",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "TSX File - React TypeScript File - Ce este fișierul .tsx și cum se deschide?",
  "description":"Aflați despre fișierul TSX React TypeScript și despre cum să îl deschideți.",
  "linktitle" : "TSX",
  "menu" : {
    "docs" : {
      "identifier": "programming-ro-tsx",
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-12-28"
}

## Ce este un fișier TSX?

Extensia de fișier „.tsx” este asociată în mod obișnuit cu fișierele TypeScript care conțin cod **React**. **TypeScript este un superset de JavaScript** care adaugă tastare statică în limbaj și **React este o bibliotecă JavaScript pentru construirea de interfețe cu utilizatorul**. Când lucrează împreună cu React și TypeScript, dezvoltatorii folosesc adesea extensia „.tsx” pentru fișierele lor pentru a indica faptul că acestea conțin atât TypeScript, cât și JSX (extensia de sintaxă a lui React pentru JavaScript).

## Exemplu de fișier TSX

TypeScript vă permite să definiți tipuri pentru variabilele dvs., parametrii funcției și multe altele. Veți vedea adesea cod TypeScript într-un fișier „.tsx” care specifică tipurile de elemente de recuzită, stare și alte variabile utilizate în componentele React.

```
// Exemplu: cod TypeScript într-o componentă React
interfață MyComponentProps {
   nume: șir;
   vârsta: număr;
}
const MyComponent: React.FC<MyComponentProps> = ({ nume, vârstă }) => {
   // Logica componentelor aici
   return <div>{nume} are {vârsta} ani.</div>;
};
```

## JSX (extensie de sintaxă React)

JSX este o extensie de sintaxă pentru JavaScript recomandată de React. Arată similar cu XML/HTML și este folosit pentru a descrie cum ar trebui să arate interfața de utilizare.

```
// Exemplu: JSX într-o componentă React
const MyComponent: React.FC<MyComponentProps> = ({ nume, vârstă }) => {
   return <div>{nume} are {vârsta} ani.</div>;
};
```

Fișierul „.tsx” va conține de obicei definiția unei componente React folosind componente funcționale sau componente de clasă.

```
// Exemplu: Reacționează definiția componentei într-un fișier „.tsx”.
const MyComponent: React.FC = () => {
   return <div>Bună ziua, Reacționează!</div>;
};
```

Veți vedea adesea instrucțiuni de import la începutul fișierului, aducând dependențele și modulele necesare.

```
// Exemplu: importați instrucțiuni într-un fișier „.tsx”.
import React din 'react';
```

## Cum se deschide un fișier TSX?

Fișierele TSX sunt fișiere text simplu, astfel încât să le puteți deschide în orice editor de text, de ex. Notepad. Cu toate acestea, acestea sunt fișiere de codare și sunt menite să fie deschise de IDE, de ex. Codul Visual Studio.