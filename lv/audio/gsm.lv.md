{
  "date": "2021-08-05",
  "keywords": [
"gsm",
"failu",
"pagarinājumu",
"formātā",
"Audio",
"Globālā mobilā audio sistēma",
"gsm paplašinājums",
"gsm faili"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par GSM failu formātu un API, kas var izveidot un atvērt GSM failus.",
  "title": "GSM — globālā mobilā audio failu formāta sistēma",
  "linktitle": "GSM",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-gs-lvm"
}
},
  "lastmod": "2021-08-05"
}

## Kas ir GSM fails?

GSM ir faila paplašinājums, kas ir saistīts ar Global System for Mobile Audio Format Files. Failus, kas satur GSM paplašinājumus, var atvērt Linux, Windows un Mac OS platformās. GSM faila formāts pieder audio failu kategorijai.

GSM fails ir kodēts ar zudumiem bagātu CBR (konstanta bitu pārraides ātruma) skaņas kompresijas kodeku. Iztveršanas ātrums GSM audio failā ir 8000 paraugu sekundē, savukārt datu pārraides ātrums ir aptuveni 13 kbps. Bitu pārraides ātrums GSM failos nodrošina kvalitāti balss ierakstīšanas laikā. Turklāt GSM faila formāts ir pazīstams arī kā globālais standarta formāts, ko izmanto mobilajos tālruņos, un WAV failus var arī viegli kodēt, izmantojot GSM faila formātu. Visas problēmas ar GSM failu var viegli atrisināt pats lietotājs, nevēršoties pie speciālista.

Lietotāji var arī konvertēt GSM failus [MP3](/audio/mp3/) un [MP4](/video/mp4/) formātos.

## Īsa GSM faila formāta vēsture

GSM ir audio faila formāts, kas tika izveidots interneta telefonijai Eiropā. To izstrādāja Eiropas Telekomunikāciju standartu institūts (ETSI), lai to izmantotu kā 2G digitālo mobilo sakaru tīklu, ko izmanto mobilajos tālruņos un planšetdatoros. Mūsdienās to izmanto telefona sarunu un balss ziņojumu ierakstu glabāšanai.

## GSM faila formāta specifikācijas ##

GSM darbs strukturētā tīklā, kas sastāv no šādām sadaļām:

- **Modulācija**: tas ir process, kurā ievades dati tiek pārveidoti formātā, ko var viegli pārsūtīt. Pārsūtītie dati tiek demodulēti uztveršanas galā
- **Pārsraides ātrums**: GSM ir digitāla sistēma, kuras bitu pārraides ātrums pārsniedz 270 kbps.
- **Augšupsaites frekvenču diapazons**: 933–960 MHz
- **Lejupsaites frekvenču diapazons**: 890–915 MHz
- **Kanālu atstatums**: tas nozīmē attālumu starp blakus esošajām barjerām, kam jābūt aptuveni 200 kHz.
- **Dupleksais attālums**: tā ir atstarpe starp augšupsaites un lejupsaites frekvencēm, kurai jābūt 80 MHz.
- **Runas kodēšana**: GSM izmanto lineāro paredzamo kodēšanu (LPC). LPC saspiež bitu pārraides ātrumu. Kad audio signāls iziet caur filtru un atdarina balss traktu. GSM kodē runu ar ātrumu 13 kbps

| Audio saspiešanas formāts | Algoritms | Izlases likme | Bitu pārraides ātruma transformācija | Latentums | CBR | VBR | Stereo | Daudzkanālu |
| ------------------------- | --------- | ----------- | ------------------- | -------- | --- | --- | ------ | ------------ |
| |
| GSM-HR | VSELP | 8 kHz | 5,6 kbit/s | 25 ms | Jā | Nē | Nē | Nē |
| GSM-FR | RPE-LTP | 8 kHz | 13 kbit/s | 20–30 ms | Jā | Nē | Nē | Nē |
| GSM-EFR | ACELP | 8 kHz | 12,2 kbit/s | 20–30 ms | Jā | Nē | Nē | Nē |

## Atsauces Nr.

* [GSM — Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_audio_coding_formats)


