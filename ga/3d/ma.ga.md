{
  "date": "2019-10-11",
  "keywords": [
"ma",
"comhad ma",
"formáid comhaid ma",
"formáid comhaid",
"3d",
"Ma comhad a íoslódáil",
".ma chomhad",
".ma"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid MA agus APIanna ar féidir leo comhaid MA a oscailt agus a chruthú.",
  "title": "Formáid Chomhaid MA",
  "linktitle": "MA",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-m-gaa"
}
},
  "lastmod": "2021-06-04"
}

## Cad is comhad MA ann?

Is comhad tionscadail 3D é comhad le síneadh .ma a cruthaíodh le feidhmchlár Autodesk Maya. Tá liosta mór d'orduithe téacsúla ann chun faisnéis a shonrú faoin gcomhad. Is féidir comhad **.ma** a oscailt agus a chur in eagar in aon eagarthóir téacs chun aon fhadhb a réiteach leis na horduithe ar eagla go n-éireoidh comhad truaillithe. Tá faisnéis sna comhaid seo chun faisnéis Radharc 3D a shainiú mar chéimseata, soilsiú, beochan agus rindreáil.

## Formáid Chomhaid MA

Déantar comhaid MA a shábháil ar diosca i bhformáid téacs ASCII murab ionann agus na comhaid MB a shábháiltear ar diosca i bhformáid dhénártha. Tá tagairt mhionsonraithe le haghaidh formáid comhaid MA ar fáil in [Autodesk Maya Documentation](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001) agus is féidir tagairt a dhéanamh di le haghaidh tagartha an fhorbróra.

### Ceanntásc Comhad MA

Tosaíonn ceanntásc an chomhaid MA le cuid de na tuairimí a thugann faisnéis chruthaithe an chomhaid agus an dáta a athraíodh. Déanann léitheoirí comhad Maya neamhaird den bhloc seo mar ní úsáidtear é ach chun críche faisnéise amháin. Caithfidh ceanntásc tosú leis an gcéad sé charachtar mar //Maya áfach.

Breathnaíonn an ceanntásc comhaid ASCII mar seo a leanas.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### Tagairtí Comhad

Tá faisnéis sa chuid tagairtí comhaid de chomhad .ma faoi gach comhad Maya eile a bhfuil tagairt á déanamh dó sa chomhad seo. Is féidir gach comhad tagartha a léamh ag baint úsáide as ordú comhad amháin atá sa chomhad céanna. Is é comhréir an ordaithe comhaid nuair a úsáidtear é le haghaidh tagartha:

```
file -r -rpr prefixString fileName;
```
nó

```
file -r -ns nameSpace fileName
```
Seo teaghrán samplach.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
Léiríonn an sampla seo go mbeadh an réad gréine atá sa chomhad `solar` inrochtana sa chomhad seo agus an t-ainm solar_sun á úsáid.

### Riachtanais

Is éard atá sa chuid riachtanas de chomhad .ma ná sraith orduithe riachtanacha agus insíonn sé do mhí na Bealtaine faisnéis ar nós faisnéis maidir le leagan agus breiseán a theastaíonn chun na comhaid a léamh. Seo a leanas sampla de chuid na riachtanas.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


Sonraíonn an chéad chuid eile na ceanglais. Tá sé seo comhdhéanta de shraith orduithe éilimh. Insíonn an chuid seo den chomhad do Maya cad iad na bogearraí a theastaíonn chun an comhad a luchtú i gceart. Go sonrach, cén leagan de Maya, agus cén breiseán.

## MA comhaid a íoslódáil
Tá sé beagán deacair an comhad MA de shamhail 3d a aimsiú agus a íoslódáil. Mar sin, is féidir leat comhad MA samplach a íoslódáil ó anseo:

- [Sample.ma](../sample.ma)


## Tagairtí

* [Eagraíocht Chomhaid Maya ASCII - Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)


