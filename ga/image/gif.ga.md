{
  "date": "2019-10-11",
  "keywords": [
"comhad gif",
"Formáid comhaid gif",
"Cad is comhad gif ann",
"comhad",
"sampla gif",
"Síneadh comhad gif",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GIF - Formáid Comhad Íomhá",
  "description": "Foghlaim faoi fhormáid comhaid GIF agus APIs ar féidir leo comhaid GIF a chruthú agus a oscailt.",
  "linktitle": "GIF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-gi-gaf"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad GIF ann? ##

Is cineál íomhá ard-chomhbhrúite é GIF nó Formáid Acomhal Grafach. Is leis Unisys é, úsáideann GIF algartam comhbhrú LZW nach ndéanann díghrádú ar cháilíocht na híomhá. Ceadaítear suas le 8 ngiotán in aghaidh na picteilín de ghnáth le GIF do gach íomhá agus ceadaítear suas le 256 dathanna trasna na híomhá. I gcodarsnacht le híomhá [JPEG](/image/jpeg/), ar féidir léi suas le 16 milliún dathanna a thaispeáint agus a bhaineann go cothrom le teorainneacha na súl daonna. Ar ais nuair a tháinig an t-idirlíon chun cinn, ba iad na GIFanna an rogha is fearr i gcónaí mar go raibh bandaleithead íseal ag teastáil uathu agus iad comhoiriúnach do na grafaicí a ídíonn réimsí soladacha datha. Comhcheanglaíonn GIF beoite go leor íomhánna nó frámaí in aon chomhad amháin agus taispeánann sé iad i seicheamh chun gearrthóg beoite nó físeán gearr a ghiniúint. Is iad na teorainneacha datha suas le 256 do gach fráma agus is dócha gurb iad na cinn is lú oiriúnach chun íomhánna agus grianghraif eile a atáirgeadh le grádán datha.

## Formáid Chomhaid GIF ##

Go coincheapúil, tá limistéar grafach seasta de mhéid ag comhaid GIF líonta le nialas nó níos mó íomhánna. Roinneann roinnt comhaid GIF an t-achar grafach seasta nó bloic ina bhfo-íomhánna atá in ann feidhmiú mar fhrámaí beoite i gcás GIF beoite. Úsáideann an fhormáid GIF an doimhneacht picteilín de 1 go 8 giotán chun na sonraí léarscáil ghiotán a stóráil. Úsáidtear samhail dath RGB agus sonraí pailéad i gcónaí chun na híomhánna a stóráil. Ag brath ar an leagan, sainmhíníonn ceanntásc ar fhad sheasta (GIF87a nó GIF89a) tús gnáthchomhad GIF.

Faoi láthair, tá dhá leagan de GIF: 87a agus 89a ar fáil. Is é an chéad fhormáid GIF bunaidh agus is é an dara ceann an fhormáid GIF nua. San fhormáid comhaid seo, luaitear saintréithe na mbloc agus na toisí picteilín i dTuairisceoir Scáileán Loighciúil fad fosaithe. Féadfaidh an tuairisceoir scáileáin a bheith ann agus méid an Tábla Dathanna Domhanda a shonrú, a rianaíonn sonraí breise más ann dóibh. Is é an leantóir an beart deireanach den chomhad ina bhfuil beart amháin de leathstad ASCII. Seo a leanas leagan amach tipiciúil comhaid GIF87a:

### Ceanntásc ###

Coinníonn an Ceanntásc sé beart agus úsáidtear é chun an cineál comhaid a shonrú mar GIF. Cé go bhfuil an Tuairisceoir Scáileáin Loighciúil scartha ón gceanntásc iarbhír ach uaireanta meastar é mar an dara ceanntásc. Féadfaidh an struchtúr céanna a úsáidtear chun an ceanntásc a stóráil an Tuairisceoir Scáileáin Loighciúil a stóráil. Tosaíonn gach comhad GIF leis an síniú 3-beart agus úsáideann na carachtair GIF” mar aitheantóir. Tá an leagan freisin trí bytes i méid agus dearbhaíonn an leagan den chomhad GIF.

### Tuairisceoir Scáileáin Loighciúil ###

Sonraíonn Tuairisceoir Íomhá fad seasta an fhaisnéis scáileáin agus dath atá riachtanach chun íomhá GIF a chruthú. Tá an luach is lú de réiteach scáileáin faoi iamh sna réimsí Airde agus Leithead, rud atá éigeantach na sonraí íomhá a thaispeáint. Mura bhfuil an gléas taispeána in ann an taifeach sonraithe a thaispeáint, beidh gá le scálaiú chun an íomhá a thaispeáint go cuí. Taispeántar Faisnéis Léarscáile Scáileáin agus Dathanna sna ceithre fho-réimse den tábla thíos (cé is é giotán 0 an giotán is lú suntasaí):


|Giotán | Fo-réimsí
---|---|
|0-2|Méid an Tábla Dathanna Domhanda
|3|Brat Sórtála Tábla Dathanna
|4-6|Taifeach Datha
|7|Bratach Tábla Dathanna Domhanda

#### Tábla Dathanna Domhanda ####

Cuirtear Tábla Dathanna Domhanda roghnach díreach tar éis an Tuairisceora Scáileáin Loighciúil. Mapáil an tábla seo chun na sonraí dath picteilín taobh istigh de na sonraí íomhá a innéacsú. In éagmais Tábla Dathanna Domhanda, úsáideann gach íomhá sa chomhad GIF a Dath Áitiúil. Is fearr tábla dathanna réamhshocraithe a sholáthar má tá Tábla Dathanna Domhanda agus Áitiúil ar iarraidh. Comhdhéanann sraith de thríbheart trí bheart gnéithe an tábla datha. Tá luach datha RGB mar thréith ag gach beart. Úsáidtear na dathanna dearg, glas agus gorm mar luachanna gach eilimint tábla datha. Buaileann na hiontrálacha sa Tábla Dathanna Domhanda uasmhéid de 256 iontráil agus seasann siad i gcumhacht dhá cheann i gcónaí.

#### Sonraí Íomhá ####

Stórálann sonraí na híomhá beart de shiombailí neamhchódaithe agus ina dhiaidh sin liosta nasctha fo- mar aon leis na sonraí ionchódaithe LZW.

#### leantóir ####

Léiríonn leantóir beart amháin de shonraí arb é an carachtar deiridh sa chomhad é. Is é luach an bhirt seo go buan ná 3Bh agus sonraíonn sé deireadh an tsrutha sonraí. Caithfidh an leantóir a bheith ag gach comhad GIF sa cheann deireanach de gach comhad.

## Tagairtí ##

* [Formáid comhaid GIF]( https://en.wikipedia.org/wiki/GIF)


