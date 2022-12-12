{
  "date" : "2019-12-13",
  "keywords" :[ "AC3", "fișier", "extensie", "format", "Codare audio", "MPEG"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier AC3 și despre API-urile care pot crea și deschide fișiere AC3.",
  "title" :"AC3 - Fișier Audio Codec 3",
  "linktitle" : "AC3",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2019-12-13"
}

## Ce este un fișier AC3?

Un fișier cu extensia .ac3 este un fișier Audio Codec 3, introdus de Dolby Laboratories. Este un format audio care poate conține până la șase canale de ieșire audio. Formatul a fost folosit inițial pentru audio, dar acum este folosit și pentru alte aplicații, cum ar fi transmisia HDTV, DVD-uri, discuri Blue-ray și console de jocuri. Aplicațiile care pot deschide fișiere AC3 includ Apple QuickTime player, Microsoft Windows Media Player, Winamp, MPlayer și altele similare.

## Format de fișier AC3

Fișierele AC3 sunt de natură binară și se bazează pe transformarea cosinus discretă modificată (MDCT), care este un algoritm de compresie cu pierderi. Dolby Laboratories a folosit algoritmul MDCT împreună cu principiile de codificare perceptivă pentru a dezvolta formatul audio AC-3. Acest lucru a condus la lansarea formatului AC-3 ca standard Dolby Digital în 1991. Formatul acceptă furnizarea a cinci canale pentru difuzoarele de gamă normală (20 Hz - 20.000 Hz) și un canal (20 Hz - 120 Hz) pentru subwoofer-ul a condus efecte de joasă frecvență. AC3 acceptă rate de eșantionare de până la 48 kHz.

### Detalii tehnice ale formatului fișierului AC3

Tehnologia Dolby Digital folosește o modalitate foarte eficientă de a comprima dimensiunea fișierelor audio multicanal fără a afecta calitatea sunetului. Această compresie duce la o dimensiune mai mică a fișierelor, ceea ce facilitează distribuirea fișierelor de sunet. Folosind Dolby Digital, este posibil să includeți un mix audio complet pe 5.1 canale pe un film imprimat sau un DVD.

#### Specificații
Specificațiile Dolby Digital sunt după cum urmează.

|Câmp|Specificație|
---|---|
|Canale |1.0 la 5.1, discrete|
|Rata datelor DVD, audio pe 5.1 canale| 384 sau 448 kbps|
|Rata de date pentru disc Blu-ray, audio pe 5.1 canale|640 kbps|
|Acceptă metadatele Dolby |Da|
|Conexiuni |S/PDIF, HDMI®, IEEE 1394|
|Capacități de amestecare/streaming|Da|

#### Parametrii metadatelor

|Parametru de metadate| Informațional|Control|
---|---|---|
|Nivel de dialog| |Da|
|Modul canal| | Da|
|Canal LFE| | Da|
|Modul Bitstream| Da| Da|
|Comprimare mod linie| | Da|
|Compresie în modul RF| | Da|
|Protecție la supramodulație RF| | Da|
|Nivelul de downmix al centrului| | Da|
|Nivel surround downmix| | Da|
|Modul Dolby Surround| |Da|
|Informații despre producția audio| Da||
|Nivel de amestec| Da||
|Tipul camerei| Da||
|Bit de drepturi de autor| Da||
|flux de biți original| Da||
|Downmix stereo preferat| |Da|
|Lt/Rt Center downmix level||Da|
|Lt/Rt Surround downmix level||Da|
|Lo/Ro Center downmix level||Da|
|Lo/Ro Surround downmix level||Da|
|Modul Dolby Digital Surround EX™||Da|
|Tip convertor A/D|Da||
|Filtru DC||Da|
|Filtru trece jos||Da|
|Filtru trece jos LFE||Da|
|Atenuare surround 3 dB||Da|
|Deplasare de fază surround||Da|

## Referințe

* [AC3 - Prin Wikiepedia](https://en.wikipedia.org/wiki/Dolby_Digital)
* [Dolby Digital 5.1](https://professional.dolby.com/tv/dolby-digital)

