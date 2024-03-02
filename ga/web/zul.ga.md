{
  "date": "2021-05-24",
  "keywords": [
"zul",
"Comhad",
"Síneadh",
"Formáid Chomhaid",
"Síneadh Comhad",
"oscailt"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZUL - Comhad Comhéadain Úsáideora ZK",
  "description": "Foghlaim faoi fhormáid comhaid ZUL agus APIanna ar féidir leo comhaid ZUL a chruthú agus a oscailt.",
  "linktitle": "ZUL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-zu-gal"
}
},
  "lastmod": "2021-05-24"
}

## Cad is comhad ZUL ann?

Is comhad gréasáin é comhad le síneadh .zul a cruthaíodh leis an dTeanga Marcáil Chomhéadain Úsáideora (ZUML) agus ina bhfuil sainmhínithe ar eilimintí comhéadan úsáideora. Tacaíonn ranganna Ajax agus Java le húsáid an ZUML bunaithe ar [XML](/web/xml/) chun comhaid taobh an fhreastalaí a fhorbairt. Forbraíodh formáid comhaid ZUL ag ZK, creat Chomhéadain a chuireann ar do chumas feidhmchláir ghréasáin agus mhóibíleacha a thógáil gan eolas ar JavaScript nó AJAX.

## Formáid Chomhaid ZUL

ZUL files are XML-based, consisting of different elements to construct user interface. The ZK loader uses each XML element to create a component. The overall processing of the page elements such as page title, description, etc. are described by each XML processing instruction of ZUML.

### ZUL Sampla

Sa sampla seo a leanas de chód ZUML, sonraíonn an chéad líne teideal an leathanaigh, cruthaíonn an dara líne comhpháirt fréimhe le teideal agus teorainn, agus cruthaíonn an tríú líne cnaipe le lipéad agus éisteoir imeachta.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
Is féidir scéimre ZUL a íoslódáil ó https://www.zkoss.org/2005/zul/zul.xsd.
## Tagairtí

* [ZUL - Le ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)

* [Scéim ZUL](https://www.zkoss.org/2005/zul/zul.xsd)


