{
  "date" : "2021-04-26",
  "keywords" :[ "aiff", "fájl", "kiterjesztés", "formátum", "audiocsere fájlformátum", "zene", "aiff fájlformátum", "aiff mp3-ba", "aiff vs wav", "aiff konvertálása formátumba mp3" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az AIFF fájlformátumról és az API-król, amelyek AIFF-fájlokat hozhatnak létre, konvertálhatnak és megnyithatnak.",
  "title" :"AIFF - Audio Interchange File Format",
  "linktitle" : "AIFF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Mi az AIFF fájl?
Az AIFF (Audio Interchange File Format) egy tömörítetlen hangfájlformátum, amelyet az Apple fejlesztett ki 1998-ban, de az **EA IFF 85** (az Electronic Arts által kifejlesztett szabvány az Interchange Format Files számára), egy Amiga rendszereken használt burkoló formátumon alapul. . Ez a fájlformátum szabványt tartalmaz a mintavételezett hangok tárolására. A formátum rugalmassága elég jó, és lehetővé teszi a monó vagy többcsatornás mintavételezett hangok tárolását különböző mintavételi frekvenciákkal és mintaszélességekkel. Mivel az AIFF-fájlok tömörítetlenek, ezért nagyobb méretük van, mint más veszteséges formátumok, például [MP3](https://docs.fileformat.com/audio/mp3/).

Az AIFF fájlok 2 csatornás tömörítetlen sztereó hangot tartalmaznak, 16 bites mintamérettel, 44,1 khz-en rögzítve. A kiváló hangminőség miatt egy 5 perces hangfelvétel akár 50 MB lemezterületet is elfoglalhat, ami hasonló a [WAV](https://docs.fileformat.com/audio/wav/) fájlformátumhoz.

## AIFF vs WAV

Az AIFF és a WAV minőségileg szinte megegyezik. Mindkettő ugyanazt a PCM (impulzuskód moduláció) kódolást használja, ami nagyobb méretűvé teszi őket más veszteséges formátumokhoz képest, mint például [MP3](https://docs.fileformat.com/audio/mp3/), [M4A](). Néhány általános eltérés az alábbi táblázatban található:

|AIFF|WAV|
---|---|
|Többnyire MAC-hoz használják|Többnyire PC-hez használják|
|Lehetővé teszi a metaadatokat| Nem engedélyezi a metadeta|

## AIFF fájl szerkezet

Az **EA IFF 85** általános struktúrát határoz meg az adatok fájlokban való tárolására. Egy **EA IFF 85** fájl számos adatcsomagból áll. Az AIFF-fájl egy darabja néhány fejlécinformációból áll, amelyeket adatok követnek:
{{< figure src="../chunk.png" alt="AIFF darab" >}}

Az AIFF-fájl számos különböző típusú darab gyűjteménye. Két általános típusú darab van, amelyek fontosak egy AIFF-fájldarab létrehozásához:
- **Common Chunk**: A mintavételezett hangot leíró fontos paramétereket tartalmazza, mint például a hossza és a mintavételi gyakoriság.
- **Sound Data Chunk**: A tényleges hangmintákat tartalmazza.
Sok más opcionális darab is létezik, amelyek felsorolják a műszerparamétereket, meghatározzák a markereket, tárolják az alkalmazásspecifikus információkat stb.

### Helyi csonktípusok

Az AIFF létrehozásához szükséges darabtípusokat az alábbi táblázat tartalmazza:

|Részlettípus| Leírás|
---|---|
|Common Chunk|A Common Chunk a mintavételezett hang alapvető paramétereit írja le|
|Sound Data Chunk|A Sound Data Chunk tartalmazza a tényleges mintakockákat|
|Marker Chunk|A Marker Chunk olyan markereket tartalmaz, amelyek a hangadatokban lévő pozíciókra mutatnak|
|Instrument Chunk|Az Instrument Chunk meghatározza azokat az alapvető paramétereket, amelyeket egy hangszer, például egy sampler használhat a hangadatok lejátszásához|
|MIDI Data Chunk|A MIDI Data Chunk használható MIDI adatok tárolására|
|Audio Recording Cunk|A Hangrögzítési csonk a hangrögzítő eszközökre vonatkozó információkat tartalmaz|
|Alkalmazásspecifikus darab|Az alkalmazásspecifikus darabot az alkalmazások gyártói bármilyen célra felhasználhatják|
|Megjegyzés-csonk|A megjegyzéscsonk a megjegyzések tárolására szolgál a FORM AIFF|-ban
|Szövegdarabok - Név, Szerző, szerzői jog, megjegyzés| Mind szövegdarabok|

## Referenciák ##

* [Audio Interchange File Format – a Wikipedia által](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)

