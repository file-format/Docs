{
  "date": "2021-08-13",
  "keywords": [
"comhad sdi",
"formáid comhaid sdi",
"cad is comhad sdi ann",
"comhad",
"sampla sdi",
"síneadh comhad sdi",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid SDI agus APIanna ar féidir leo comhaid SDI a chruthú agus a oscailt.",
  "title": "SDI - Comhad Íomhá Imlonnaithe Córas Windows",
  "linktitle": "SDI",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-sd-gai"
}
},
  "lastmod": "2021-08-13"
}

## Cad is comhad SDI ann?
Tá blob ualaigh, blob tosaithe agus blob páirteach sa chomhad le síneadh .sdi; a úsáidtear go coitianta ag Windows Embedded Studio chun dioscaí RAM nó dioscaí tosaithe a chruthú chun Windows a luchtú agus a shuiteáil. Tá an SDI giorraithe le haghaidh Íomhá Imlonnaithe Córais. Is clár é an Windows Embedded Studio a úsáidtear chun íomhánna diosca a chruthú do Windows. I ndáiríre tá clár Bainisteoir Comhad SDI sa chlár seo agus uirlis líne ordaithe ar a dtugtar **sdimgr.exe**, is féidir an dá cheann a úsáid chun íomhánna SDI a chur i bhfeidhm, a chruthú agus a chur in eagar.

## Formáid comhaid SDI
Úsáidtear formáid comhaid SDI go forleathan le gur féidir diosca fíorúil a úsáid chun córas a chur ar bun. Cumasaíonn roinnt leaganacha de Microsoft Windows ** booting RAM**, rud atá tábhachtach chun comhad SDI a luchtú isteach sa chuimhne agus ansin tosaithe uaidh. Cumasaíonn an fhormáid comhaid SDI é féin le haghaidh tosaithe líonra freisin trí úsáid a bhaint as an PXE (Preboot Execution Environment). Tá sé á úsáid freisin le haghaidh íomháithe diosca crua.
### rannóga comhaid SDI
Is féidir an comhad SDI féin a fhoroinnt sna hailt seo a leanas:
- **Boot BLOB**: Áiríonn sé seo an clár tosaithe iarbhír, STARTROM.COM. Tá sé seo cosúil le hearnáil tosaithe diosca crua.
- **Lódáil BLOB**: Go hiondúil bíonn NTLDR ann agus seolann an Boot BLOB é.
- **Páirt BLOB**: Áiríonn sé seo an t-am rite tosaithe iarbhír; folaíonn sé freisin na comhaid boot.ini agus ntdetect.com ba cheart a bheith suite laistigh de fhréamh-eolaire an ama rite.
- **Diosc BLOB**: Is íomhá HDD cothrom í seo ag tosú le MBR. Úsáidtear é le haghaidh íomháú tiomántán crua in ionad booting. Chomh maith leis sin ní féidir ach BLOBanna Diosca a fheistiú le fóntais Microsoft.


## Tagairtí 

* [Íomhá Imlonnaithe an Chórais - le Vicipéid](https://en.wikipedia.org/wiki/System_Deployment_Image)



