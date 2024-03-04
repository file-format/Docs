{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "STR failas - dBASE struktūros sąrašo objektų failas - kas yra .str failas ir kaip jį atidaryti?",
  "description" : "Sužinokite apie STR dBASE struktūros sąrašo objektų failą ir kaip jį atidaryti.",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-str-lt",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Kas yra STR failas?

STR failo formatas dažniausiai siejamas su dBASE, duomenų bazių valdymo sistema. dBASE sistemoje .str failas paprastai reiškia struktūros sąrašo objekto failą. Šiame faile yra duomenų bazės lentelės struktūra, įskaitant informaciją apie laukus (stulpelius) ir jų savybes.

Struktūros sąrašo objekto faile (.str) yra metaduomenų, tokių kaip laukų pavadinimai, duomenų tipai, laukų ilgiai ir visos kitos ypatybės, susietos su kiekvienu duomenų bazės lentelės lauku. Jis naudojamas duomenų bazės lentelės struktūrai apibrėžti be faktinių duomenų įrašų.

Tokios programos kaip dBASE ar kiti duomenų bazių valdymo įrankiai gali naudoti šį failą, kad suprastų duomenų bazės lentelės išdėstymą ir atliktų tokias operacijas kaip užklausų pateikimas, atnaujinimas arba naujų įrašų kūrimas pagal šią struktūrą.

Štai pagrindinis pavyzdys, kas gali būti STR faile:

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

Šiame pavyzdyje aprašoma lentelė su keturiais laukais: ID, Vardas, Amžius ir DOB, kartu su atitinkamais duomenų tipais ir ilgiais.

## Kaip atidaryti STR failą?

Pagrindinis būdas atidaryti .str failus yra naudoti pačią dBASE, ypač Windows operacinėse sistemose. dBASE gali skaityti ir interpretuoti šių failų turinį, todėl vartotojai gali peržiūrėti ir dirbti su duomenų bazės struktūra.

Kadangi .str failai iš esmės yra paprasto teksto failai, kuriuose yra informacijos apie duomenų bazės struktūrą, juos taip pat galite atidaryti naudodami teksto rengyklę. Teksto rengyklės pavyzdžiai yra Microsoft Notepad sistemoje Windows ir Apple TextEdit sistemoje Mac. Atidarę teksto rengyklėje, galėsite matyti failo turinį, įskaitant laukų pavadinimus, duomenų tipus ir kitą struktūrinę informaciją, žmogui suprantamu formatu.

## Nuorodos
* [dBase](https://en.wikipedia.org/wiki/DBase)


