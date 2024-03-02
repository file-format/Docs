{
  "date": "2019-10-11",
  "keywords": [
"comhad dicom",
"formáid comhaid dicom",
"cad is comhad dicom ann",
"comhad",
"sampla dicom",
"síneadh comhad dicom",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DICOM - Íomháú Digiteach agus Formáid Chomhaid Chumarsáide",
  "description": "Foghlaim faoi fhormáid comhaid DICOM agus APInna ar féidir leo comhaid DICOM a chruthú agus a oscailt.",
  "linktitle": "DICOM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dico-gam"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad DICOM ann?

Is é DICOM an t-acrainm le haghaidh Íomháú Digiteach agus Cumarsáid sa Leigheas agus baineann sé le réimse na Faisnéisíochta Leighis. Úsáidtear DICOM chun feistí íomháithe leighis amhail printéirí, freastalaithe, scanóirí srl ó dhíoltóirí éagsúla a chomhtháthú agus tá sonraí aitheantais gach othar ann freisin le haghaidh uathúlachta. Is féidir comhaid DICOM a roinnt idir dhá pháirtí má tá siad in ann sonraí íomhá a fháil i bhformáid DICOM. Is prótacal ciseal feidhmchlár an chuid cumarsáide de DICOM agus úsáidtear TCP/IP chun cumarsáid a dhéanamh idir eintitis. Is iad na leaganacha a fhaigheann tacaíocht ó sheirbhísí gréasáin ná 1.0, 1.1, 2 nó níos déanaí.

## Stair ##

DICOM was developed jointly by American College of Radiology (ACR) and National Electrical Manufacturers Association (NEMA) for the exchange and viewing of medical images like MRIs, CT scans and ultrasound images. Initially, it was hard to decode the images that the machines produced. Therefore, ACR and NEMA together formed a team in 1983 which released its first standard, ACR/NEMA 300 in 1985. Eisíodh an dara leagan i 1988, rud a bhí níos mó tóir i measc díoltóirí, ach go luath tugadh faoi deara go dteastaíonn feabhsú ar an dara leagan freisin. Eisíodh an 3ú leagan den chaighdeán i 1993 mar DICOM. Is é 3.0 an leagan is déanaí fós ach tá sé nuashonraithe go leanúnach ó 1993 i leith.

## Formáid Chomhaid DICOM ##

Is meascán de shainiú formáid comhaid agus prótacal cumarsáide líonra é DICOM. Úsáideann DICOM an síneadh .DCM. Tá .DCM in dhá fhormáid dhifriúla .i. formáid 1.x agus formáid 2.x. Tá DCM Formáid 1.x ar fáil tuilleadh i dhá leagan gnáth agus leathnaithe. Úsáidtear prótacail HTTP agus HTTPS do sheirbhísí gréasáin DICOM.

### Ceanntásc an Chomhaid ###

I gceanntásc an chomhaid tá 128 beart Réamhfhocal Comhad, agus 4 beart réimír DICOM.

**Brollach # 128 Beart**|** Réimír # 4 Beart D, I, C, M**

Úsáidtear **Brollach** chun rochtain a fháil ar na híomhánna agus ar shonraí eile i gcomhad DICOM a sholáthraíonn comhoiriúnacht le formáidí comhaid íomhá a úsáidtear go coitianta.

Tá an teaghrán DICM mar charachtair chás uachtair sa réimír**.

### Tacar Sonraí ###

Ní mór tacar sonraí amháin a bheith i ngach comhad a léiríonn an t-ásc SOP agus an Aicme SOP le IOD gaolmhar. Is éard is tacar sonraí ann ná faisnéis ón bhfíorshaol a léiriú. Tá eilimintí sonraí sa tacar sonraí agus tá luachanna tréithe an réada sin sna heilimintí sonraí. Sonraítear struchtúr tréithe in IODanna. Is éard atá i réad sonraí DICOM roinnt tréithe, lena n-áirítear míreanna mar ainm, ID, etc., agus freisin tréith speisialta amháin ina bhfuil na sonraí picteilín íomhá.

### Eilimintí Sonraí ###

Is éard atá sa eilimint sonraí ná an eilimint sonraí Clib, fad an luacha agus luach na hEiliminte Sonraí. Tá 5 chineál d’eilimintí Sonraí ann eadhon Eilimintí Sonraí Riachtanach Cineál 1, Eilimintí Sonraí Coinníollacha de Chineál 1C, Eilimintí Sonraí Riachtanacha Cineál 2, Eilimintí Sonraí Coinníollacha Cineál 2C agus Eilimintí Sonraí Roghnacha Cineál 3. Bunúsach Seo a leanas na trí chineál struchtúr eiliminte sonraí.

** Eilimint Sonraí le VR Soiléir**

|Uimhir Ghrúpa|Uimhir na hEiliminte|Uimhir Luacha|Forchoimeádta|Fad Luacha|Réimse Luacha
---|---|---|---|---|---|
|2 Beart|2 Beart|2 Beart|2 Beart # 0x00, 0x00|4 Beart| Bearta Fad Luacha

** Eilimint Sonraí le VR Soiléir**

|Grúpa-Uimhir|Uimhir na hEiliminte|Lionadaíocht Luacha|Fad Luacha|Réimse Luacha
---|---|---|---|---|
|2 Beart|2 Beart|2 Beart|2 Beart|Bearta Fad Luacha

** Eilimint Sonraí le VR intuigthe**


|Uimhir Ghrúpa|Uimhir na hEilime|Fad Luacha|Réimse Luacha
---|---|---|---|
|2 Beart|2 Beart|4 Beart|Bearta Fad Luacha

1. **Clib na hEiliminte Sonraí**: Slánuimhir ordaithe a sheasann don uimhir ghrúpa agus don uimhir dhúil
1. **Luachionadaíocht VR**: Is teaghrán carachtair é VR a léiríonn VR na hEiliminte sonraí.
1. **Fad Luacha**: an seasann sé don tslánuimhir gan síniú fad sainráite an réimse luacha.
1. **Réimse Luacha**: Déantar cur síos ar luachanna na n-eilimintí sonraí.

## Aistrigh Comhréir ##

Is éard atá i gcomhréir aistrithe ná sraith rialacha maidir le hionchódú chun comhréireanna níos teibí a léiriú gan athbhrí. Le cabhair ó chomhréir aistrithe déanann eintitis chumarsáide idirbheartaíocht ar theicnící ionchódaithe coitianta a dtacaíonn siad leo.

## SOPanna ##

Sainmhíníonn Union of IOD agus DIMSE Aicme SOP. Tá na rialacha agus an tséimeantaic sa sainmhíniú ar Aicme SOP a d’fhéadfadh srian a chur ar úsáid na seirbhísí i nGrúpa Seirbhíse DIMSE nó i dTréithe an IOD. Samplaí d’Eilimintí Seirbhíse is ea Stóráil, Faigh, Faigh, Bog, etc. Samplaí d’Oibiachtaí is ea íomhánna CT, íomhánna MR, ach áirítear freisin liostaí sceidil, scuainí priontála, etc.

## Seirbhísí ##

Soláthraíonn DICOM seirbhísí éagsúla, a bhaineann go príomha le cumarsáid sonraí. Déantar cur síos gairid ar gach ceann díobh seo thíos:


**Store:** Seolann seirbhís DICOM Store íomhánna nó réada eile chuig córas cartlannaithe pictiúr agus cumarsáide (PACS) nó freastalaí.


**Tiomantas stórála:** Úsáidtear seirbhís tiomantais stórála le deimhniú go bhfuil íomhá stóráilte go buan ar aon chineál meán.


**Ceist/aisghabh:** Cuireann an tseirbhís seo ar chumas stáisiún oibre liostaí na n-íomhánna nó réada eile a aimsiú agus iad a aisghabháil ansin ó PACS.


**Liosta oibre módúlachta:** Tugann an tseirbhís liosta oibre modhúlachta liosta de nósanna imeachta íomháithe atá sceidealaithe le haghaidh feidhmíochta ag feiste fála íomhá.


**Priontáil:** Seolann an tseirbhís seo íomhánna chuig an printéir.

## Uimhreacha poirt thar IP ##

Úsáideann DICOM na calafoirt TCP agus UDP seo a leanas :

1. 104
1. 2761
1. 2762
1. 11112

## Tagairtí ##

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)

* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)

* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)

* [https://www.dicomlibrary.com/dicom/ ](https://www.dicomlibrary.com/dicom/)


