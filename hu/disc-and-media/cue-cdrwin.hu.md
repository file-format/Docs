{
"dátum":"2023-10-18",
   "keywords":[
"dákó",
"cue fájl",
"cue cdrwin cue sheet file",
"hogyan lehet megnyitni egy cue fájlt",
"fájl",
"cue fájl kiterjesztése",
"kiterjesztés",
"fájl"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"CUE fájlformátum - CDRWIN cue lap",
   "description":"További információ a CUE CDRWIN Cue Sheet fájlformátumról és az API-król, amelyek CUE fájlokat hozhatnak létre és nyithatnak meg.",
"linktitle":"CUE CDRWIN",
   "menu":{
      "docs":{
         "identifier":"disc-and-media-cue-cdrwin",
         "parent":"disc-and-media"
}
},
"lastmod":"2023-10-18"
}

## Mi az a CUE fájl?

A **.CUE** fájl, más néven **CDRWIN Cue Sheet**, egyszerű szöveges fájl, amely információkat tartalmaz az audio CD vagy lemezkép műsorszámairól és elrendezéséről, jellemzően BIN vagy ISO formátumban. Ezeket a fájlokat gyakran használják a lemez szerkezetének és tartalmának leírására, lehetővé téve a CD-író szoftverek vagy a virtuális meghajtó szoftverek számára az eredeti lemez pontos reprodukálását.

## Példa a CUE fájlra

Íme egy példa arra, hogyan nézhet ki a „.cue” fájl:

```
PERFORMER "Artist Name"
TITLE "Album Title"
FILE "DiscImage.bin" BINARY
  TRACK 01 AUDIO
    TITLE "Track 1 Title"
    PERFORMER "Artist Name"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "Track 2 Title"
    PERFORMER "Artist Name"
    INDEX 01 03:45:21
  TRACK 03 AUDIO
    TITLE "Track 3 Title"
    PERFORMER "Artist Name"
    INDEX 01 07:28:17
  TRACK 04 AUDIO
    TITLE "Track 4 Title"
    PERFORMER "Artist Name"
    INDEX 01 12:15:40
  (Additional tracks go here...)
```

## CDRWIN dákólap

A CDRWIN Cue Sheet a CDRWIN szoftver által használt ".cue" fájlformátum speciális változata. A CDRWIN egy CD/DVD-író és -készítő szoftver, és a ".cue" lapjait ezzel a szoftverrel való használatra tervezték. Ezek a ".cue" lapok olyan információkat tartalmaznak, amelyek a CDRWIN számára szükségesek a CD vagy DVD pontos létrehozásához vagy írásához.

Íme néhány kulcsfontosságú részlet a CDRWIN dákólapokról:

1. **Egyedülálló a CDRWIN esetében**: A CDRWIN „.cue” lapjai a CDRWIN szoftverre specifikus, szabadalmaztatott formátumok. Bár hasonlóságokat mutatnak a szabványos ".cue" fájlokkal, a CDRWIN szolgáltatásaival és beállításaival való együttműködésre lettek kialakítva.
    






2. **Felhasználóbarát felület**: A CDRWIN könnyen használható felületet biztosít a ".cue" lapok létrehozásához és szerkesztéséhez. A felhasználók felhasználóbarát módon adhatnak hozzá vagy módosíthatnak információkat a sávokról, indexekről, hézagokról és egyéb paraméterekről.
    






3. **Kompatibilis lemeztípusok**: A CDRWIN Cue Sheet-eket elsősorban különböző típusú CD-k és DVD-k készítésére használják, beleértve az adatlemezeket, audio-CD-ket, vegyes módú lemezeket és egyebeket. A formátum lehetővé teszi a felhasználók számára, hogy meghatározzák a létrehozni kívánt lemez típusát és tartalmát.
    






4. **Lemez elrendezésének vezérlése**: A CDRWIN Cue Sheets részletes vezérlést biztosít a lemez elrendezése és szerkezete felett, beleértve a műsorszámok sorrendjét, a szünet/közbeállításokat és a felhasználó egyéb különleges preferenciáit.
    






5. **ISO és BIN támogatás**: A CDRWIN ISO és BIN lemezképformátumokkal is működik. A „.cue” lap meghatározza, hogy melyik képfájlt használja a lemez, biztosítva a megfelelő szinkronizálást a jelzések és a kép között.
    






6. **Írás és bemásolás**: Ezek a ".cue" lapok kulcsfontosságúak lemezek írásakor vagy számok kimásolásakor a CDRWIN használatával. Segítenek abban, hogy a végtermék megfeleljen a tervezett elrendezésnek és tartalomnak.
    






7. **Biztonsági mentés és visszaállítás**: A CDRWIN felhasználók gyakran hoznak létre ".cue" lapokat, amikor biztonsági másolatot készítenek CD-jükről vagy DVD-jükről. Ezek a lapok később felhasználhatók a lemez tartalmának visszaállítására, beleértve a műsorszámok elrendezését és az időzítést.

## CUE fájl - Mivel nyitható meg egy CUE fájl?

A CDRWIN Cue Sheet-eket kifejezetten a CDRWIN szoftverekhez tervezték, ezért általában a CDRWIN-en belüli megnyitásra és használatra készültek.

A CUE fájlokat megnyitó vagy hivatkozó programok

- CDRWIN
- Intelligens projektek IsoBuster
- EZB Systems UltraISO

## Egyéb CUE fájlok

Íme más fájltípusok, amelyek a **.cue** fájlkiterjesztést használják.

**Lemez és adathordozó**
- [CUE - Cue Sheet File](/hu/disc-and-media/cue/)
- [CUE - CDRWIN Cue Sheet](/hu/disc-and-media/cue-cdrwin/)

## Hivatkozások
* [CDRWIN](https://en.wikipedia.org/wiki/CDRWIN)

