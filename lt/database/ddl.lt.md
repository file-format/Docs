{
  "date": "2020-11-11",
  "keywords": [
"DDL",
"pratęsimas",
"failą",
"Dokumento formatas",
"Duomenų bazės failo tipas",
"Duomenų bazės failo formatas",
"Duomenų bazės failai"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie DDL failo formatą ir API, kurios gali kurti ir atidaryti DDL failus.",
  "title": "DDL failo formatas – duomenų apibrėžimo kalbos failas",
  "linktitle": "DDL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dd-ltl"
}
},
  "lastmod": "2020-11-11"
}

## Kas yra DDL failas?

Failas su plėtiniu .ddl yra duomenų apibrėžimo kalbos failas, naudojamas duomenų bazės schemai apibrėžti. Jame yra sakinių/komandų, skirtų darbui su duomenų bazės struktūromis, tokiomis kaip lentelės, stulpeliai, įrašai ir kiti laukai. DDL failo komandos parašytos [SQL](/database/sql/) ir gali atlikti tokias operacijas kaip lentelės kūrimas duomenų bazėje, išmetimas ir atnaujinimas. Duomenų bazės schema priklauso jos sukurtai ir su ja galima atlikti visas CRUD operacijas. Populiarios programos, kuriomis galima kurti ir atidaryti DDL failus, yra Windows Text Editor, Jetbrains Intellij Idea ir EclipseLink.

## DDL komandos

Viename DDL faile gali būti kelios komandos, kurios dėl teisingos sintaksės bus vykdomos nuosekliai ir pakeis schemą, pvz., sukurs simbolių rinkinius ir lenteles, išmesdamos lenteles, pervadindamos ir keisdamos lenteles. Šios DDL komandos dažniausiai naudojamos dirbant su duomenų bazės schema.

CREATE – naudojama duomenų bazei arba jos objektams (pvz., lentelei, indeksui, funkcijai, rodiniams, saugojimo procedūrai ir paleidimams) sukurti.

DROP – naudojamas objektams ištrinti iš duomenų bazės.

ALTER – naudojama duomenų bazės struktūrai pakeisti.

TRUNCATE – naudojamas norint pašalinti visus įrašus iš lentelės, įskaitant visus įrašams skirtus tarpus.

`COMMENT` – prideda komentarų į duomenų žodyną.

PERVARDYTI – pervardija esamą objektą duomenų bazėje.

## DDL pavyzdys

Šiame pavyzdyje parodytas DDL sakinys komandai CREATE, kuri sukuria lentelę ir apibrėžia jos laukus.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## Nuorodos Nr.

* [DDL pateikė Vikipedija](https://en.wikipedia.org/wiki/Data_definition_language)


