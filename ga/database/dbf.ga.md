{
  "date": "2021-06-15",
  "keywords": [
"DBF",
"síneadh",
"comhad dbf",
"Formáid comhaid dbf",
"Cineál Comhaid Bunachar Sonraí",
"Formáid Comhaid Bunachar Sonraí",
"Cad is comhad dbf ann",
"dBASE"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid DBF agus APIs ar féidir leo comhaid DBF a chruthú agus a oscailt.",
  "title": "DBF - Comhad Bunachar Sonraí dBase",
  "linktitle": "DBF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-db-gaf"
}
},
  "lastmod": "2021-06-15"
}

## Cad is comhad DBF ann?
The file with .dbf extension is a database file used by a database management system application called **dBASE**. Inititally, the dBASE database was named as Project Vulcan; started by **Wayne Ratliff** in 1978. Tugadh an cineál comhaid DBF isteach le dBASE II i 1983. Socraíonn sé taifid sonraí iolracha le réimsí de chineál Array. Na bogearraí bunachar sonraí **xBase** atá coitianta mar gheall ar a chomhoiriúnacht le raon leathan formáidí comhaid; Tacaíonn na comhaid DBF freisin.

## Formáid Comhaid DBF
Baineann formáid comhaid DBF le córas bainistíochta bunachar sonraí dBASE ach d’fhéadfadh sé a bheith comhoiriúnach le xBase nó le bogearraí DBMS eile. Is éard a bhí sa leagan tosaigh den chomhad dbf ná tábla simplí ina bhféadfaí sonraí a chur leis, a mhodhnú, a scriosadh nó a phriontáil ag baint úsáide as an tacar carachtar ASCII. Le himeacht ama feabhsaíodh .dbf, agus cuireadh comhaid bhreise leis chun gnéithe agus cumais an chórais bhunachair sonraí a mhéadú.

I dBASE nua-aimseartha tá comhad DBF comhdhéanta de cheanntásc, na taifid sonraí, agus an marcóir EOF (Deireadh Comhaid).

- Tá faisnéis faoin gcomhad sa cheanntásc, amhail líon na dtaifead agus líon na gcineálacha réimsí a úsáidtear sna taifid.
- Tá na sonraí iarbhír sna taifid.
- Tá beart amháin marcáilte ag deireadh an chomhaid, dar luach 0x1A.

### Ceanntásc comhaid
Tugtar leagan amach ceanntásc an chomhaid in dBase sa tábla seo a leanas:

| Beart | Clár | Brí |
---|---|---|
| 0 | 1 beart | DBASE bailí do chomhad DOS; léiríonn giotán 0–2 uimhir leagain, léiríonn giotán 3 láithreacht dBASE do chomhad meamraim DOS, léiríonn giotán 4–6 láithreacht tábla SQL, léiríonn giotán 7 láithreacht aon chomhad meamraim (dBASE m PLUS nó dBASE do DOS) |
| 1–3 | 3 beart | Dáta an nuashonraithe is déanaí; formáidithe mar YYMMDD |
| 4–7 | Uimhir 32-giotán | Líon na dtaifead sa chomhad bunachar sonraí |
| 8–9 | Uimhir 16-giotán | Líon na mbeart sa cheanntásc |
| 10–11 | Uimhir 16-giotán | Líon na mbeart sa taifead |
| 12–13 | 2 beart | Curtha in áirithe; líonadh le 0 |
| 14 | 1 beart | Bratach a léiríonn idirbheart neamhiomlán[nóta 1] |
| 15 | 1 beart | Bratach criptiúcháin[nóta 2] |
| 16–27 | 12 beart | Curtha in áirithe le haghaidh dBASE le haghaidh DOS i dtimpeallacht ilúsáideora |
| 28 | 1 beart | Bratach comhad .mdx a tháirgeadh; 1 má tá comhad .mdx táirgthe ann, 0 mura bhfuil |
| 29 | 1 beart | ID tiománaí teanga |
| 30–31 | 2 beart | Curtha in áirithe; líonadh le 0 |
| 32–n [nóta 3][nóta 4] | 32 beart an ceann | sraith tuairisceoirí allamuigh (féach thíos le haghaidh leagan amach na dtuairisceoirí) |
| n+1 | 1 beart | 0x0D mar an críochnaitheoir eagar tuairisceora réimse |

- Seiceálann an fheidhm ISMARKEDO an bhratach seo (socraíonn BEGIN TRANSACTION go 1 é, END TRANSACTION agus ROLLBACK athshocrú go 0).
- Má tá an bhratach seo socraithe go 1, feictear an Bunachar Sonraí teachtaireachta criptithe.
- Is é 255 uaslíon na réimsí.
- ciallaíonn n an beart deireanach san eagar tuairisceora réimse.

### Eagar tuairisceora réimse
Leagan amach na dtuairisceoirí réimse in dBASE:

| Beart | Clár | Brí |
---|---|---|
| 0–10 | 11 beart | Ainm páirce in ASCII (líonta nialasach) |
| 11 | 1 beart | Cineál réimse. Luachanna ceadaithe: C, D, F, L, M, nó N (féach an chéad tábla eile le haghaidh bríonna) |
| 12–15 | 4 beart | Curtha in áirithe |
| 16 | 1 beart | Fad réimse i dénártha (uasmhéid 254 (0xFE)). |
| 17 | 1 beart | Comhaireamh deachúil allamuigh i ndénártha |
| 18–19 | 2 beart | Aitheantas an limistéir oibre |
| 20 | 1 beart | Sampla |
| 21–30 | 10 mbeart | Curtha in áirithe |
| 31 | 1 beart | Bratach réimse MDX Táirgeadh; 1 má tá clib innéacs ag an réimse sa chomhad MDX táirgthe, 0 mura bhfuil |

### Taifid bunachar sonraí
Tosaíonn gach taifead le bratach scriosta (1-beart). Tá réimsí fillte i dtaifid gan deighilteoirí páirce. Tá na sonraí allamuigh go léir ASCII. Ag brath ar chineál an réimse, cuireann an t-iarratas srianta breise. Seo na cineálacha páirce in dBase:

| Cineál réimse | cuimhneacháin | Cad a ghlacann sé |
-------|-----|----|
| C | Carachtar | Aon téacs ASCII (stuáilte le spásanna suas go fad na páirce) |
| D | Dáta | Uimhreacha agus carachtar chun mí, lá agus bliain a scaradh (stóráilte go hinmheánach mar 8 ndigit i bhformáid BBBBBB) |
| F | Snámhphointe | -, ., 0–9 (ar dheis údar, stuáilte le spásanna bána) |
| L | Loighciúil | Y, y, N, n, T, t, F, f, nó ? (nuair a bheidh sé neamhluaite) |
| M | Meamram | Aon téacs ASCII (stóráilte go hinmheánach mar 10 ndigit a léiríonn uimhir bhloc .dbt, údar ceart, stuáilte le spásanna bána) |
| N | Uimhriúil | -, ., 0–9 (ar dheis údar, stuáilte le spásanna bána) |









## Tagairtí ##

* [.dbf - Vicipéid](https://en.wikipedia.org/wiki/.dbf)


