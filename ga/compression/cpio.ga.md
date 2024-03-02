{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Comhad CPIO - Formáid Chomhaid Cartlainne Unix CPIO",
  "description":"Faigh amach cad is comhad CPIO agus APIs ann ar féidir comhaid CPIO a chruthú agus a oscailt.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio-ga",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## Cad is comhad CPIO ann?

Is comhad cartlainne é comhad CPIO a cruthaíodh i bhformáid Unix's Copy In Copy Out (CPIO). Tá sé cosúil le formáid comhaid TAR seachas go bhfuil sé neamh-chomhbhrúite. Is féidir le comhaid CPIO comhaid gléas a stóráil, naisc siombalacha agus tréithe comhaid leathnaithe.

## Formáid Chomhaid CPIO

Cruthaítear cartlann CPIO mar chomhad dénártha nach bhfuil inléite ag an duine. Stórálann sé an bailiúchán comhad agus eolaire. Aithnítear ábhar cartlainne CPIO le faisnéis meiteashonraí amhail ainmneacha comhaid, ceadanna, úinéireacht agus stampaí ama. Stóráiltear an fhaisnéis meiteashonraí seo sa chomhad cartlainne freisin le go bhféadfaidh an córas rochtain cliathánach a dhéanamh air.

## Formáid Chartlann CPIO

Cuimsíonn comhad CPIO comhad comhalta comhdhlúite amháin nó níos mó. Tá ceanntásc i ngach comhad sa chartlann agus ansin inneachar an chomhaid mar atá luaite sa cheanntásc. Tá ceanntásc eile sa chartlann ag an deireadh a bhfuil cur síos air ag comhad folamh darb ainm TRAILER!!.

### Cineálacha Cartlanna CPIO

Tá dhá chineál cartlann CPIO ann. Siad seo difriúil ach amháin i stíl an header.

* Cartlanna ASCII - Tá ceanntásc inphriontáilte ag na cartlanna CPIO seo a thagann chun bheith ina gcuid de chartlann CPIO más comhaid ASCII atá sa chartlann féin

* Cartlanna Dénártha - Tá ceanntásca dénártha ag na cartlanna CPIO seo.


## Ag obair le Cartlann CPIO

### Conas Cartlanna CPIO a chruthú?

Is féidir leat CPIO a chruthú ar chórais cosúil le Unix ag baint úsáide as an ordú ** cpio**. Gheobhaidh an t-ordú seo a leanas gach comhad agus eolaire san eolaire reatha agus ina fochomhadlanna. Ansin cuirtear an t-aschur seo chuig an ordú cpio a ghinfidh cartlann CPIO nua darb ainm archive.cpio.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### Conas Comhaid a Bhaint as Cartlanna CPIO?

Baineann an t-ordú seo a leanas na comhaid as cartlann atá ann cheana féin.

```
cpio -id < archive_cpio.cpio
```
Léifidh sé an comhad archive.cpio ón ionchur caighdeánach agus bainfidh sé na comhaid chuig an eolaire reatha.


## Tagairtí

* [CPIO - Le Vicipéid]( https://en.wikipedia.org/wiki/Cpio)

* [CPIO File Format](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

