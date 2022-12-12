{
  "date" : "2021-02-20",
  "keywords" :[ "WMA", "fájl", "kiterjesztés", "formátum", "audiocsere fájlformátum", "zene" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a WMA fájlformátumról és az API-król, amelyek WMA-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"WMA - Windows Media Audio File",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## Mi az a WMA fájl?

A .wma kiterjesztésű fájl Advanced Systems Format (ASF) formátumban mentett hangfájl. Az ASF a Microsoft szabadalmaztatott formátuma, amely a Windows Media Audio 9 által kódolt bitfolyamokat tartalmazza. A hangtartalom mellett a WMA-fájl metaadat-objektumokat is tartalmaz, például a szám címét, albumát, előadóját és műfaját. A WMA-fájlokat elsősorban az interneten keresztüli streamelésre használják, hasonlóan az [.mp3](/hu/audio/mp3/) fájlokhoz.

## WMA fájl formátum

A WMA fájl bináris fájlformátum, és az ASF fájlformátumban található. Meghatározza a fájl metaadatainak kódolását, hasonlóan az MP3 fájlok által használt ID3 címkékhez. A WMA kodeket a Microsoft 2008 óta használja Protected Interoperable File Format (PIFF) formájában. A kapcsolódó iparági szabványok, például a DECE UltraViolet és az MPEG-DASH azonban nem minősítették szabványos audiokodeknek.

### WMA típusspecifikus adatok

A Windows Media Audio kodek típusspecifikus információi a következő formátumban vannak tárolva a Stream Properties objektum típusspecifikus adatai részeként.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Hivatkozások

* [ASF áttekintése – Microsoft](https://docs.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format?redirectedfrom=MSDN)

