{
  "date": "2019-10-11",
  "keywords": [
"comhad rtf",
"Formáid comhaid rtf saor in aisce,",
"Cad is comhad rtf ann",
"comhad",
"sampla rtf",
"Síneadh comhad rtf saor in aisce,",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RTF - Formáid Téacs Saibhir",
  "description": "Foghlaim faoi fhormáid comhaid RTF agus APIanna ar féidir leo comhaid RTF a chruthú agus a oscailt.",
  "linktitle": "RTF",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-rt-gaf"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad RTF ann?

Arna thabhairt isteach agus doiciméadaithe ag Microsoft, is ionann an Rich Text Format (**RTF**) agus modh chun téacs formáidithe agus grafaic a ionchódú le húsáid laistigh d’fheidhmchláir. Éascaíonn an fhormáid malartú doiciméad tras-ardán le Táirgí Microsoft eile, rud a fhreastalaíonn ar chuspóir na hidir-inoibritheachta. Fágann an cumas seo gur caighdeán aistrithe sonraí é idir bogearraí próiseála focal agus, mar sin, is féidir inneachar a aistriú ó chóras oibriúcháin amháin go ceann eile gan formáidiú doiciméad a chailleadh. Tá na sonraíochtaí formáid comhaid ar fáil ag Microsoft don phobal [download](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf) agus is féidir tagairt a dhéanamh dóibh ó thaobh an fhorbróra de.

## Stair Achomair d'Fhormáid Chomhaid RTF ##

RTF file format has underwent several revisions since its publication. Its official version for read/write was published as part of Microsoft Word 3.0 for Macintosh with version 1.0 specifications. The final version of specifications, 1.9.1 was published by Microsoft in Mar 2008. Ní dhéantar tuilleadh feabhsuithe ar na sonraíochtaí ina dhiaidh seo. Faoi láthair, tá feidhmchláir níos saibhre ag beagnach gach córas oibriúcháin a laghdaigh/laghdaigh úsáid formáid comhaid RTF.

## Sonraíochtaí Formáid Chomhaid RTF ##

RTF serves as a standard of data transfer between word processing software and transfer of content from one operating system to another. This is achieved using control words that were introduced by Microsoft Office Word up through 2007. Tá comhad RTF caighdeánach comhdhéanta de ASCII chun téacs saibhir a léiriú agus le carachtair neamh-ASCII a thiontaítear go luachanna cód cuí. Is féidir le leaganacha níos nuaí de Word comhaid RTF a ghintear le leaganacha roimhe seo a léamh, agus déanann na leaganacha níos sine neamhaird ar fhocail rialaithe agus grúpaí nach dtuigeann siad.

### Bunús RTF a Thuiscint ###

Úsáideann comhaid RTF gnáth-théacs ASCII 7-giotán, ar a bhfuil:

* focail a rialú

* siombailí rialaithe, agus

*grúpaí.


Feidhmíonn siad seo mar bhunchlocha chun sonraí RTF a léiriú mar ionchódú téacs agus carachtar intuigthe.

#### Focal Rialaithe ####

Léiríonn siad seo ordú sainfhormáidithe a úsáidtear chun carachtair a mharcáil le taispeáint agus ní féidir leo a bheith níos faide ná 32 litir. Sainmhínítear focal rialaithe mar:

\<ASCII Letter Sequence> //<//Delimiter//> //

Tá gach focal rialaithe cásíogair agus tosaíonn sé le cúlslais. Is féidir Aibítir ASCII (a trí z agus A go Z) a bheith i Seicheamh Litreach ASCII. Tá an<Delimite> marcálann sé deireadh ainm an fhocail rialaithe agus is féidir leis a bheith mar cheann díobh seo a leanas:

* A spás. Ní fheidhmíonn sé seo ach chun teorainn a chur le focal rialaithe agus déantar neamhaird de sa phróiseáil ina dhiaidh sin.

* Figiúr uimhriúil nó comhartha lúide ASCII, a thugann le fios go bhfuil baint ag paraiméadar uimhriúil leis an bhfocal rialaithe. Déantar an seicheamh digiteach ina dhiaidh sin a theorannú ag aon charachtar seachas digit ASCII (focal rialaithe eile a thosaíonn le cúlslais go hiondúil). Is féidir leis an bparaiméadar a bheith ina uimhir dheachúil dhearfach nó dhiúltach. Is é raon na luachanna don uimhir go hainmniúil –32768 trí 32767, ie, slánuimhir sínithe 16-giotán. Glacann líon beag focal rialaithe luachanna sa raon‌ −2,147,483,648 go 2,147,483,647 (slánuimhir sínithe 32-giotán). Áirítear ar na focail rialaithe seo **\binN**, **\revdttmN//**, **\rsidN** focail rialaithe a bhaineann le chéile agus roinnt airíonna pictiúir mar **\bliptagN**. Anseo seasann **N** don pharaiméadar uimhriúil. Caithfidh parsálaí RTF suas le 10 ndigit a cheadú go roghnach agus comhartha lúide roimhe sin. Más spás é an teorannóir, déantar é a chaitheamh i leataobh, is é sin, níl sé san áireamh sa phróiseáil ina dhiaidh sin.

* Aon charachtar seachas litir nó digit. Sa chás seo, cuireann an carachtar teorannaithe deireadh leis an bhfocal rialaithe agus níl sé mar chuid den fhocal rialaithe. Ar nós cúlslais “\”, a chiallaíonn focal rialaithe nua nó siombail rialaithe seo a leanas.


#### Siombail Rialaithe ####

Is ionann Siombail Rialaithe agus teagmhas speisialta a bhfuil brí ar leith leis ag brath ar a bhfuil ann. Is éard atá ann ná cúlslais agus carachtar speisialta (carachtar neamhaibítre) ina dhiaidh sin agus níl aon teorannóirí ann.

#### Grúpa ####

Is féidir le grúpa a bheith comhdhéanta de théacs, focail rialaithe, nó siombailí rialaithe faoi iamh i braces (**{ }**). Léiríonn an brace tosaigh (**{** ) tús an ghrúpa agus léiríonn an brace deiridh ( **}**) deireadh an ghrúpa. Sonraíonn gach grúpa an téacs a dtéann an grúpa i bhfeidhm air agus tréithe éagsúla an téacs sin.

### Struchtúr Comhad RTF ###

Tá an chomhréir Chaighdeánach seo a leanas i gcomhad RTF:

Arna thabhairt isteach agus doiciméadaithe ag Microsoft, is ionann an Rich Text Format (**RTF**) agus modh chun téacs formáidithe agus grafaic a ionchódú le húsáid laistigh d’fheidhmchláir. Éascaíonn an fhormáid malartú doiciméad tras-ardán le Táirgí Microsoft eile, rud a fhreastalaíonn ar chuspóir na hidir-inoibritheachta. Fágann an cumas seo gur caighdeán aistrithe sonraí é idir bogearraí próiseála focal agus, mar sin, is féidir inneachar a aistriú ó chóras oibriúcháin amháin go ceann eile gan formáidiú doiciméad a chailleadh. Tá na sonraíochtaí formáid comhaid ar fáil ag Microsoft don phobal [download](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf) agus is féidir tagairt a dhéanamh dóibh ó thaobh an fhorbróra de.

#### Ceanntásc RTF ####

Tá an ionadaíocht seo a leanas ag Ceanntásca RTF.

| Réimse | Cur síos
---|---|
|\<header> |**\rtf1\fbidis**? \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

Caithfidh táblaí ceanntásca a bheith san ord seo má tá siad ann. Is féidir leis an gcomhad RTF grúpaí le haghaidh clónna, stíleanna, dath scáileáin, pictiúir, fonótaí, nótaí tráchta (nótaí), ceanntásca agus buntásca, faisnéis achomair, réimsí, leabharmharcanna, doiciméad-, rannán-, airíonna formáidithe carachtar, matamaitic, íomhánna, agus rudaí. Má tá cló, comhad, stíl, dath, marc athbhreithnithe, agus grúpaí faisnéise achomair agus airíonna formáidithe doiciméad san áireamh sa chomhad, caithfidh siad a bheith le feiceáil sa cheanntásc RTF, a thagann roimh an gcomhlacht RTF. Mura n-úsáidtear ábhar grúpa ar bith, is féidir an grúpa a fhágáil ar lár. Ní mór do ghrúpa ar bith a úsáideann na hairíonna atá sainmhínithe i ngrúpa eile a bheith le feiceáil i ndiaidh an ghrúpa a shainíonn na hairíonna sin. Mar shampla, caithfidh dath agus airíonna cló a bheith roimh an stílghrúpa.

#### Leagan RTF ####

Ní mór do dhoiciméad RTF tosú amach leis na sé charachtar seo:

```
{\rtf1
```
áit a léiríonn an 1 uimhir an leagain RTF.

#### Socraigh Carachtair ####

Tar éis an {\rtf1, ba cheart don doiciméad a dhearbhú cén tacar carachtar a úsáideann sé. Is é ceann de na horduithe seo an bealach chun tacar carachtar a dhearbhú:

`\ansi` - Tá an doiciméad sa tacar carachtar ANSI, ar a dtugtar Cód Leathanach 1252 freisin, an gnáththacar carachtar MSWindows.

`\ mac` - Tá an doiciméad sa tacar carachtar MacAscii, an gnáth-thacar carachtar faoi sheanleaganacha (réamh-10) de Mac OS.

`\pc` - Tá an doiciméad i gCód DOS Leathanach 437, an tacar carachtar réamhshocraithe do MS-DOS. Tabharfaidh clóscríobhaithe le cuimhne matán maith faoi deara gurb é seo an tacar carachtar a úsáidtear fós chun cóid Alt uimhriúil” a léirmhíniú - ie, nuair a choinníonn tú Alt síos agus nuair a chlóscríobhann tú 130” ar an eochaircheap uimhriúil, táirgeann sé é, mar gheall ar charachtar 130 in CP437 is an é. Is é sin an t-aon úsáid a fheiceann CP437 na laethanta seo.

`\ pca` - Tá an doiciméad i Leathanach an Chóid DOS 850, ar a dtugtar an Leathanach Cód Ilteangach MS-DOS freisin.

#### Ordú Cló ####

Leanann an t-ordú `\ deffN` an sainmhíniú ar thacar Carachtair. Sainmhíníonn sé seo gurb í an chlóuimhir N an cló réamhshocraithe don doiciméad seo. Déantar tagairt don chlóuimhir N ón tábla cló. Tá an t-ordú `\ deffN` roghnach go teicniúil, ach ba cheart go mbeadh sé ann le bheith ar an taobh sábháilte mar phrolog coitianta cosúil le seo a leanas roghnaigh cló 0 mar an cló réamhshocraithe.

`{\rtf1\ansi\deff0`

#### Cló Tábla ####

Tá na clónna go léir is féidir a úsáid i ndoiciméad liostaithe i dtábla cló ina bhfuil clóuimhir léirithe ag gach cló. Ní mór tábla cló a bheith ag an doiciméad cé go n-oibreoidh roinnt clár gan é sin freisin.

Is é {\fonttbl //...declarations//...} an chomhréir le haghaidh tábla cló, ina bhfuil an chomhréir bhunúsach seo ag gach dearbhú:

`{\fnumber\familycommand Clóainm;}`

Seo a leanas tábla cló le ceithre dhearbhú:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

I ndoiciméad leis an tábla cló sin, phriontáilfeadh `{\f2 stuff}` stuff” in Courier New. Ní féidir cló a úsáid i ndoiciméad go dtí go bhfuil sé liostaithe sa tábla cló.

### Críoch an Doiciméid ###

Caithfidh } críochnú le gach doiciméad RTF, chun an grúpa a d'oscail an { is é sin an chéad charachtar sa doiciméad a dhúnadh. Ní féidir le haon rud an } deiridh a leanúint, ach amháin b'fhéidir líne nua.

## Tagairtí ##

* [Sonraíochtaí RTF 1.9.1](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf)

* [Formáid Téacs saibhir](https://en.wikipedia.org/wiki/Rich_Text_Format)


