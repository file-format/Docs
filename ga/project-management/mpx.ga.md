{
  "date": "2019-10-11",
  "keywords": [
"comhad mpx",
"Formáid comhaid mpx",
"Cad é an comhad mpx",
"comhad",
"sampla mpx",
"Síneadh comhad mpx",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MPX - Formáid Comhaid Malartú Tionscadal Microsoft",
  "description": "Foghlaim faoi fhormáid comhaid MPX agus APIs is féidir comhaid MPX a chruthú agus a oscailt.",
  "linktitle": "MPX",
  "menu": {
    "docs": {
      "parent": "project-management",
      "identifier": "project-management-mp-gax"
}
},
  "lastmod": "2021-05-07"
}

## Cad is comhad MPX ann? ##

Is Formáid Chomhaid Microsoft Exchange é comhad le síneadh .mpx. D'fhorbair Microsoft Project (MSP) formáid comhaid MPX chun malartú faisnéise tionscadail a éascú idir BPA agus feidhmchláir eile a thacaíonn le formáid comhaid MPX, lena n-áirítear Primavera Project Planner, Sciforma, agus Timerline Precision Extimating. Ag baint úsáide as na comhaid MPX, is féidir leat gach cineál faisnéise a aistriú ó thionscadal go córas difriúil, mar shampla faisnéis mhionsonraithe sannadh acmhainne, faisnéis fhéilire, nó faisnéis ón mbosca dialóige Tionscadal Info.

Microsoft Project 4.0 introduced support for creating and reading MPX file formats that continued to be used through Microsoft Project 98. Mar sin féin, tá deireadh le scaoileadh Microsoft Project 2000 le tacaíocht do chomhaid MPX a chruthú, agus ní thacaíonn na leaganacha go dtí Microsoft Project 2010 ach le léamh MPX. Ní thacaítear le formáid comhaid MPX i leaganacha níos déanaí ná BPA 2010.

## Formáid Chomhaid MPX ##

Tugtar forbhreathnú ar na sonraíochtaí comhaid MPX sa chuid seo. Is féidir sonraíochtaí iomlána a fháil san alt [Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) seo agus is féidir iad a tharchur le haghaidh sonraí.

### Taifid ###

Is éard atá i dTaifead den chomhad MPX faisnéis don tionscadal. Tá cineálacha éagsúla taifead ann ina bhfuil a ord féin ag gach taifead. Aithnítear gach cineál taifid trína uimhir thaifid. Le haghaidh comhad MPX, ní mór an cineál taifid Cruthú Comhad a bheith ann. Níl cineálacha eile taifead éigeantach. Taispeánann an tábla seo a leanas na cineálacha taifead go léir, a n-uimhreacha taifead, agus an líon taifead a fhéadfaidh a bheith i ngach cineál sa chomhad MPX. Caithfidh cuimsiú taifead sa chomhad MPX an t-ord tábla a leanúint, agus tuairimí a chur isteach áit ar bith.

|Ainm Taifid|Uimhir Thaifid|Uastalíon Taifead
---|---|---|
|Cruthú Comhad (riachtanach)|níl ar bith|1
|Socruithe Airgeadra|10|1
|Socruithe Réamhshocraithe|11|1
|Socruithe Dáta agus Ama|12|1
|Bunfhéilire Sainmhíniú|20|250
|Bunuaireanta Féilire|25| 7 in aghaidh an taifead Bonn Féilire Sainmhíniú
|Eisceacht Bonnfhéilire|26| 250 in aghaidh an taifead Bonn Féilire Sainmhíniú
|Ceanntásc an Tionscadail|30|1
|Sainmhíniú ar an Tábla Acmhainne Téacs|140|1- (Nó is féidir leat taifead sainmhínithe Tábla Acmhainne Uimhriúil a úsáid)
|Tábla Acmhainní Uimhriúil Sainmhíniú|41|1
|Acmhainn|50|9,999
|Nótaí Acmhainne|51| 1 in aghaidh an taifid Acmhainní
|Sainmhíniú ar Fhéilire Acmhainní|55| 1 in aghaidh an taifid Acmhainní
|Uaireanta Féilire Acmhainní|56| 7 in aghaidh an Fhéilire Acmhainní
|Eisceacht an Fhéilire Acmhainní| 57|250 in aghaidh an Fhéilire Acmhainní
|Sainmhíniú ar an Tábla Tasc Téacs|60|1 (Nó is féidir leat an taifead Sainmhínithe Tábla Tasc Uimhriúil a úsáid)
|Sainiú Tábla Tasc Uimhriúil|61|1
|Tasc|70|9
|Nótaí Tasc|71| 1 in aghaidh taifead Tasc
|Tasc Athfhillteach|72| 1 in aghaidh taifead Tasc
|Tasc Acmhainne|75| 100 in aghaidh an taifead Tasc
|Réimsí an Ghrúpa Oibre Sannacháin|76| 1 in aghaidh an taifid Sannta
|Ainmneacha an Tionscadail|80|500
|Naisc Cliant DDE agus OLE|81|500
|Nótaí|0|gan teorainn

### Struchtúr Comhad ###

Is éard atá i gcomhad MPX ná taifid a luaitear thuas atá socraithe ar bhealach réamhshocraithe laistigh den chomhad. Pléitear sonraí faoi na cineálacha taifead seo mar seo a leanas:

**Taifead Cruthaithe Comhad (FCR):** Is taifead éigeantach é seo a bhfuil sé mar chuspóir aige na:

* Formáid comhaid (MPX)

* Carachtar deighilteoir Liosta a úsáidtear sa chomhad

* Clár agus uimhir leagain a úsáideadh chun an comhad a chruthú

* Uimhir leagan na formáid comhaid MPX a úsáidtear sa chomhad

* Leathanach cód a úsáidtear chun an comhad a chruthú


Caithfidh gurb é seo an chéad taifead sa chomhad. Agus é ag onnmhairiú ó Microsoft Project, sonraítear an carachtar deighilteoir liosta sa mhír Socruithe Réigiúnacha i bPainéal Rialúcháin Windows. Cuimsíonn Taifead FCR na réimsí seo a leanas:

* MPX ina dhiaidh láithreach ag an carachtar deighilteoir liosta

* Ainm an Chláir/Aitheantóir

* Leagan Uimhir an chomhaid

* Leathanach an Chóid (850, 437, MAC, ANSI)


Mar shampla, is féidir faisnéis **MPX, Microsoft Project, 3.0** a bheith sa taifead a shonraíonn go n-úsáidtear camóg mar charachtar deighilteoir liosta sa chomhad MPX seo. Easpórtáiltear an leagan den fhormáid MPX a úsáidtear sa chomhad ó Microsoft Project leagan 3.0.

**Socruithe Airgeadra** Sonraíonn an taifead seo, agus an uimhir is airde riamh 10 aige, socruithe do na roghanna airgeadra sa bhosca dialóige Roghanna. Mura bhfuil an taifead seo san áireamh, úsáidtear na socruithe reatha sa bhosca dialóige Roghanna. Sonraítear na Deighilteoirí Mílte agus Deachúla sa mhír Socruithe Réigiúnacha i bPainéal Rialaithe Windows.
Is iad na réimsí atá san áireamh sa taifead seo:

* Siombail Airgeadra

* Seasamh Siombail (0 # i ndiaidh, 1 # roimhe sin, 2 # i ndiaidh le spás, 3 # roimhe sin le spás)

* Digití Airgeadra (0,1,2)

* Na mílte deighilteoir

* Deighilteoir Deachúil


**Sampla:** 10,$,1,2,,,.
Sonraíonn an sampla seo go n-áirítear i luachanna airgeadra comhartha dollar ($) os a gcomhair, go n-áirítear dhá dhigit tar éis an phointe deachúil, go n-úsáidtear camóg chun na mílte a scaradh, agus go n-úsáidtear tréimhse mar phointe deachúil. Toisc go bhfuil an carachtar deighilteoir liosta san áireamh i réimse na Mílte Deighilteoir, tá an réimse timpeallaithe ag comharthaí athfhriotail.

**Socruithe Réamhshocraithe:** Sonraíonn an taifead seo, agus uimhir thaifid 11 aige, socruithe do na roghanna réamhshocraithe sa bhosca dialóige Roghanna. Mura sonraítear ré, ní mór an tAonad Réamhshocraithe Aga a shocrú chun aonaid ré a áireamh i gceart. Mura bhfuil an taifead seo san áireamh, úsáidtear na socruithe reatha sa bhosca dialóige Roghanna.
Is iad na réimsí atá san áireamh sa taifead seo:

* Aonaid Aga Réamhshocraithe (0 # nóiméad, 1 # uair, 2 # lá, 3 # seachtaine)

* Cineál Réamhshocraithe Fad (0 # gan a bheith socraithe, 1 # socraithe)

* Aonaid Réamhshocraithe Oibre (0 # nóiméad, 1 # uair, 2 # lá, 3 # seachtaine)

* Réamhshocrú Uaireanta / Lá

* Uaireanta/Seachtain Réamhshocraithe

* Ráta Caighdeánach Réamhshocraithe

* Ráta Réamhshocraithe Ragoibre

* Stádas Acmhainne Nuashonraithe ar Stádas Tasc (0 # níl, 1 # tá)

* Tascanna Scoilte atá ar siúl (0 # níl, 1 # tá)


**Date and Time Settings:** This record, having record number 12, specify settings for the date and time options in the Options dialog box, and the Bar Text Date Format option in the Layout dialog box. If this record is not included, the current settings in the Options dialog box are used.
\\Is iad na réimsí atá san áireamh sa taifead seo:

* Ordú Dáta (0 # mí/lá/bliain, 1 # lá/mí/bliain, 2 # bliain/mí/lá)

* Formáid Ama (0 # 12 uair, 1 # 24 uair)

* Am Réamhshocraithe (líon nóiméad tar éis meán oíche)

* Deighilteoir Dáta

* Deighilteoir Ama

* 0:00 go 11:59 Téacs

* 12:00 go 23:59 Téacs

* Formáid Dáta (0 -14)*

* Barra Téacs Formáid Dáta (0 -194)*


**Sainmhíniú ar an mBonnfhéilire:** Sainíonn na taifid seo, a bhfuil an uimhir is airde riamh acu 20, bunfhéilirí agus a laethanta oibre agus a laethanta oibre den tseachtain. Úsáidtear na socruithe réamhshocraithe mura bhfuil aon iontráil ar feadh lae. Is iad na socruithe réamhshocraithe ná Luan go hAoine le haghaidh laethanta oibre agus Dé Sathairn agus Dé Domhnaigh do laethanta nach laethanta oibre. Sa taifead seo, tá an réimse Ainm ag teastáil. I gcás gach ceann de na laethanta, léiríonn iontráil 0 gur lá neamh-oibre é an lá, agus léiríonn iontráil 1 gur lá oibre é an lá.
Is iad na réimsí atá san áireamh sa taifead seo:

* Ainm

* Domhnach

* Dé Luain

* Dé Máirt

* Dé Céadaoin

* Déardaoin

* Dé hAoine

* Dé Sathairn


**Bunuaireanta Féilire:** Sonraíonn na taifid seo, agus an uimhir thaifid 25 acu, na huaireanta oibre do laethanta na seachtaine má tá siad difriúil leis na socruithe réamhshocraithe. Is iad na huaireanta oibre réamhshocraithe ná 8:00 AM go 12:00 PM agus 1:00 PM go 5:00 PM Tagraíonn gach taifead Bonnuaireanta Féilire don taifead Base Calendar Definition roimhe seo. Is féidir le suas le seacht gcinn de na taifid seo gach taifead Bonnfhéilire Sainmhíniú a leanúint.

* Lá na Seachtaine (1 - 7, áit a bhfuil 1 # Domhnach agus 7 # Satharn)

* Ó Am 1

* Go Am 1

* Ó Am 2

* Go Am 2

* Ó Am 3

* Go Am 3


**Eisceacht Bonnfhéilire:** Sainmhíníonn na taifid seo, a bhfuil taifead uimhir 26 orthu, na heisceachtaí ó na laethanta agus na huaireanta a sonraíodh sa dá chineál taifid roimhe seo. Is féidir le suas le 250 de na taifid seo gach taifead Sainmhínithe Bonnfhéilire a leanúint. Ní mór na taifid seo a liostú in ord croineolaíoch. Más eisceacht lá amháin, féadfaidh tú an réimse To Date a fhágáil folamh. Mura gcuirtear aon amanna in iúl, úsáidtear na hamanna réamhshocraithe ó 8:00 AM go 12:00 PM agus 1:00 PM go 5:00 PM.
Is iad na réimsí atá san áireamh sa taifead seo:

* Ón Dáta

* Go dtí seo

* Neamh-oibre/Ní oibríonn (0 # neamh-oibre, 1 # ag obair)

* Ó Am 1

* Go Am 1

* Ó Am 2

* Go Am 2

* Ó Am 3

* Go Am 3


**Project Header:** This record, having record value 30,  sets global project fields, such as the project start date and project finish date. The fields in this record correspond to the information in the Project Info and Statistics dialog boxes.
Is iad na réimsí agus na cluaisíní atá san áireamh sa taifead seo:

* Tionscadal tab

* Cuideachta

* Bainisteoir

* Féilire (Caighdeánach in úsáid mura bhfuil aon iontráil ann)

* Dáta Tosaigh (ríomhtar an réimse seo nó an chéad réimse eile do chomhad iompórtáilte, ag brath ar an socrú Sceidil Ón)

* Dáta Críochnaithe

* Sceideal Ó (0 # tús, 1 # chríochnú)

*Dáta Reatha*

* Tuairimí

* Costas

* Costas Bunlíne

* Costas Iarbhír

* Obair

* Obair Bhunlíne

* Obair Iarbhír

* Obair

*Fad*

*Aga Bunlíne*

* Ré Iarbhír

* Céatadán Críochnaithe

* Tosaigh Bunlíne

* Críochnaigh Bunlíne

* Tús Iarbhír

* Críoch Iarbhír

* Athraitheas Tosaigh

* Críochnaigh Athraitheas

* Ábhar

* Údar

* Eochairfhocail


**Tábla Acmhainne Téacs Sainmhíniú**: Liostaítear sa taifead seo na réimsí acmhainne, in ord, atá á n-iompórtáil nó á n-easpórtáil. Maidir le comhaid iompórtáilte, ní mór go mbeadh na hainmneacha ag teacht leis na hainmneacha páirce a úsáidtear i Microsoft Project. Maidir le comhaid easpórtáilte, tagann an taifead seo ón tábla Easpórtála acmhainne. Ní mór an taifead seo nó taifead sainmhínithe Tábla Acmhainne Uimhriúil a úsáid. Nuair a bhíonn an dá thaifead seo á n-onnmhairiú ó Microsoft Project, cuirtear san áireamh iad.

**Tábla Acmhainne Uimhriúil Sainmhíniú:** Ag baint úsáide as uimhreacha seachas ainmneacha, liostaíonn an taifead seo na réimsí acmhainne, in ord, atá á n-iompórtáil nó á n-easpórtáil. Is modh malartach é seo chun na réimsí acmhainne atá san áireamh i ngach taifead Acmhainne a shainaithint agus tá sé úsáideach nuair a bhíonn comhad MPX cruthaithe ag táirge i dteanga iasachta á shainiú.

**Acmhainn:** Sna taifid seo tá an fhaisnéis maidir le gach acmhainn atá á hiompórtáil nó á heaspórtáil. Déanann gach taifead Áis cur síos ar acmhainn amháin. Nuair a iompórtálann tú faisnéis, sainmhínítear na réimsí a chuimsítear leis an taifead Sainmhíniú Tábla Acmhainne Téacs nó taifead Sainmhíniú Tábla Acmhainne Uimhriúil. Nuair a easpórtálann tú faisnéis, is iad na réimsí atá san áireamh na cinn atá liostaithe sa tábla Easpórtála acmhainne.

**Nótaí Acmhainní:** Sna taifid seo tá nótaí faoin taifead Acmhainní díreach roimhe seo. Le haghaidh líne nua laistigh den nóta, úsáidtear carachtar ASCII 127. Má tá an carachtar deighilteora liosta san áireamh sa nóta, cuir an nóta faoi iamh i gcomharthaí athfhriotail.

**Sainmhíniú ar an bhFéilire Acmhainní:** Sainmhíníonn na taifid seo na laethanta oibre don acmhainn atá sonraithe sa taifead Acmhainní díreach roimhe seo. Maidir le comhaid iompórtáilte, mura bhfuil aon iontráil ann don réimse Ainm Bonn Féilire, úsáidtear Standard. Ní thugann aon iontráil don lá sonrach le fios go bhfuil an lá socraithe don réamhshocrú (2). Mura bhfuil aon taifid Sainmhíniú ar Fhéilire Acmhainní, úsáidtear Standard mar bhunfhéilire na hacmhainne, agus úsáidtear réamhshocraithe do na laethanta. I gcás gach ceann de na laethanta, léiríonn iontráil 0 gur lá neamh-oibre é an lá, léiríonn 1 gur lá oibre é an lá, agus sonraíonn 2 go n-úsáidtear an réamhshocrú.

**Uaireanta Féilire Acmhainní:** Sainmhíníonn na taifid seo na huaireanta oibre don acmhainn atá éagsúil leis an bhféilire bonn a úsáideann an acmhainn. Baineann na taifid seo leis an taifead Sainmhíniú Féilire Acmhainní díreach roimh an taifead seo. Is féidir le suas le seacht gcinn de na taifid seo gach taifead Sainmhíniú ar Fhéilire Acmhainní a leanúint.

**Eisceacht an Fhéilire Acmhainní:** Sainmhíníonn na taifid seo na heisceachtaí ó na laethanta agus na huaireanta a shonraítear sa dá chineál taifid roimhe seo. Féadfaidh suas le 250 de na taifid seo gach taifead Sainmhíniú ar Fhéilire Acmhainní a leanúint. Ní mór na taifid seo a liostú in ord croineolaíoch. Mura bhfuil sa eisceacht ach lá amháin, féadfaidh tú an réimse To Date a fhágáil folamh. Mura gcuirtear aon amanna in iúl, úsáidtear na hamanna réamhshocraithe ó 8:00 AM go 12:00 PM agus 1:00 PM go 5:00 PM.

**Text Task Table Definition:** This record lists the task fields, in order, that are being imported or exported. For imported files, the names must match the field names used in Microsoft Project. If the file is being exported, this record comes from the task Export table. When exporting from Microsoft Project, both of these records are included. Fields that are calculated by Microsoft Project, such as Scheduled Start and Scheduled Finish, are ignored if imported. If you have task start or finish dates that are fixed, use the Constraint Type and Constraint Date fields.

**Sainmhíniú Tábla Tasc Uimhriúil:** Ag baint úsáide as uimhreacha seachas ainmneacha, liostaíonn an taifead seo na réimsí tascanna, in ord, atá á n-iompórtáil nó á n-easpórtáil. Is modh malartach é seo chun na réimsí tascanna a chuimsítear i ngach taifead Tasc a shainaithint agus tá sé úsáideach nuair a bhíonn comhad MPX cruthaithe ag táirge i dteanga iasachta á shainiú.

**Tasc:** Sna taifid seo tá an fhaisnéis maidir le gach tasc atá á iompórtáil nó á onnmhairiú. Déanann gach taifead Tasc cur síos ar thasc amháin. Nuair a iompórtálann tú faisnéis, sainmhínítear na réimsí atá san áireamh leis an taifead Sainmhíniú Tábla Tasc Téacs nó an taifead Sainmhínithe Tábla Tasc Uimhriúil. Nuair a easpórtálann tú faisnéis, is iad na réimsí atá san áireamh na cinn atá liostaithe sa tábla Easpórtála Tasc.

**Nótaí Tasc:** Tá nótaí ar thaifead an Tasc díreach roimhe seo sna taifid seo. Úsáid carachtar ASCII 127 chun líne nua laistigh den nóta a léiriú. Má tá an carachtar deighilteora liosta san áireamh sa nóta, cuir an nóta faoi iamh i gcomharthaí athfhriotail.

**Tasc Acmhainne**: Liostaíonn na taifid seo faisnéis faoi na hacmhainní a sannadh don tasc a bhí sainithe i dtaifead an Tasc roimhe seo. Má tá comhaid á gcumasc agat agus má theastaíonn uait go gcoinneofaí faisnéis sannadh acmhainne, ní mór duit an fhaisnéis a chur san áireamh sa chomhad MPX. Má chumasc tú, scriosfar gach tasc atá ann cheana féin ar thascanna cumaisc. Má tá tú ag cumasc comhaid atá bunaithe ar Aitheantais Uathúla, sanntar acmhainní trí úsáid a bhaint as Aitheantais Acmhainne Uathúla seachas IDanna.

**Resource Assignment Workgroup Fields:** These records list the information that is stored with each assignment for the Workgroup features of Microsoft Project 4.0 and 4.1. Má úsáideann tú na gnéithe Grúpa Oibre, ní mór duit an taifead seo a chur san áireamh lena chinntiú nach gcailltear aon chuid den fhaisnéis.

**Ainmneacha an Tionscadail:** Liostaíonn na taifid seo na naisc DDE go léir atá stóráilte sa tionscadal.

**Naisc Cliant DDE agus OLE:** Liostaíonn na taifid seo naisc DDE leis an tionscadal.

**Tuairimí:** Is féidir na taifid seo a úsáid chun tuairimí a chur leis an gcomhad agus is féidir iad a thaispeáint in aon áit sa chomhad. Ní mór tús a chur le gach taifead Tráchta le 0.

## Fadhbanna le comhad MPX a oscailt ##

Seo liosta de roinnt saincheisteanna coitianta a d’fhéadfadh teacht chun cinn agus a d’fhéadfadh a bheith ina gcúis le mífheidhmiú formáid MPX:

 *   Neamhláithreacht bogearraí tacaíochta
 *   Comhad truaillithe
 *   Comhad ionfhabhtaithe de bharr víreas
 *   Níl aon cheart rochtana sa chóras chun na comhaid a oscailt
 *   Tiomántán as dáta i do chóras
 *   Athainmnítear síneadh an chomhaid

## Tagairtí ##

* [MPX - Microsoft Knowledge Base]( https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)


