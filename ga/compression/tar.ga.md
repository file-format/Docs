{
  "date": "2019-10-11",
  "keywords": [
"comhad tarra",
"formáid comhaid tarra",
"cad is comhad tarra ann",
"comhad",
"sampla tarra",
"síneadh comhad tarra",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TAR - Formáid Chomhaid Cartlainne Unix",
  "description": "Foghlaim faoi cad is comhad TAR ann agus APIanna ar féidir comhaid TAR a chruthú agus a oscailt.",
  "linktitle": "TAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-ta-gar"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad TAR ann?

Is cartlann iad comhaid le síneadh .tar a cruthaíodh le fóntais Unix-bhunaithe chun comhad amháin nó níos mó a bhailiú. Stóráiltear comhaid iolracha i bhformáid neamh-chomhbhrúite le tacaíocht ó chomhaid chomh maith le fillteáin a chur leis an gcartlann. Tá áirgiúlacht TAR ar Unix bunaithe ar Ordú, ach tá an chuid is mó de na córais cartlannaithe comhad ar bheagnach gach córas oibriúcháin ag tacú le comhaid a chruthaítear. Chruthaigh AT&T Bell Laboratories é den chéad uair i 1979 agus foilsíodh leaganacha ina dhiaidh sin le himeacht ama.

## Formáid Chomhaid TAR

TAR is an open file format with full specifications available for developer's reference. Its file structure was standardized in POSIX.1-1988 and later in POSIX.1-2001. Coinníonn na tacair sonraí a chruthaítear le tarra faisnéis faoi pharaiméadair an chórais comhad mar:

* Ainm

* Stampaí Ama

* Úinéireacht

* Ceadanna Rochtana Comhad

* Eagraíocht Eolaire


Níl aon uimhir draíochta ag comhad TAR. Tá sraith de bhlocanna ann ina bhfuil gach bloc de bhearta BLOCKSIZE.

Léirítear gach comhad a chartlannaítear le bloc ceanntásca a chuireann síos ar an gcomhad, agus ina dhiaidh sin tá nialas nó níos mó bloic a thugann a bhfuil sa chomhad. Ag deireadh an chomhaid cartlainne tá dhá bhloc 512-beart líonta le nialais dhénártha mar mharcóir deireadh comhaid. Ba cheart do chóras réasúnta a leithéid de mharcóir deireadh comhaid a scríobh ag deireadh cartlann, ach ní mór glacadh leis go bhfuil bloc den sórt sin ann agus cartlann á léamh. Go háirithe eisíonn GNU tar rabhadh i gcónaí mura dtagann sé trasna air.

Féadfar na bloic a bhlocáil le haghaidh oibríochtaí fisiceacha I/O. Scríobhtar gach taifead de n bloic (áit a bhfuil n socraithe ag an rogha blocála-fachtóir = 512-size go tarra) le hoibríocht amháin write(). Ar théipeanna maighnéadacha, is taifead aonair é toradh a leithéid de scríobh. Agus cartlann á scríobh, ba cheart an taifead deireanach de bhlocanna a scríobh ag an méid iomlán, le bloic tar éis an bhloic nialais ina bhfuil na nialais go léir. Agus cartlann á léamh, ba cheart do chóras réasúnta cartlann a láimhseáil i gceart a bhfuil a taifead deireanach níos giorra ná an chuid eile, nó ina bhfuil taifid truflais tar éis bloc nialasach.

### Ceanntásc Comhad TAR

Cosúil le haon cheanntásca comhaid eile, tá meiteashonraí faoi chomhad i dtaifead ceanntásca an chomhaid agus taispeántar é sa tábla seo a leanas.

|Fritháireamh réimse|Méid an raoin (Beit)|Réimse
---|---|---|
|0|100|Ainm comhaid
|100|8|Mód comhaid
|108|8|Aitheantas úsáideora uimhriúil an úinéara
|116|8|Aitheantas úsáideora uimhriúil an ghrúpa
|124|12|Méid an chomhaid i mbearta (bonn octal)
|136|12|Aga modhnuithe is déanaí san fhormáid ama uimhriúil Unix (octal)
|148|8|Seiceáil le haghaidh taifead ceanntásca
|156|1|Táscaire naisc (cineál comhaid)
|157|100|Ainm an chomhaid nasctha

Líontar réimsí neamhúsáidte le bearta NUL. Cuimsíonn ceanntásc 257 beart atá stuáilte le bearta NUL chun é a líonadh go dtí taifead 512 beart.

## Conas Comhad TAR a Chruthú

### Cruthaigh Comhad TAR ar Windows

Ar Windows, is féidir leat an Fochóras Windows le haghaidh Linux (WSL) nó uirlisí tríú páirtí cosúil le 7-Zip a úsáid chun comhaid TAR a chruthú. Seo conas é a dhéanamh ag baint úsáide as WSL:

 1. Suiteáil WSL mura bhfuil sé agat cheana féin. Is féidir leat é a shuiteáil trí shocruithe Gnéithe Windows.

 1. Oscail críochfort WSL agus bain úsáid as an t-ordú tarra céanna agus atá ar chórais Linux nó Unix chun comhad TAR a chruthú.

### Cruthaigh Comhad TAF ar Linux ón Líne Ordú

Chun comhad TAR a chruthú ag baint úsáide as an líne ordaithe ar chórais bunaithe ar Linux nó Unix, oscail teirminéal agus úsáid an t-ordú tarra. Is féidir leat comhad TAR a chruthú i bhformáidí comhbhrú éagsúla (m.sh., .tar.gz, .tar.bz2, .tar.xz), ach anseo, cruthóimid gnáthchomhad .tar:

Chun comhad TAR a chruthú ó chomhad nó eolaire amháin, bain úsáid as an ordú seo a leanas:

```
tar -cvf archive.tar file_or_directory
```

## Conas Comhad TAR a oscailt

### Oscail Comhad TAR ar Windows

Ní mór duit fóntais dí-chomhbhrú a shuiteáil ar Windows OS mar 7-Zip. Is áirgiúlacht cartlannaithe saor in aisce é ar féidir a úsáid chun formáidí comhaid comhbhrúite éagsúla a chruthú agus a bhaint as. Cliceáil ar dheis ar do chomhad TAR agus roghnaigh **Sliocht** rogha.

### Oscail Comhad TAR ar Mac

Ar Mac, níl le déanamh ach cliceáil faoi dhó ar an gcomhad TAR, TGZ, nó TAR.GZ chun é a dhíphacáil.

### Oscail Comhad TAR ar Linux

Má tá Linux nó an aip Mac Terminal in úsáid agat, úsáid tar -xvf le haghaidh comhaid TAR, nó tar -xvzf le haghaidh comhaid a chríochnaíonn in TGZ nó TAR.GZ.

## Tagairtí ##

* [TAR - Le Vicipéid]( https://ga.wikipedia.org/wiki/Tar_(computing))

* [Formáid Bhunúsach TAR]( https://www.gnu.org/software/tar/manual/html_node/Standard.html)


