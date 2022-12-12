{
  "date" : "2021-06-11",
  "keywords" :[ "mp2", "mp2 fájl", "kiterjesztés", "formátum", "mi az mp2 fájl", "zene", "mp2 fájlformátum"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ismerje meg az MP2 fájlformátumot és az API-kat, amelyek MP2 fájlokat hozhatnak létre, konvertálhatnak és megnyithatnak.",
  "title" :"MP2 - MPEG Layer 2 Audio File Format",
  "linktitle" : "MP2",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Mi az MP2 fájl?

Az MP2 fájl, amelyet MPA-fájlnak is neveznek, egy MPEG-1 vagy MPEG-2 II. réteggel tömörített hangfájl; az ISO/IEC 11172-3 által meghatározott veszteséges hangtömörítési formátum az MPEG-1 Audio Layer I és MPEG-1 Audio Layer III ([MP3](/hu/audio/mp3/)) mellett az audiofájl méretének csökkentése érdekében. Míg az MP3 népszerűbb, mint az MP2, kisebb mérete és az interneten keresztüli elérhetősége miatt. Ezért az MP2 továbbra is létfontosságú szabvány az audio műsorszórásban.

## MP2 fájl formátum

Az MPEG Audio Layer II (MP2) az MP3 szabványok alapalgoritmusa. Az MPEG-1 Audio Layer 2 kódolást a MUSICAM audiokodekből szereztük be. A Digital Audio Broadcast (DAB) projektként indult Németországban, az EUREKA kutatási program részeként. Az Eureka 147 három fő elemet tartalmazott: átviteli kódolást és multiplexelést, COFDM-modulációt és MUSICAM audiokódolást (Maszkoló minta univerzális alsávba integrált kódolás és multiplexelés). A MUSICAM azon kevés kódolások egyike volt, amelyek monofonikus csatornánként 64 és 192 kbit/s közötti bitsebességgel kiváló hangminőséget tudtak elérni. A cél az volt, hogy alacsony késleltetésű, alacsony komplexitású, hiba robusztusságot, rövid hozzáférésű egységet biztosítsanak, és teljesítsék a műsorszórás, a távközlés és a digitális adathordozón történő rögzítés műszaki követelményeit.

Az MP2 egy alsávos hangkódoló, amely az időtartományban tömöríthető egy alacsony késleltetésű szűrőbankkal, amely 32 frekvenciatartomány-komponenst generál. Összehasonlításképpen, az MP3 egy transzformációs audio kódoló hibrid szűrőbankkal, ami azt jelenti, hogy a frekvenciatartományban alkalmazott tömörítés az időtartományból történő hibrid transzformáció után. Az MP2 kódoló kihasználhatja a csatornák közötti redundanciákat az opcionális "közös sztereó" intenzitású kódolás használatával.

### MP2 fájlformátum specifikációi

Az MP2 fájlformátum 1152 mintavételi intervallumból álló egymást követő digitális képkockákon alapul, négy lehetséges formátummal:

- mono formátum
- sztereó formátum
- intenzitáskódolt közös sztereó formátum (sztereó irreleváns)
- kétcsatornás (korrelálatlan) formátum
Az MP2 néhány fontos műszaki specifikációja az alábbi táblázatban található:

|Leírás| Leírás|
---|---|
|**Mintavételi arányok**| 32, 44,1 és 48 kHz|
|**Bitráta**|32, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 és 384 kbit/s|
|**További mintavételi frekvenciák**|16, 22,05 és 24 kHz|
|**További bitsebességek**|8, 16, 24, 40 és 144 kbit/s|
|**Többcsatornás támogatás**|Akár 5 teljes tartományú audiocsatorna és egy LFE-csatorna (alacsony frekvenciájú csatorna)|

## Referenciák ##

* [MPEG-1 Audio Layer II – Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

