{
  "date": "2021-04-15",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid MPG",
  "keywords": [
"MPG",
"comhad",
"síneadh",
"formáid",
"formáid físeán",
"Cad é formáid comhaid mpg",
"Formáid comhaid mpg",
"Imreoir comhaid mpg",
"comhbhrú mpeg",
"físeán",
"MPEG",
"MPEG-1",
"MPEG-2"
],
  "description": "Foghlaim faoi fhormáid comhaid MPG agus APIs is féidir a chruthú agus a thaispeáint go conas a oscailt na comhaid MPG.",
  "linktitle": "MPG",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mp-gag"
}
},
  "lastmod": "2021-07-26"
}

## Cad é formáid comhaid MPG? ##

The file with a .mpg extension belongs to the group of file extensions for MPEG-1 or MPEG-2 audio and video compression. MPEG-1 Part 2 video is not easily available, and this extension (MPG file format) typically points to a MPEG program stream which is defined in MPEG-1 and MPEG-2, or an MPEG transport stream which is defined in MPEG-2. Tá síntí eile cosúil le .m2ts ann freisin a shonraíonn an coimeádán cruinn, sa chás seo, MPEG-2 TS, ach is beag an bhaint atá aige seo le meáin MPEG-1. Is é [.mp3](/audio/mp3/) an breiseán is coitianta do chomhaid ina bhfuil fuaim MP3. Is gnáthshruth fuaime amh é comhad MP3; Is é an bealach traidisiúnta chun comhaid MP3 a chlibeáil ná trí shonraí srutha a scríobh chuig codanna truflais de gach fráma, rud a shábhálann faisnéis na meán ach a chuireann an **seinnteoir comhaid mpg** i leataobh. Is teicníocht den chineál céanna é seo a úsáidtear chun na comhaid AAC a chlibeáil, ach is lú an tacaíocht a thugtar dóibh inniu.

## Comhbhrú MPEG ##

Seasann an t-ainm MPEG do Moving Pictures Experts Group. Is uirlis é MPEG le haghaidh comhbhrú físeáin, a bhaineann le comhbhrú íomhánna agus fuaimeanna, chomh maith le sioncrónú an dá cheann.
Tá roinnt caighdeáin MPEG ann faoi láthair.

- Tá MPEG-1 beartaithe le haghaidh rátaí sonraí idirmheánacha, thart ar 1.5 Mbit/soicind.
- Tá MPEG-2 beartaithe le haghaidh rátaí arda sonraí de 10 Mbit/soicind ar a laghad.
- Moladh MPEG-3 le haghaidh comhbhrú HDTV ach fuarthas go raibh sé iomarcach agus rinneadh é a chumasc le MPEG-2.
- Tá MPEG-4 molta do rátaí sonraí an-íseal níos lú ná 64 Kbit/soic.


## Sruth cláir formáid comhaid MPG ##

Is coimeádán é sruth an chláir chun ilphléacsáil fuaime digiteach, físeáin agus go leor eile. Tá formáid Sruth na gClár sonraithe sa 1ú chuid de MPEG-1 (ISO/IEC 11172-1) agus sa chuid 1ú de MPEG-2, Córais (caighdeán ISO/IEC 13818-1/ITU-T H.222.0). Tá Sruth Clár MPEG-2 bunaithe ar analóg agus cosúil le ciseal ISO/IEC 11172 Systems agus comhoiriúnach ar aghaidh.

### Sonraí códaithe ###

Seo iad na sonraí códaithe maidir le formáid ceanntásca pháirteach an phacáiste MPEG-2 Stream Stream:

| Ainm | Líon giotán | Cur Síos |
---|---|---|
| bearta sioncronaithe | 32 | 0x000001BA |
| giotán marcála | 2 | 01b le haghaidh leagan MPEG-2. Is iad na giotán marcála don leagan MPEG-1 ná 4 ghiotán le luach 0010b. |
| Clog córais [32..30] | 3 | Giotán Tagartha Clog an Chórais (SCR) 32 go 30 |
| giotán marcála | 1 | 1 Giotán socraithe i gcónaí. |
| Clog córais[29..15] | 15 | Giotán clog córais 29 go 15 |
| giotán marcála | 1 | 1 Giotán socraithe i gcónaí. |
| Clog córais [14..0] | 15 | Giotán clog córais 14 go 0 |
| giotán marcála | 1 | 1 Giotán socraithe i gcónaí. |
| Síneadh SCR | 9 | |
| giotán marcála | 1 | 1 Giotán socraithe i gcónaí. |
| ráta giotán | 22 | In aonaid 50 beart in aghaidh an tsoicind. |
| giotán marcála | 2 | 11 Giotán socraithe i gcónaí. |
| in áirithe | 5 | in áirithe le húsáid sa todhchaí |
| fad líonadh | 3 | |
| beart líonadh | 8*fad líonta | |
| ceanntásc córais (roghnach) | 0 nó níos mó | má leanann cód tosaithe ceanntásc an chórais: 0x000001BB |

Taispeánann an tábla seo a leanas formáid ceanntásca an chórais pháirtigh:

| Ainm | Líon na mbeart | Cur Síos |
---|---|---|
| bearta sioncronaithe | 4 | 0x000001BB |
| fad ceanntásca | 2 | |
| ráta faoi cheangal agus giotán marcóra | 3 | |
| closcheangal agus bratacha | 1 | |
| bratacha, giota marcóra, agus ceangal físe | 1 | |
| Srianadh ráta paicéad agus beart forchoimeádta | 1 | |


## Tagairtí ##

- [MPEG-1 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-1)



