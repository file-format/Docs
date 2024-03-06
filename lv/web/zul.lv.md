{
  "date": "2021-05-24",
  "keywords": [
"zul",
"Fails",
"Pagarinājums",
"Faila formāts",
"Faila paplašinājums",
"atvērts"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZUL — ZK lietotāja interfeisa fails",
  "description": "Uzziniet par ZUL failu formātu un API, kas var izveidot un atvērt ZUL failus.",
  "linktitle": "ZUL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-zu-lvl"
}
},
  "lastmod": "2021-05-24"
}

## Kas ir ZUL fails?

Fails ar paplašinājumu .zul ir tīmekļa fails, kas izveidots ar lietotāja interfeisa iezīmēšanas valodu (User Interface Markup Language — ZUML) un satur lietotāja interfeisa elementu definīcijas. Ajax un Java klases atbalsta [XML](/web/xml/) bāzes ZUML izmantošanu servera puses failu izstrādei. ZUL faila formātu izstrādāja ZK — lietotāja saskarnes ietvars, kas ļauj izveidot tīmekļa un mobilās lietojumprogrammas, nezinot JavaScript vai AJAX.

## ZUL faila formāts

ZUL files are XML-based, consisting of different elements to construct user interface. The ZK loader uses each XML element to create a component. The overall processing of the page elements such as page title, description, etc. are described by each XML processing instruction of ZUML.

### ZUL piemērs

Nākamajā ZUML koda piemērā pirmajā rindā ir norādīts lapas nosaukums, otrajā rindā tiek izveidots saknes komponents ar virsrakstu un apmali, bet trešajā rindā tiek izveidota poga ar iezīmi un notikumu klausītāju.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
ZUL shēmu var lejupielādēt no https://www.zkoss.org/2005/zul/zul.xsd.

## Atsauces
* [ZUL — ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [ZUL shēma](https://www.zkoss.org/2005/zul/zul.xsd)
