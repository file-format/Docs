{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru XFDF - Co je soubor XFDF?",
  "description":"Další informace o souboru XFDF a rozhraních API, která mohou vytvářet a otevírat soubory XFDF.",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor XFDF?

Soubor s příponou .xfdf je formát dat XML Forms, který je generován pomocí softwaru Adobe Acrobat. Stejně jako [FDF](/cs/pdf/fdf/) obsahuje XFDF popis formulářových prvků a jejich hodnoty ve formátu XML. To může zahrnovat názvy a hodnoty textových polí ve formuláři PDF. XFDF jsou uloženy ve formátu čitelném pro člověka a lze je číst programově pomocí programovacích jazyků, jako je C#.

## Formát souboru XFDF – Další informace

Soubory XFDF se ukládají ve formátu XML, což je univerzální formát používaný pro import a export dat. Struktura souboru XFDF se skládá ze záhlaví, za nímž následují hodnoty polí a data prvků, jak je uvedeno níže.

|Prvek|Atribut|Obsah|
---|---|---|
|\<XFDF> ||Nejvyšší prvek|
|\<fields> ||Všechny hodnoty polí pro tuto šablonu|
|<field (T)> |jméno |Název pole|
|<value (V)> |hodnota |Hodnota pole|

## Reference

* [Podpora formátu FDF od společnosti Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for-acroforms.html)
* [Zdroje pro vývojáře Adobe](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

