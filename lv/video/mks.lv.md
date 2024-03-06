{
  "date": "2021-24-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "MKS faila formāts",
  "keywords": [
"mks",
"matroska video",
"mkv formātā",
"failu",
"formātā",
"video"
],
  "description": "Uzziniet par MKS faila formātu subtitriem, ko izveido tikai Matroska, un API, kas var izveidot un atvērt MKS failus.",
  "linktitle": "MKS",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mk-lvs"
}
},
  "lastmod": "2021-25-02"
}

## Kas ir MKS fails?

The MKS files are generally known as Matroska files containing subtitles only. Although the Matroska is a general file container, it avoids keeping the information of specific formats. Since subtitles are being used in some of the audio or video containers, Matroska is paying attention to store some common subtitle formats. It helps Matroska to be consistent with the growth rate. You need to follow the points as given below to store the subtitles in Matroska:

- .mks”. paplašinājumu izmantos Matroska fails (satur tikai subtitrus).
- **CodecPrivate** tiek izmantots, lai saglabātu visu ar kodekiem saistīto informāciju, kas ir globāla visai straumei.
- Noņemiet sākuma un beigu laikspiedolus, kas tiek izmantoti sākotnējā krātuves formātā. Tā vietā izmantojiet bloku laikspiedolu un ilgumu.
- Varat izmantot jebko ar caurspīdīgu slāni, ieskaitot video.

## Kopējie subtitru formāti

Here are some brief notes about more common subtitle formats stored in Matroska:

### Attēli Subtitri
VobSub subtitru formāts ir pirmais attēla subtitru formāts, kas importēts programmā Matroska. Šis formāts tiek ģenerēts, eksportējot subtitrus no DVD. Uzglabājot Matroskā, ieraksti ir jāatdala, ja VobSub sastāv no vairāku straumju kopas.

### SRT subtitri
The SRT is the most simple and basic of all subtitle formats. It consists of four parts as given below:
 
 1. Skaitlis, kas norāda subtitru secību.
 2. Subtitru parādīšanās un pazušanas laiks ekrānā.
 3. Pats apakšvirsraksts.
 4. Tukša rindiņa, kas norāda nākamā apakšvirsraksta sākumu.
 
### SSA/ASS subtitri
Sub Station Alpha (SSA) ir faila formāts, ko izmanto populārais subtitru redaktors SubStation Alpha. SSA subtitrus plaši izmanto fanu abonētāji. Tam ir iespēja parādīt modernas funkcijas, piemēram, karaoke, pozicionēšana, stils utt.
 
### WebVTT subtitri
World Wide Web Consortium (W3C) izstrādāja WebVTT, kas ir saīsināts kā Web Video Text Tracks Format”. Šis formāts tiek izmantots, lai atzīmētu ārējos teksta celiņa resursus saistībā ar HTML elementu.

### HDMV prezentācijas grafikas subtitri
HDMV prezentācijas grafikas subtitru formāts (HDMV PGS) ir bitkartes sērija, un mēs to vispār nevaram pateikt kā tekstu. Citiem vārdiem sakot, jūs varat teikt, ka tā ir tikai noteikta grafisko attēlu secība. Lai iegūtu informāciju, PGS konvertēšana uz SRT ir nepieciešams process.

### HDMV teksta subtitri
HDMV teksts ir pazīstams kā teksta subtitru formāts, ko izmanto Blu-rays. Matroska atļauj tikai UTF-8 rakstzīmju kopu When saglabā TextST subtitrus.

### Digitālās video apraides (DVB) subtitri
DVB subtitru formāts tika ieviests, lai regulētu vairāku valodu subtitru pārraidi un attēlošanu TV signālos. Tipisks subtitru formāts ļautu arī jebkuram skatītājam skatīties DVB subtitru pārraides neatkarīgi no pārraides sistēmu ražotāja.


## Atsauces Nr.

- [Matroska Subtitles](https://www.matroska.org/technical/subtitles.html)

