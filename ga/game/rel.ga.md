{
  "date": "2021-09-08",
  "keywords": [
"comhad rel",
"formáid comhaid rel",
"cad is comhad rel",
"comhad",
"sampla rel",
"síneadh comhad rel",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid REL agus APIs is féidir comhaid REL a chruthú agus a oscailt.",
  "title": "REL - Comhad Modúl In-athshuite",
  "linktitle": "REL",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-re-gal"
}
},
  "lastmod": "2021-09-08"
}

## Cad is comhad REL ann?
Is féidir comhad le síneadh .rel a úsáid chun críocha éagsúla. Mar sin, i dtéarmaí aicmiú cluiche tugtar comhad modúl athlonnaithe air a úsáideann roinnt cluichí Nintendo Wii, mar shampla Brawl, Super Smash Bros agus Mario Kart Wii. Cuimsíonn sé na sonraí gameplay, lena n-áirítear samhlacha carachtar agus céimeanna. Feidhmíonn comhaid REL mar an gcéanna leis na comhaid .DLL a úsáideann Microsoft Windows.

## Formáid comhaid REL saor in aisce,
I bhformáid comhaid REL, roinntear an comhad i roinnt rannóg, grúpáilte de réir a leithéid de rochtain, m.sh. sonraí inléite amháin i rannóg amháin, cuirtear gach cód inrite i gceann eile, srl. Tosaíonn an comhad le rannóg ceanntásca, agus ina dhiaidh sin:
- Tábla ina bhfuil faisnéis alt.
- Na sonraí alt.
- Faisnéis athlonnú.

### Ceanntásc comhaid
Tosaíonn an comhad le ceanntásc suas le 0x4C beart:
| Fritháireamh | Méid | Ainm an Réimse | Cur Síos |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | id | Arbitrary identification number. Must be unique amongst all RELs used by a game. Must not be 0. |
| 0x04 | 4 | seo chugainn | Pointeoir chuig an gcéad mhodúl eile, líonta ag am rite. |
| 0x08 | 4 | roimhe seo | Pointeoir don mhodúl roimhe seo, líonta ag am rite. |
| 0x0c | 4 | uimhreachaRanna | Líon na n-alt sa chomhad. |
| 0×10 | 4 | altInfoOffset | Fritháireamh go dtí tús an tábla rannáin. |
| 0×14 | 4 | ainm Fritháireamh | Fritháireamh go teaghrán ASCII ina bhfuil ainm an mhodúil. D'fhéadfadh a bheith NULLComment. I gcomparáid le tús an chomhaid REL. |
| 0×18 | 4 | ainmMéid | Méid ainm an mhodúil i mbearta. |
| 0x1c | 4 | leagan | Uimhir leagan na formáid comhaid REL. |
| 0×20 | 4 | bsSize | Méid na rannóige '.bss'. |
| 0×24 | 4 | relOffset | Fritháireamh go dtí an tábla athlonnaithe. |
| 0×28 | 4 | fritháireamh | Fritháireamh go tábla imp. |
| 0x2c | 4 | impSize | Méid an tábla IMP i mbeart. |
| 0x30 | 1 | prologSection | Index into section table which prolog is relative to. Skip if this field is 0. |
| 0x31 | 1 | epilogSection | Index into section table which epilog is relative to. Skip if this field is 0. |
| 0x32 | 1 | unresolvedSection | Index into section table which unresolved is relative to. Skip if this field is 0. |
| 0×33 | 1 | bsSection | Innéacs i dtábla na rannóige a bhfuil bss i gcoibhneas leis. Líonta ag am rite! |
| 0×34 | 4 | prolog | Fritháireamh i gcuid sonraithe den fheidhm _prolog. |
| 0×38 | 4 | eipeil | Fritháireamh i gcuid sonraithe den fheidhm _epilog. |
| 0x3c | 4 | gan réiteach | Fritháireamh i gcuid shonraithe den fheidhm _gan réiteach. |
| 0x40 | 4 | align | Version ≥ 2 only. Alignment constraint on all sections, expressed as power of 2. |
| 0x44 | 4 | bssAlign | Version ≥ 2 only. Alignment constraint on all '.bss' section, expressed as power of 2. |
| 0×48 | 4 | deisiúMéid | Leagan ≥ 3 amháin. Má tá REL nasctha le OSLinkFixed (in ionad OSLink), is féidir an spás i ndiaidh an tseolta seo a úsáid chun críocha eile (cosúil le BSS). |

### Tábla Faisnéise na Rannóige
I dtábla faisnéise na rannóige tá iontrálacha **numSections** gach 0x8 beart ar fad:
| Fritháireamh | Méid | Cur Síos |
-------|------------|-------------|
| 0x0 | 30 giotán | Fritháireamh ó thús an REL go dtí an t-alt. Más nialas é seo, is rannán neamhchlóite í an chuid (.i. bss). |
| 0×3.6 | 1 ghiotán | Anaithnid. |
| 0×3.7 | 1 ghiotán | Bratach inrite; más é seo 1 tá an chuid inrite. |
| 0×4 | 4 | Fad i mbearta an ailt. Más é seo náid, ní dhéantar an iontráil seo. |
| 0×8 | An chéad iontráil eile | An chéad iontráil eile |

### Sonraí Athlonnaithe
Is iad na sonraí athlonnaithe liosta amháin nó níos mó de struchtúir beart 0x8. Tá deireadh gach liosta marcáilte leis an gcineál speisialta cód 203:
| Fritháireamh | Ainm | Méid | Cur Síos |
-------|------------|------------|-----|
| 0x0 | fhritháireamh | 2 | Fritháireamh i mbearta ón athlonnú roimhe seo go dtí an ceann seo. Más é seo an chéad athlonnú sa rannóg, tá sé seo i gcoibhneas le tús an rannáin. |
| 0×2 | cineál | 1 | An cineál athlonnaithe. Cur síos air thíos. |
| 0×3 | alt | 1 | An chuid den tsiombail le hathlonnú ina choinne. Maidir leis an gcineál athlonnaithe speisialta 202, is é seo ina ionad sin uimhir na coda sa chomhad seo lena mbaineann na hiontrálacha athlonnaithe seo a leanas. |
| 0×4 | aguisín | 4 | Fritháireamh i mbearta na siombaile le hathlonnú ina gcoinne, i gcoibhneas le tús a rannóige. Is seoladh iomlán é seo le haghaidh athlonnaithe i gcoinne main.dol. |
| 0×8 | An chéad iontráil eile | An chéad iontráil eile | An chéad iontráil eile |


 



## Tagairtí 

* [Formáid Modúil Oibiachta In-athshuite]( https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)



