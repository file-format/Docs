{
  "date": "2019-10-11",
  "keywords": [
"j2k comhad",
"formáid comhaid j2k",
"cad is comhad j2k ann",
"comhad",
"j2k sampla",
"Síneadh comhad j2k",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "J2K",
  "description": "Foghlaim faoi fhormáid comhaid J2K agus APIanna ar féidir leo comhaid J2K a chruthú agus a oscailt.",
  "linktitle": "J2K",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-j2-gak"
}
},
  "lastmod": "2020-08-03"
}

## Cad is comhad J2K ann?

Is íomhá é comhad **J2K** a chomhbhrúitear trí úsáid a bhaint as comhbhrú tonnlet in ionad comhbhrú DCT. Úsáideann Comhghrúpa na Saineolaithe Grianghrafadóireachta (JPEG) 2000 an fhormáid comhaid seo. Stórálann comhaid J2K faisnéis meiteashonraí faoin gcomhad íomhá in XML murab ionann agus .jpeg nó .jpg a úsáideann an fhormáid EXIF chun na críche seo. Tacaíonn comhaid J2K le dath 15-giotán, trédhearcacht alfa, agus comhbhrú gan chailliúint. Tá roinnt APIs tráchtála ann chun íomhánna JPEG 2000 a dhíchódú mar J2K-Codec. Is féidir comhad J2K a oscailt ar Windows OS ag baint úsáide as an lucht féachana íomhá caighdeánach.

## Formáid Chomhaid J2K ##

Tá formáid comhaid J2K mar an gcéanna le formáid JPEG 2000 a shábháiltear go minic mar .jp2 agus .jpc. Fágann sin go leanann comhaid J2K an cur chuige céanna maidir le meiteashonraí a ionchódú i bhformáid XML ina n-úsáidtear an Caighdeán 12234-1 mar thagairt idir na clibeanna Exif agus na comhpháirteanna XML. Déantar é a fheabhsú tuilleadh le síneadh JPEG 2000 cuid-2 a chomhcheanglaíonn an mheicníocht beochana agus cumraíochtaí srutha cód in aon íomhá amháin. Sábháltar a leithéid de chomhaid leathnaithe i bhformáid comhaid mar .jpx.

### Leagan amach Comhad JPEG2000 ###

Tacaíonn JPEG2000 le héagsúlacht feidhmchlár atá bunaithe ar chomhlíonadh formáidí comhaid sínte. Cé gur féidir íomhá amháin a bheith sa chineál is simplí, is féidir sraith íomhánna a áireamh i gcineálacha níos casta, atá cruachta ar bharr a chéile nó in ord ama-bhunaithe.

#### Bosca JP2 ####
Is é bloc tógála barrleibhéil an fhormáid comhaid JP2 agus tá réimsí cineáil agus faid sa cheanntásc, agus secton sonraí. Is é an cineál bosca is suntasaí ná an bosca srutha cód atá tadhlach. Stórálann an bosca seo ina chuid sonraí an sruth cód JPEG2000.

#### JPEG2000 Sruth Cód ####

Is seicheamh beart é an JPEG2000 CodeStream a theastaíonn chun íomhá comhbhrúite JPEG2000 a dhíchódú. Sa chás nach bhfuil aon rud eile sa chomhad seachas an sruth cód seo, tugtar comhad srutha cód amh air. De ghnáth is éard is sruth cód JPEG ann ná algartam comhbhrú JPEG2000 a chur i bhfeidhm ar íomhá, cé nach é an t-aon bhealach é.

#### Páirteanna Tíleanna ####

Is éard is íomhá ionchódaithe JPEG2000 ann ná bailiúchán aonad sonraí ar a dtugtar paicéid. Coinnítear na paicéid seo sa sruth cód laistigh de ghrúpaí paicéad ar a dtugtar tíl-pháirteanna. Sula ndéantar íomhá a ionchódú, déanann an t-ionchódóir an íomhá a roinnt ina ghreille dronuilleogach de bhloic, ar a dtugtar tíleanna ina bhfuil gach tíl ionchódaithe ar leithligh beag beann ar tíleanna eile.

{{< figure src="../JPEG2000_Codestream.png" alt="Formáid Comhaid JPEG2000" >}}

## Comhbhrú J2K ##
Úsáideann JPEG 2000 teicneolaíocht comhbhrú tonnchosc rud a fhágann go bhfuil sé go tapa bunaithe ar an bhfíric gur beag picteilín a thaispeántar i cibé radharc nó fuinneog a thaispeánann an t-amharcóir an íomhá. Is féidir béim a leagan air seo toisc nach mbeidh ach cúpla meigeavata picteilín le feiceáil ar an scáileán le haghaidh íomhánna méid an-mhór (i ghigibheart). Cuidíonn sé seo leis an gcuid sin de shonraí na híomhá a theastaíonn chun na picteilíní taispeána a líonadh agus a thabhairt go tapa. Éilíonn sé seo freisin teicneolaíocht dí-chomhbhrú ardluais chun an mheicníocht um ghabháil íomhánna a bhrostú chun na híomhánna a theastaíonn ar an eitilt a chruthú.

Baineann J2K leas as dí-chomhbhrú tapa agus ní fhaigheann sé ach faisnéis riachtanach le haghaidh sonraí picteilín chun cuid d’íomhánna infheicthe a sholáthar go tapa ar na scáileáin. Tá J2K deartha go príomha chun sonraí a fheiceáil agus gan eagarthóireacht a dhéanamh orthu.

## Aitheantas J2K ##
Tá bearta sínithe 6A 50 20 20 ag comhaid JPEG 2000.

### Cineálacha Mím ###
Áirítear le Cineálacha Míme Cláraithe do chomhaid JPEG 2000:
  * íomhá/jp2
  * íomhá/jpx
  * íomhá/jpm
  * físeán/mj2

## Feabhsuithe thar an gcaighdeán JPEG ##
I measc na bhfeabhsuithe thar an gcaighdeán JPEG tá:
  * Feidhmíocht comhbhrú níos fearr
  * Léiriú réitigh iolracha
  * Tarchur forásach ag picteilín agus cruinneas réitigh
  * Rogha comhbhrú lossless nó lossy
  * Athléimneacht earráide, formáid comhaid solúbtha
  * Tacaíocht raon ard dinimiciúil
  * Eolas spásúil cainéal taoibh

## Tagairtí ##
  * [Taubman, David; Marcellin, Michael (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

