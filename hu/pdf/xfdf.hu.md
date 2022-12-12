{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XFDF fájlformátum - Mi az XFDF fájl?",
  "description":"Ismerje meg az XFDF fájlokat és az API-kat, amelyek XFDF fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az XFDF fájl?

Az .xfdf kiterjesztésű fájl az Adobe Acrobat szoftverrel előállított XML Forms adatformátum. Az [FDF](/hu/pdf/fdf/)-hez hasonlóan az XFDF is tartalmazza az űrlapelemek leírását és értékeit XML formátumban. Ez tartalmazhatja a PDF-űrlap szövegmezőinek nevét és értékeit. Az XFDF-fájlok ember által olvasható formátumban vannak elmentve, és programozottan olvashatók olyan programozási nyelvekkel, mint a C#.

## XFDF fájlformátum - További információ

Az XFDF fájlok XML fájlformátumban kerülnek mentésre, amely egy univerzális formátum az adatok importálásához és exportálásához. Az XFDF fájlstruktúra fejlécből, majd mezőértékekből és elemadatokból áll, az alábbiak szerint.

|Elem|Attribútum|Tartalom|
---|---|---|
|\<XFDF> ||Legfelső elem|
|\<fields> ||A sablon összes mezőértéke|
|<field (T)> |név |Mezőnév|
|<value (V)> |érték |Mezőérték|

## Hivatkozások

* [FDF formátum támogatás az Acrobattól](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for -acroforms.html)
* [Adobe fejlesztői források](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

