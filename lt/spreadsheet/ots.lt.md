{
  "date": "2019-12-16",
  "keywords": [
"OTS",
"failą",
"pratęsimas",
"Dokumento formatas",
"Excel",
"Skaičiuoklė"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie OTS failo formatą ir API, kurios gali kurti ir atidaryti OTS failus.",
  "title": "OTS – „OpenDocument“ skaičiuoklės šablono failo formatas",
  "linktitle": "OTS",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-ot-lts"
}
},
  "lastmod": "2021-01-19"
}

## Kas yra OTS failas?

Failas su plėtiniu .ots yra OpenDocument skaičiuoklės šablono failas, sukurtas naudojant Calc taikomąją programinę įrangą, įtrauktą į Apache OpenOffice. Calc taikomoji programinė įranga yra panaši į Excel, kurią galima rasti Microsoft Office. OTS failo formatas naudojamas kuriant šablonus, kuriuose yra iš anksto nustatyti parametrai, susiję su stiliais, šriftu, duomenimis, skaičiuoklės išdėstymu ir formatavimu. OTF failuose yra mime tipo application/vnd.oasis.opendocument.spreadsheet-template. Šiuos šablonų failus galima naudoti kaip pradinį tašką generuojant ir išsaugant tikrus duomenų failus, kurie yra išsaugoti [ODS file format](/spreadsheet/ods/). OTS failus galima naudoti su tokiomis programomis kaip OpenOffice ir LibreOffice.

## OTS failo formatas

OTS failai išsaugomi OASIS OpenDocument XML failo formatu, kurį sudaro kelių antrinių dokumentų rinkinys su paketu kaip [ZIP](/compression/zip/) archyvas. Kiekviename ZIP archyve saugoma dalis viso dokumento, o kiekviename antriniame dokumente saugomas tam tikras dokumento aspektas. Pavyzdžiui, viename antriniame dokumente yra stiliaus informacija, o kitame – dokumento turinys. Įprastą ODF dokumentą sudaro šie komponentai:

### OTS Content.xml

Content.xml faile yra tikrasis dokumento turinys. Tačiau tai neapima dvejetainių duomenų, pvz., vaizdų.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### OTS failo formato Styles.xml

Faile styles.xml yra stiliaus informacijos ir jis labai naudojamas formatavimui ir išdėstymui. Stilių tipai apima:

 * Pastraipų stiliai
 * Puslapių stiliai
 * Personažų stiliai
 * Rėmelių stiliai
 * Stilių sąrašas

### Meta.xml

Meta.xml faile yra informacijos apie failo metaduomenis, pvz., autorių, paskutinio modifikavimo datą ir kt.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Settings.xml

settings.xml faile yra dokumento lygio nustatymai, tokie kaip mastelio koeficientas ir žymeklio padėtis.

## Nuorodos Nr.

* [OpenDocument 1.2 specifikacija](https://www.oasis-open.org/standards#opendocumentv1.2)

* [OpenDocument – pateikė Vikipedija](https://en.wikipedia.org/wiki/OpenDocument)


