{
  "date": "2020-08-20",
  "keywords": [
"ttf failu",
"ttf faila formātā",
"kas ir ttf fails",
"failu",
"ttf piemērs",
"ttf faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TTF — TrueType fonta faila formāts",
  "description": "TrueType fonti (TTF) ir balstīti uz digitālo fontu tehnoloģijas specifikācijām, kuras sākotnēji izstrādāja Apple, Inc. Gan Apple, gan Microsoft izmantoja TTF operētājsistēmās Mac un Windows.",
  "linktitle": "TTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-tt-lvf"
}
},
  "lastmod": "2020-09-21"
}

## Kas ir TTF fails?

Fails ar paplašinājumu .ttf ir fontu faili, kuru pamatā ir TrueType specifikāciju fontu tehnoloģija. Sākotnēji to izstrādāja un palaida Apple Computer, Inc operētājsistēmai Mac OS, un vēlāk to pieņēma Microsoft operētājsistēmai Windows. TrueType fonti nodrošina augstākās kvalitātes displeju datora ekrānos un printeros bez atkarības no izšķirtspējas. Visas mūsdienu lietojumprogrammas, kas izmanto fontus, spēj strādāt ar TTF failiem. TTF fontu faili ir brīvi pieejami internetā, un tos var arī konvertēt citos fontu failu formātos, piemēram, OTF un WOFF.

## Īsa vēsture

Designed by Apply Computer, Inc in 1980s for MacOS, the TTF font format was aimed at resolving some technical limitations by Adobe's Type 1 format. Apple included support for TrueType fonts in Mac in 1991. TTF fontu dizaina mērķis bija uzglabāšanas un apstrādes efektivitāte un paplašināmība. Pamatojoties uz šo paplašināmību, esošos fontus var pārvērst TrueType formātā.

Microsoft pirmo reizi TrueType fontus izmantoja operētājsistēmā Windows 3.1 1992. gada aprīlī pēc tam, kad Apple piekrita licencēt TrueType Microsoft. Tas uzlaboja rastrizācijas mehānismu, kā arī uzlaboja tā efektivitāti un veiktspēju.

## Patiesā tipa faila formāta specifikācijas

TrueType fonta fails ir binārs fails, kas sastāv no sasaistītu tabulu secības. Katra tabula ir vārdu secība, un tai ir nosaukums, kas pazīstams kā Tag. Katrs tags ir uint32 datu tipa un sastāv no četrām rakstzīmēm. Pirmā tabula failā ir fontu direktorijs, kas nodrošina piekļuvi citām fontu faila tabulām. Fontu dati ir ietverti citās tabulās, kas seko pēc fontu direktoriju tabulas. Tā kā katrai tabulai var piekļūt ar tās tagu, tabulas failā var parādīties jebkurā secībā.

Nepieciešamās tabulas un to tagu nosaukumi ir parādīti nākamajā tabulā.

|**Taga**|**Tabula**|
---|---|
|'cmap'| rakstzīmju un glifu kartēšana|
|'glyf'| glifu dati|
|'galva'| fonta galvene|
|'hhea'| horizontālā galvene|
|'hmtx'| horizontālā metrika|
|'loca'| rādītājs uz atrašanās vietu|
|'maxp'| maksimālais profils|
|'nosaukums'| nosaukšana|
|'post'| PostScript|

### Datu veidi
TrueType fonti izmanto standarta veselo skaitļu un papildu datu tipus, kā norādīts nākamajā tabulā.

|**Datu veids** | **Apraksts** |
---|---|
|shortFrac| 16 bitu daļdaļa|
|Fiksēts| 16,16 bitu zīme fiksēta punkta numurs|
|FWord| 16 bitu vesels skaitlis, kas apraksta daudzumu FU vienībās, kas ir mazākais izmērāmais attālums em telpā.|
|uFWord| 16 bitu neparakstīts vesels skaitlis, kas apraksta daudzumu FU vienībās, kas ir mazākais izmērāmais attālums em telpā.|
|F2Dot14| Fiksēts skaitlis ar 16 bitu zīmi, un zemie 14 biti apzīmē daļu.|
|longDateTime|	The long internal format of a date in seconds since 12:00 midnight, January 1, 1904. It is represented as a signed 64-bit integer.|

### Fontu direktorijs

Pirmā TrueType fonta tabula ir fontu direktorijs, kas nodrošina piekļuvi informācijai, kas nepieciešama, lai piekļūtu datiem citās tabulās. Turklāt tas sastāv no:

 * Nobīdes apakštabula - saglabā tabulu ierakstu fontā un nodrošina nobīdes informāciju, lai piekļūtu katrai direktorija tabulai
 * `Tabulas direktorijs` — satur katras fonta tabulas ierakstus

#### Ofseta apakštabula
Nobīdes apakštabula ir parādīta zemāk.

|**Veids**|**Nosaukums**|**Apraksts**|
---|---|---|
|uint32| skalera tips| Tags, kas norāda OFA mērogošanas līdzekli, kas jāizmanto šī fonta rasterēšanai; Papildinformāciju skatiet tālāk norādītajā piezīmē par mērogošanas veidu.|
|uint16| numTables| tabulu skaits|
|uint16| meklētRange| (maksimālā jauda 2 <= numTables)*16|
|uint16| ierakstsSelector| log2(maksimālā jauda 2 <= numTables)|
|uint16| rangeShift| numTables*16-searchRange|

#### Tabulu direktorijs
Tabulas direktorijs ir uzreiz aiz nobīdes apakštabulas. Tā struktūra ir tāda, kā parādīts nākamajā tabulā.

|**Veids**|**Nosaukums**|**Apraksts**|
---|---|---|
|uint32| tags| 4 baitu identifikators|
|uint32| kontrolsumma| kontrolsumma šai tabulai|
|uint32| nobīde| nobīde no sfnt| sākuma
|uint32| garums| šīs tabulas garums baitos (faktiskais garums nav polsterēta garums)|

Katrai fonta faila tabulai ir jābūt savam tabulas direktorijas ierakstam. Tabulas ieraksti ir jākārto augošā secībā pēc atzīmes.


## Atsauces
 * [TrueType fontu uzziņu rokasgrāmata](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
 * [TrueType pārskats](https://learn.microsoft.com/en-us/typography/truetype/)

