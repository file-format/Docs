{
  "date": "2019-10-11",
  "keywords": [
"jhtml",
"jhtml failą",
"jhtml failo formatas",
"jhtml failo tipas",
"failą",
"tipo",
"kas yra jhtml failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JHTML – Java HTML failas",
  "description": "Sužinokite apie JHTML failo formatą ir API, kurios gali kurti ir atidaryti JHTML failus.",
  "linktitle": "JHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-jhtm-ltl"
}
},
  "lastmod": "2021-06-09"
}

## Kas yra JHTML failas?

Failas su .jhtml plėtiniu yra [HTML](/web/html/) failas su [Java](/programming/java/) kodu, kuris vykdomas serveryje, kai klientas naršyklėje užklausa šio puslapio. Serveris apdoroja užklausas, vykdo funkcijoje esančias Java funkcijas ir grąžina puslapį į kliento naršyklę. Java objektai, įterpti į JHTML puslapius, veikia serveryje, kad tvarkytų tokio tipo puslapių užklausas. JHTML failai taip pat gali pasiekti informaciją iš duomenų bazės naudodami JDBC (Java [Database](/database/) Connectivity) ryšį. JHTML failus galima atidaryti bet kuriame teksto rengyklėje ir peržiūrėti žiniatinklio naršyklėse, pvz., Google Chrome, Firefox ir Safari.

## JHTML failo formatas

JHTML yra patentuota ATG technologija ir gali būti sukurta naudojant ATG (Art Technology Group) Dynamo dokumentų rengyklę. JHTML failai parašyti paprasto teksto failo formatu, naudojant standartinį HTML ir Java kodą. Jose yra standartinių HTML žymų, be patentuotų žymų, nurodančių Java objektus. Kai vartotojas paprašo tokio puslapio, HTTP serveris persiunčia užklausą Java programų serveriui. JHTML puslapis pirmiausia konvertuojamas į .java failą ir sukompiliuojamas, kad būtų sukurtas [.class](/programming/class/) failas, kuris vykdomas kaip servlet. Tai sugeneruoja standartinių HTTP ir HTML duomenų srautą, kuris grąžinamas atgal į užklausą teikiančią naršyklę, kad būtų rodomas vartotojui. Tai naudinga norint paleisti su duomenų baze susijusias užklausas serveryje ir grąžinti galutinį sukauptą rezultatą į kliento naršyklę.

## Nuorodos

* [Globali HTML dokumento struktūra](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)


