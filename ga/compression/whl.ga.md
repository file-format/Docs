{
  "date": "2022-06-29",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhaid WHL - Comhad Pacáiste Rothaí Python",
  "description": "Foghlaim faoi fhormáid comhaid WHL agus APIanna ar féidir leo comhaid WHL a chruthú agus a oscailt.",
  "linktitle": "WHL",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-wh-gal"
}
},
  "lastmod": "2022-06-29"
}

## Cad is comhad WHL ann?

Is comhad pacáiste dáileacháin é comhad WHL (Roth) a shábháiltear i bhformáid roth Python. Is suiteáil formáid chaighdeánach é dáiltí Python agus tá na comhaid agus na meiteashonraí go léir a theastaíonn le haghaidh suiteála ann. Tá faisnéis sa chomhad WHL freisin faoi na leaganacha Python agus na hardáin a dtacaíonn an comhad rotha seo leo. Cosúil le comhad socraithe [MSI](/executable/msi/), is formáid réidh le suiteáil í formáid comhaid WHL a cheadaíonn an pacáiste suiteála a rith gan an dáileadh foinse a thógáil.

## Formáid Comhaid WHL

Is cartlann [ZIP](/compression/zip/) (.zip) í formáid comhaid WHL ina bhfuil na comhaid suiteála agus na meiteashonraí go léir a theastaíonn ó shuiteálaithe chun pacáiste a shuiteáil. Is féidir na comhaid WHL seo a bhaint as an rogha unzip nó feidhmchláir chaighdeánacha bogearraí dí-chomhbhrú ar nós WinZIP agus WinRAR.

### Coinbhinsiún Ainm Comhad WHL

Ainmnítear comhad WHL de réir an choinbhinsiúin seo a leanas.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

Seo a leanas sampla d’ainm comhaid WHL.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

 * `cryptography` an t-ainm pacáiste.
 * Is é `2.9.2` an leagan pacáiste de chripteagrafaíocht. Is teaghrán PEP 440-chomhlíontach é leagan mar 2.9.2, 3.4, nó 3.9.0.a3.
 * Is é `cp35` an chlib Python agus seasann sé an cur i bhfeidhm Python agus an leagan a éilíonn an roth.
 * Is é `abi3` an chlib ABI. Seasann ABI do chomhéadan dénártha feidhmchláir.
 * Is é `macosx_10_9_x86_64` an chlib ardán, rud a tharlaíonn a bheith ina bhéal go leor.

## Tagairtí

* [Cad is Rothaí Python ann agus Cén Fáth ar Chóir duit Aire a thabhairt?](https://realpython.com/python-wheels/)

* [Roth Python](https://pypi.org/project/wheel/)


