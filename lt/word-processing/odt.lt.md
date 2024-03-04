{
  "date": "2019-10-11",
  "keywords": [
"odt failą",
"odt failo formatas",
"kas yra odt failas",
"failą",
"keistas pavyzdys",
"odt failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ODT – „OpenDocument“ tekstinis failas",
  "description": "Sužinokite apie ODT failo formatą ir API, kurios gali kurti ir atidaryti ODT failus.",
  "linktitle": "ODT",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-od-ltt"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra ODT failas?

ODT failai yra dokumentų tipai, sukurti naudojant teksto apdorojimo programas, pagrįstas OpenDocument teksto failo formatu. Jie sukurti naudojant teksto rengyklės programas, tokias kaip nemokama OpenOffice Writer, ir gali turėti tokį turinį kaip tekstas, vaizdai, objektai ir stiliai. ODT failas yra skirtas Writer tekstų rengyklėms tai, kas [DOCX](/word-processing/docx/) yra Microsoft Word. Kelios programos, įskaitant Google dokumentus ir Google žiniatinklio teksto rengyklę, įtrauktą į Google diską, gali atidaryti ODT failus redaguoti. Microsoft Word taip pat gali atidaryti ODT failus ir išsaugoti juos kitais formatais, pvz., [DOC](/word-processing/doc/) ir DOCX.

## Trumpa istorija ##

ODP failo formato specifikacijos yra pagrįstos standartu, sukurtu kaip ODF specifikacijos. Šios specifikacijos praeityje buvo sukurtos trimis versijomis, kurias sukūrė ir paskelbė OASIS:

**2005 m.** 1.0 versija buvo paskelbta 2005 m. gegužės mėn

**2007 m.:** 1.1 versija buvo paskelbta 2007 m. vasario mėn

**2011 m.:** 1.2 versija buvo paskelbta 2011 m. rugsėjo mėn

Pereinant nuo ODF 1.0 prie 1.1 versijų buvo gana nedidelių pakeitimų. [ODF 1.2 version](https://www.oasis-open.org/standards#opendocumentv1.2) yra naujausia ODF specifikacijų versija, todėl kūrėjai turėtų konsultuotis dėl programų, susijusių su ODS skaitymu / rašymu, kūrimo.

## Failo formato specifikacijos ##

OpenDocument formatas palaiko dokumento vaizdavimą kaip vieną XML dokumentą ir kelių antrinių dokumentų rinkinį pakete kaip [ZIP](/compression/zip/) archyvą. Kiekviename faile iš ZIP archyvo saugoma dalis viso dokumento. Kiekviename antriniame dokumente saugomas tam tikras dokumento aspektas. Pavyzdžiui, viename antriniame dokumente yra stiliaus informacija, o kitame – dokumento turinys. Įprastą ODF dokumentą sudaro šie komponentai:

* content.xml – dokumento turinys ir turinyje naudojami automatiniai stiliai.

* styles.xml – dokumento turinyje naudojami stiliai ir pačiuose stiliuose naudojami automatiniai stiliai.

* meta.xml – dokumento metainformacija, pvz., autorius arba paskutinio išsaugojimo veiksmo laikas.

* settings.xml – konkrečios programos nustatymai, pvz., lango dydis arba spausdintuvo informacija.


Be šių, pakete gali būti daug kitų antrinių dokumentų, tokių kaip dokumento miniatiūra, vaizdai ir kt. Dokumentų failai yra ODF failų poaibis, kuriame turinys (lapai) saugomas //content.xml// antriniame dokumente.

## Nuorodos Nr.

* [OpenDocument – Vikipedija](https://en.wikipedia.org/wiki/OpenDocument)


