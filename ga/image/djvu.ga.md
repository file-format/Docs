{
  "date": "2019-10-11",
  "keywords": [
"Comhad djvu",
"Formáid comhaid djvu",
"Cad é an comhad djvu",
"comhad",
"Djvu sampla",
"Síneadh comhad djvu",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhaid DJVU",
  "description": "Foghlaim faoi fhormáid comhaid DJVU agus APIs ar féidir leo comhaid DJVU a chruthú agus a oscailt.",
  "linktitle": "DJVU",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-djv-gau"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad DJVU ann?

Is formáid comhaid grafaice é DjVu, a fhuaimnítear mar déjà vu”, atá dírithe ar dhoiciméid agus leabhair scanta go háirithe iad siúd a chuimsíonn téacs, líníochtaí, íomhánna agus grianghraif. D'fhorbair AT&T Labs é. Úsáideann sé teicnící iolracha cosúil le deighilt ciseal íomhá na n-íomhánna téacs agus cúlra, luchtú forásach, códú uimhríochtúil agus comhbhrú caillte na n-íomhánna biotúnacha. Ós rud é gur féidir íomhánna datha, grianghraif, téacs agus líníochtaí atá comhbhrúite ach ardcháilíochta a bheith i gcomhad DJVU agus gur féidir iad a shábháil i níos lú spáis, mar sin, úsáidtear é ar an ngréasán mar ríomhleabhair, lámhleabhair, nuachtáin, doiciméid ársa, etc.

Is féidir DjVu a ghrádú mar rogha eile seachas [PDF](/pdf/). Is iad na síntí comhaid a bhaineann le DjVu ná .DJVU nó .DJV. Is féidir le DjVu cóimheasa comhbhrú a bhaint amach thart ar 5 – 10 níos fearr ná na modhanna atá ann cheana féin ar nós [JPEG](/image/jpeg/) & [GIF](/image/gif/) do dhoiciméid datha agus 3 – 8 n-uaire níos fearr ná [TIFF](/image/tiff/) i ndoiciméid dubh agus bán. Is féidir doiciméid scanta ag 300 pso le lándaite suas le 25 MB a chomhbhrú síos go dtí 30 go 100 KB. Ar an gcaoi chéanna is féidir doiciméid dhubh agus bhána a chomhbhrú suas le 5 go 30 KB. Is féidir le meánleathanach HTML a bheith suas le 50 KB, mar sin is féidir na doiciméid seo a uaslódáil ar an ngréasán gan aon fhadhb.

## Stair Ghearr ##

The DjVu technology was developed in AT&T labs by [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3%A9on_Bottou), Patrick Haffner, and Paul G from 1996 to 2001. Tá formáid comhaid DjVu tar éis dul trí leasuithe éagsúla, an ceann is déanaí ó 2005.


|Leagan|Dáta Eisiúna|Nótaí
---|---|---|
|1–19|1996–1999|Seo iad na leaganacha forbraíochta.
|20|Aibreán 1999|Athraíodh leathanach aonair go formáid Illeathanaigh.
|23|Iúil 2002|Cumann CID
|24|Feabhra 2003|Spúnóg LTAno
|21|Meán Fómhair 1999|Cuireadh formáid indíreach stórála ina ionad. Cuireadh ciseal cuardaigh téacs leis.
|22|Aibreán 2001|Treoshuíomh leathanaigh, dath JB2
|25|Bealtaine 2003|Sumpall NAVM. Cuireadh tacaíocht do leabharmharcanna DjVu leis.
|26|Aibreán 2005|Nótaí téacs/líne

## Formáid Comhaid DjVu ##

DjVu documents are IFF85 files. The structure provides a hierarchy of containers which holds information in a DjVu file. These containers are also called “Chunks”. Chunk type and Chunk ID describes how the chunk is used. There is a 4byte header followed by IFF structure. The first four bytes of a DjVu file are 0x41 0x54 0x26 0x54. Pléann an chuid seo na cineálacha éagsúla doiciméad DjVu agus na smuillí comhfhreagracha arb éard atá iontu.


|Aitheantas Tosca|Úsáid
---|---|
|FOIRM|An chéad cheithre beart sonraí den smután FOIRM ar aitheantóir tánaisteach é an smután ilchodach.
|FOIRM:DJVM|Doiciméad illeathanaigh DjVu. Smután ilchodach ina bhfuil an smután DIRM.
|FOIRM:DJVU|Doiciméad DjVu aon leathanach. Smután ilchodach ina bhfuil na smután a dhéanann suas leathanach i ndoiciméad djvu.
| FOIRM:DJVI|Comhad DjVu roinnte” atá san áireamh tríd an smután INCL. Foclóir comhroinnte nótaí agus cruthanna.
|FOIRM:THUM|Sumpa ilchodach ina bhfuil na smután TH44 arb iad na mionsamhlacha leabaithe iad.
|DIRM|Faisnéis faoi ainm leathanaigh le haghaidh doiciméad illeathanaigh.
|NAVM|Faisnéis leabharmharc
|ANTa, ANTz|Anótálacha lena n-áirítear socruithe tosaigh agus hipearnasc forleagtha, boscaí téacs, etc.
|TXTa, TXTz|Faisnéis faoin téacs agus faoin leagan amach Unicode.
|Djbz|Tábla cruthanna comhroinnte.
|Sjbz|BZZ comhbhrú JB2 sonraí bitonal a úsáidtear chun masc a stóráil.
|FG44|Sonraí IW44 a úsáidtear chun tulra a stóráil
|BG44|Sonraí IW44 a úsáidtear chun an cúlra a stóráil
|TH44|Sonraí IW44 a úsáidtear chun íomhánna mionsamhlacha leabaithe a stóráil
|WMRM|Sonraí JB2 riachtanach chun comhartha uisce a bhaint
|FGbz|Sonraí Dath JB2. Soláthraíonn sé dath do gach (blit nó cruth?) sa smután Sjbz comhfhreagrach.
|INFO|Eolas faoin leathanach a DjVu
|INCL|Aitheantas FOIRM san áireamh: smután DJVI.
|BGjp|Cúlra ionchódaithe JPEG
|FGjp|Tulra ionchódaithe JPEG
|Smmr|Masc ionchódaithe G4

### Comhbhrú DJVU

Tá íomhá aonair roinnte ina go leor íomhánna éagsúla, agus ansin tá gach íomhá comhbhrúite ar leithligh. Chun comhad DjVu a chruthú, roinntear an íomhá ar dtús i dtrí íomhá, cúlra, tulra agus masc-íomhá. De ghnáth is íomhánna dathanna le réiteach níos ísle iad na híomhánna cúlra agus tulra; ach is íomhá ardtaifigh í an íomhá masc agus go hiondúil stóráiltear an téacs ann. Tar éis an scaradh, déantar na híomhánna tulra agus cúlra a chomhbhrú trí algartam comhbhrú bunaithe ar thonnlet IW44, agus déantar an íomhá masc a chomhbhrú le modh eile ar a dtugtar JB2.

Cuireann an modh ionchódaithe JB2 deireadh le cuid mhór den iomarcaíocht san íomhá téacs trí chruthanna comhionanna ar an leathanach a aithint, mar shampla tarluithe iolracha de charachtar i gcló ar leith. Cóidíonn JB2 léarscáil ghiotán gach crutha ar leith ar dtús trí leas a bhaint as an iomarcaíocht idir cruthanna comhchosúla. Cóidíonn sé ansin na láithreacha ag a bhfuil gach cruth le feiceáil ar an leathanach. Braitheann JB2 agus IW44 araon ar chineál nua de chódóir uimhríochta dénártha oiriúnaitheach ar a dtugtar an ZP-coder a sháraíonn aon iomarcaíocht atá fágtha laistigh de chúpla faoin gcéad de theorainn na Sionainne. Tá an ZP-coder oiriúnaitheach, agus níos tapúla ná códóirí uimhríochta dénártha eile.

## Tagairtí ##

* [DjVu - Vicipéid](https://ga.wikipedia.org/wiki/DjVu)

* [DjVu File Format](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)

