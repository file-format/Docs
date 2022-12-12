{
  "date" : "2019-10-11",
  "keywords" :[ "AVI", "Tömörített audiovideó", "Fájl", "Kiterjesztés", "Fájlformátum", "Multimédia tároló", "XVid", "DivX", "Kodekek", "Erőforráscsere fájlformátum", "RIFF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AVI fájlformátum - Audio-video interleave fájl",
  "description":"További információ az AVI fájlformátumról és az API-król, amelyek AVI-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "AVI",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-04-23"
}

## Mi az AVI fájl? ##

Az **AVI** fájlformátum egy audio-videó multimédiás tárolófájlformátum, amelyet a Microsoft vezetett be. Tárolja a hang- és videoadatokat, amelyeket több kodekkel (kódolók/dekóderek) hoztak létre és tömörítenek, például **XVid** és **DivX**. Mivel az AVI tartalmak kódolására különböző kodekek használhatók, a visszakereső alkalmazások, azaz az AVI lejátszók csak akkor tudják megnyitni ezeket, ha telepítve vannak a szükséges kodekek, amelyekkel az AVI tartalmat létrehozták. A formátum alapértelmezés szerint az összes **Microsoft Windows** platformon, valamint szinte az összes többi jelentős platformon támogatott. Számos alkalmazás és API lehetővé teszi az AVI létrehozását/mentését, olvasását és más népszerű formátumokká konvertálását, például MP4, MOV, WMV stb.

## AVI fájl formátum ##

Az .avi kiterjesztésű fájl AVI-fájl. Ez a Resource Interchange File Format (RIFF) alformátuma. A RIFF blokkokba vagy "darabokba" rendezi az adatokat, amelyeket FourCC címkével azonosítanak. Az AVI fájl egyszerűen egy "darab" egy RIFF formátumú fájlban.

Az első részdarabban a fájl fejlécét a "hdrl" címke azonosítja; tartalma tartalmazza a videó szélességét, magasságát és képkockasebességét. A második részegységben a mozgáscímke a videó képkockasebességét jelzi. Az AVI videó a tényleges audio/vizuális adatokból áll ebben a darabban. Van egy harmadik opcionális alcsonk is az „idx1” címkével, amely a fájlhoz tartozó egyes adatdarabok fájlon belüli helyét jelzi.

### Korlátozások ###

* A képarány információ nem kódolható az eredeti AVI specifikációban, bár a későbbi OpenDML specifikáció (AVI 2.0) szabványos módszert kínál
* Bár az AVI-fájlokat széles körben használják a filmek és a televíziós utómunkálatok során, az időkód hozzáadásának különféle módjai versengenek egymással, ami befolyásolja a formátum használhatóságát.
* Az AVI-ban kódolt videofájlok nem használhatnak olyan tömörítési technikát, amely a kódolt képkockán túlmenő jövőbeli képkockák adatait igényli (B-kocka)
* Problémás a változó bitrátájú (VBR) AVI fájlok használata (például MP3 hang 32 kHz alatti mintavételi frekvencián)
* A normál felbontású játékfilmeket kódoló AVI-fájlok általában óránként körülbelül 5 MB többletköltséget jelentenek, a fájl felhasználási módjától függően
* A feliratokat be kell kódolni a videó adatfolyamba, vagy külön fájlban kell terjeszteni arra az esetre, ha az AVI-fájlok nem férnek hozzá mellékletekhez, például betűtípusokhoz és feliratokhoz

## Rövid története ##

Az AVI-t a Microsoft 1992-ben vezette be azzal a céllal, hogy robusztusabb és fejlettebb audio- és videofájlformátumot biztosítson. A formátum gyorsan népszerűvé vált az internet használatával, lehetővé téve az egyéneknek a videofájlok közvetlen és közvetett megosztását felhő alapú médiatáron keresztül.

## Referenciák ##

* [AVI – a Wikipedia által](https://en.wikipedia.org/wiki/Audio_Video_Interleave)

