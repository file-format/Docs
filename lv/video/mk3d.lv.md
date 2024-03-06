{
  "date": "2021-23-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "MK3D faila formāts",
  "keywords": [
"mk3d",
"matroska video",
"mkv formātā",
"stereoskopisks 3D",
"StereoMode",
"video",
"failu",
"formātā"
],
  "description": "Uzziniet par MK3D faila formātu stereoskopiskiem 3D videoklipiem, ko izveidojis Matroska, un API, kas var izveidot un atvērt MK3D failus.",
  "linktitle": "MK3D",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mk3-lvd"
}
},
  "lastmod": "2021-23-02"
}

## Kas ir MK3D fails? ##

MK3D faili pieder Matroska video formātu saimei. Šie faili patiesībā ir **stereoskopiski 3D** video, kas izveidoti, izmantojot Matroska 3D formātu. MKV faila konteiners izmanto lauka StereoMode vērtību, lai definētu stereoskopisku 3D video saturu. StereoMode vērtība ir pieejama arī, lai parādītu vecos stereo 3D video, atdalot ciānas un sarkanas krāsas (AnaGlyph)

## Tehniskas detaļas ##
3D videoklipus var saspiest divos veidos:

- Katrai acij atsevišķa trase.
- Apvienojiet katru acu izsekošanu vienā ierakstā.

MKV failu konteiners atbalsta abus šos.

Viena celiņa videoklipiem, kas ir vienkāršāki ar 3D materiālu, ir jāiestata lauks **StereoMode**, kas nosaka, vai plaknes ir saliktas mono vai kreisās labās puses kombinētajā celiņā. Varat izmantot vienu no šīm StereoMode lauka vērtībām:

|Vērtība | Apraksts |
|---|---|
|0| mono|
|1| blakus (kreisā acs ir pirmā)|
|2| augša-apakšējā (labā acs ir pirmā)|
|3| augša-apakšējā (kreisā acs ir pirmā)|
|4| čekas dēlis (labais ir pirmais)|
|5| šaha (kreisais ir pirmais)|
|6| rinda pārsegta (labā ir pirmā)|
|7| rinda pārsegta (kreisais ir pirmais)|
|8| kolonna savīta (labais ir pirmais)|
|9| kolonna savīta (kreisais ir pirmais)|
|10| anaglifs (ciāna/sarkana)|
|11| blakus (labā acs ir pirmā)|
|12| anaglifs (zaļš/purpursarkans)|
|13| abas acis sašņorētas vienā blokā (kreisā acs ir pirmā) (lauka secīgais režīms)|
|14| abas acis sasietas vienā blokā (labā acs ir pirmā) (lauka secīgais režīms)|

Vairākiem celiņiem MKV konteineram ir jāizlemj par katra sliežu ceļa funkcionalitāti atsevišķi. Darba veikšanai tiek izmantotas **TrackOperation** ar **TrackCombinePlanes**.


## Atsauces Nr.

- [Matroska Specification Notes](https://www.matroska.org/technical/notes.html)
- [MKV File Container Support for Stereo 3D Video and the MK3D Files](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d-files/)

