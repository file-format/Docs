{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "keywords": [
"SWF",
"failą",
"pratęsimas",
"formatu",
"vaizdo formatu",
"Kas yra SWF failas",
"swf failo formatas",
"swf failų grotuvas",
"kaip atidaryti swf failą"
],
  "title": "SWF failas – Shockwave Flash filmo failo formatas",
  "description": "Sužinokite, kas yra SWF failas ir API, kurios gali sukurti ir parodyti, kaip atidaryti SWF failą.",
  "linktitle": "SWF",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-sw-ltf"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra SWF failas?

SWF failas yra animacijos failas, sukurtas naudojant Adobe Flash. Jame gali būti įvairių tipų elementų, pvz., teksto, vektorinių vaizdų, rastrinių vaizdų, veiksmų scenarijų, objektų, tokių kaip apskritimai, linijos, kvadratai ir stačiakampis animacijai sukurti. SWF failai suskirsto šiuos daugialypės terpės elementus į kadrus, kuriuos galima leisti skirtingais kadrais per sekundę (fps). SWF reiškia trumpą žiniatinklio failą, bet taip pat žinomas kaip Shockwave formatas.

Programos, galinčios *atidaryti SWF failus**, apima Adobe Flash Player (dabar nebegaunama) ir Eltima Elmedia Player.

## SWF failo formatas – daugiau informacijos

SWF failai buvo naudojami kaip dvejetainiai failai diske. SWF failo formatas buvo naudojamas kuriant animacijas ir žaidimus, kuriuos būtų galima įterpti į svetaines ir žaisti savarankiškai. Jis taip pat palaikė vaizdo įrašus ir garsus, kurie suteikė kūrėjams daug pasirinkimų kurti interaktyvias daugialypės terpės programas. SWF failus galima leisti žiniatinklio naršyklėse, kuriose įdiegta Adobe Shockwave. Adobe Flash buvo nutraukta 2020 m. gruodžio mėn. dėl jos trūkumų ir saugumo problemų.

## Trumpa SWF failo formato istorija

SWF failo formatą iš pradžių sukūrė FutureWave Software, kad būtų rodoma animacija, skirta grotuvo programinei įrangai paleisti bet kurioje sistemoje su lėtesniu tinklo ryšiu, išlaikant mažą failo dydį. 1996 m. gruodžio mėn. Macromedia priklausė FutureWave ir buvo konvertuota į Macromedia Flash 1.0.

In 2005, Macromedia was acquired by Adobe, who announced the SWF as a part of its open source project in 2008. Tais pačiais metais Adobe išleido kodą populiariems visame pasaulyje žiniatinklio varikliams, kad jie galėtų tikrinti ir indeksuoti SWF failus. Tačiau, kadangi atrodo, kad SWF failai tampa standartiniu Flash turinio skelbimo internete formatu, SWF buvo pakeistas ir reiškia mažą žiniatinklio formatą.

## SWF failo struktūra

Kelias yra pagrindinis SWF grafinis elementas, kuris yra pagrindinių elementų segmentų seka, pradedant nuo paprastų linijų iki Bezier kreivių. Šie paprasti elementai taip pat padeda sukurti kitus papildomus primityvus, tokius kaip kubeliai, elipsės ir net tekstai. SWF grafiniai primityvai yra panašūs į kitų formatų, pvz., SVG ir MPEG-4 BIFS, grafinius elementus.

Formatas taip pat leidžia rodyti sąrašus ir pakartotinai naudoti/pervardyti jau apibrėžtus elementus. Dvejetainį SWF srauto formatą galima palyginti su QuickTime atomais, kurie yra panašūs pagal žymą, dydį ir naudingąją apkrovą. Dvejetainis srauto formatas leidžia vyresniems žaidėjams praleisti nepalaikomą turinį. Nors originalios SWF versijos apsiribojo vektorine grafika ir vaizdais, todėl naujos versijos taip pat leidžia naudoti garso ir vaizdo turinį.

A new, low-level 3D API of the Flash Player named “Stage3D” was introduced in version 11. Ši API buvo numatyta kaip OpenGL arba Direct3D atitikmuo. Stage3D apibrėžia spalvas žemo lygio kalba, vadinama Adobe Graphics Assembly Language (AGAL). Toliau pateikiami keli pagrindiniai SWF failo formato duomenų tipai.

### Koordinatės

XY koordinatės SWF failo formatu saugomos kaip sveikieji skaičiai ir matuojamos vienetu, vadinamu twip. Twip susideda iš 1/20 loginio pikselio. Loginis pikselis ir ekrano pikselis yra vienodi, kai failas atkuriamas be mastelio 100%.

### Sveikųjų skaičių tipai ir baitų tvarka

SWF failo formatu leidžiami 8, 16, 32 ir 64 bitų sveikųjų skaičių pažymėti ir nepasirašyti tipai. Little-endian baitų tvarka naudojama sveikųjų skaičių reikšmėms saugoti. Nors bitų tvarka yra baitais, ji išsaugoma big-endian. Visos sveikųjų skaičių reikšmės turi būti sulygiuotos pagal baitus. Ženkliniai sveikieji skaičiai pateikiami naudojant tradicinius 2 papildymo bitų šablonus.

### Fiksuoto taško numeriai

SWF failo formatas palaiko dviejų tipų fiksuoto taško skaičius, ty 32 ir 16 bitų.

### Slankaus kablelio skaičiai

SWF 8 ir naujesnėse versijose naudojami trijų tipų slankiojo kablelio skaičiai (FLOAT, FLOAT 16, DOUBLE), kurie yra suderinami su IEEE 754 standartu slankiojo kablelio tipams.

### Užkoduoti sveikieji skaičiai

Vieno tipo užkoduotas sveikasis skaičius palaikomas SWF 9 ir naujesnėje versijoje su kintamu baitų skaičiumi.

## Nuorodos

* [SWF failo formatas](https://en.wikipedia.org/wiki/Swf)


