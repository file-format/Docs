{
  "date" : "2023-12-28",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Comhad TSX - Comhad React TypeScript - Cad é an comhad .tsx agus conas é a oscailt?",
  "description":"Foghlaim faoi chomhad TSX React TypeScript agus conas é a oscailt.",
  "linktitle" : "TSX",
  "menu" : {
    "docs" : {
      "identifier": "programming-tsx-ga",
      "parent" : "programming"
}
},
  "lastmod" : "2023-12-28"
}

## Cad is comhad TSX ann?

Is minic a bhaineann comhad TSX le comhaid TypeScript a bhfuil cód **React** iontu. **Is forshraith de JavaScript** é TypeScript a chuireann clóscríobh statach leis an teanga, agus **Is leabharlann JavaScript é React chun comhéadain úsáideora a thógáil**. Agus iad ag obair le React agus TypeScript le chéile, is minic a úsáideann forbróirí an síneadh .tsx dá gcuid comhad chun a chur in iúl go bhfuil TypeScript agus JSX (síneadh comhréire React le haghaidh JavaScript) iontu.

## Sampla Comhad TSX

Ligeann TypeScript duit cineálacha a shainiú do d’athróga, paraiméadair feidhme agus níos mó. Is minic a fheicfidh tú cód TypeScript i gcomhad .tsx ina sonraítear na cineálacha frapaí, stáit agus athróg eile a úsáidtear i gcomhpháirteanna React.

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

## JSX (Eisínteacht Comhréire React)

Is síneadh comhréire é JSX do JavaScript atá molta ag React. Breathnaíonn sé cosúil le XML/HTML agus úsáidtear é chun cur síos ar an gcuma ar cheart don Chomhéadain.

```
// Example: JSX in a React component
const MyComponent: React.FC<MyComponentProps> = ({ name, age }) => {
  return <div>{name} is {age} years old.</div>;
};
```

Go hiondúil beidh an sainmhíniú ar chomhpháirt React ag baint úsáide as comhpháirteanna feidhmiúla nó comhpháirteanna ranga sa chomhad .tsx.

```
// Example: React component definition in a ".tsx" file
const MyComponent: React.FC = () => {
  return <div>Hello, React!</div>;
};
```

Is minic a fheicfidh tú ráitis allmhairithe ag tús an chomhaid, ag tabhairt isteach na spleáchais agus na modúil riachtanacha.

```
// Example: Import statements in a ".tsx" file
import React from 'react';
```

## Conas comhad TSX a oscailt?

Is comhaid gnáth-théacs iad comhaid TSX ionas gur féidir leat iad a oscailt in aon eagarthóir téacs m.sh. Notepad. Mar sin féin, is comhaid códaithe iad seo agus tá sé i gceist iad a oscailt ag IDE eg Cód Stiúideo Amharc.

