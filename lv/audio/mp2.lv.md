{
  "date": "2021-06-11",
  "keywords": [
"mp2",
"mp2 fails",
"pagarinājumu",
"formātā",
"kas ir mp2 fails",
"mūzika",
"mp2 faila formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par MP2 failu formātu un API, kas var izveidot, konvertēt un atvērt MP2 failus.",
  "title": "MP2 — MPEG Layer 2 audio faila formāts",
  "linktitle": "MP2",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-mp-lv2"
}
},
  "lastmod": "2021-06-11"
}

## Kas ir MP2 fails?

MP2 fails, ko sauc arī par MPA failu, ir audio fails, kas saspiests ar MPEG-1 vai MPEG-2 II slāni; audio saspiešanas formāts ar zudumiem, ko nosaka ISO/IEC 11172-3 kopā ar MPEG-1 Audio Layer I un MPEG-1 Audio Layer III ([MP3](/audio/mp3/)), lai samazinātu audio faila lielumu. Tā kā MP3 ir populārāks par MP2, jo tas ir mazāks un pieejams internetā. Tāpēc MP2 joprojām ir būtisks audio apraides standarts.

## MP2 faila formāts

MPEG Audio Layer II (MP2) ir MP3 standartu pamatalgoritms. MPEG-1 Audio Layer 2 kodējums tika iegūts no MUSICAM audio kodeka. Tas sākās kā Digital Audio Broadcast (DAB) projekts Vācijā kā daļa no EUREKA pētniecības programmas. Eureka 147 ietvēra trīs galvenos elementus: pārraides kodēšana un multipleksēšana, COFDM modulācija un MUSICAM audio kodēšana (maskēšanas modelis universālā apakšjoslas integrētā kodēšana un multipleksēšana). MUSICAM bija viens no nedaudzajiem kodējumiem, kas spēja sasniegt augstu audio kvalitāti ar bitu pārraides ātrumu diapazonā no 64 līdz 192 kbit/s uz vienu monofonisko kanālu. Mērķis bija nodrošināt zemu aizkavi, zemu sarežģītību, kļūdu robustumu, īsas piekļuves vienības un izpildīt apraides, telekomunikāciju un ierakstīšanas ciparu datu nesējos tehniskās prasības.

MP2 ir apakšjoslas audio kodētājs, ko var saspiest laika domēnā ar zemas aizkaves filtru banku, kas ģenerē 32 frekvenču domēna komponentus. Salīdzinājumam, MP3 ir transformācijas audio kodētājs ar hibrīda filtru banku, kas nozīmē, ka frekvenču domēnā tiek izmantota saspiešana pēc hibrīda pārveidošanas no laika domēna. MP2 kodētājs var izmantot starpkanālu dublēšanu, izmantojot izvēles kopīgo stereo intensitātes kodējumu.

### MP2 faila formāta specifikācijas

MP2 faila formāts ir balstīts uz secīgiem digitāliem kadriem ar 1152 iztveršanas intervāliem ar četriem iespējamiem formātiem:

- mono formāts
- stereo formāts
- intensitātes kodēts locītavas stereo formāts (stereo neatbilstība)
- divkanālu (nekorelēts) formāts
Dažas svarīgas MP2 tehniskās specifikācijas ir norādītas zemāk esošajā tabulā:

|Specifikācija| Apraksts|
---|---|
|**Paraugu ņemšanas biežums**| 32, 44,1 un 48 kHz|
|**Bitu pārraides ātrums**|32, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 un 384 kbit/s|
|**Papildu iztveršanas frekvences**|16, 22,05 un 24 kHz|
|**Papildu bitu pārraides ātrums**|8, 16, 24, 40 un 144 kbit/s|
|**Daudzkanālu atbalsts**|Līdz 5 pilna diapazona audio kanāliem un LFE kanāls (Zemas frekvences uzlabošanas kanāls)|

## Atsauces Nr.

* [MPEG-1 Audio Layer II — Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)


