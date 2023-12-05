{
"dátum": "2023-06-21",
  "keywords": [
"alfájl",
"mi az alfájl",
"példa MicroDVD feliratfájlra",
"Felirat-kiterjesztések",
"Open Sub",
"Feliratfájltípusok",
"hogyan kell megnyitni a SUB fájlt",
"fájl",
"SUB fájl kiterjesztése",
"kiterjesztés"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "SUB fájl formátum - MicroDVD feliratfájl",
  "description":"További információ a SUB formátumról és az API-król, amelyek SUB fájlokat hozhatnak létre és nyithatnak meg.",
"linktitle": "SUB",
  "menu": {
    "docs": {
      "identifier": "video-sub",
      "parent": "video"
}
},
"lastmod": "2023-06-21"
}

## Mi az a SUB fájl?

A SUB-fájl egy MicroDVD-feliratfájl-formátum, amelyet a videók feliratainak megjelenítésére használnak, és általában .sub-fájlkiterjesztéssel rendelkeznek. Ezek a fájlok időzítési információkat és szöveget tartalmaznak minden egyes felirat bejegyzéshez.

A MicroDVD feliratfájlok egyszerű szövegalapú formátumot használnak, ahol minden egyes felirat több sorból áll. Az első sor a felirat időzítési adatait tartalmazza, beleértve a kezdési és befejezési időbélyeget. A következő sorok tényleges feliratszöveget tartalmaznak.

Íme egy példa a MicroDVD feliratfájlra:

```
{0}{100}Subtitle line 1
{150}{300}Subtitle line 2
{350}{550}Subtitle line 3
...
```

## Feliratkiterjesztések

A feliratok különböző kiterjesztésűek lehetnek a formátumtól függően. Néhány gyakori feliratfájl-kiterjesztés:

- **.srt:** SubRip feliratformátum. Ez az egyik legszélesebb körben használt feliratformátum, és számos médialejátszó és videószerkesztő szoftver támogatja.
- **.sub:** Feliratfájl formátum, amelyet különböző feliratformátumok használhatnak, például MicroDVD, SubViewer és SubStation Alpha.
- **.ass vagy .ssa:** Advanced SubStation Alpha vagy SubStation Alpha feliratformátum. Támogatja a fejlett funkciókat, például a szöveg formázását, pozicionálását és effektusait.
- **.vtt:** WebVTT (Web Video Text Tracks) formátum, amelyet a webes videók feliratainak megjelenítésére használnak. Általában HTML5 videolejátszókkal használják.
- **.idx/.sub:** DVD-feliratok által használt formátum. Az .idx fájl időzítési és formázási információkat tartalmaz, míg a .sub fájl a tényleges feliratszöveget.
- **.smi vagy .sami:** Szinkronizált Accessible Media Interchange formátum. Általában a Windows Media Player zárt és feliratozására használják.

## Mit jelent az Open Sub?

Az Open Sub általában az OpenSubtitles-t jelenti, amely egy népszerű online platform, amely több nyelven kínál feliratokat filmekhez és tévéműsorokhoz. Feliratfájlok hatalmas gyűjteményét kínálja felhasználói közössége által. Az OpenSubtitles webhelyén (www.opensubtitles.org) kereshet és tölthet le feliratokat a kívánt filmekhez vagy tévésorozatokhoz.

## Feliratfájl típusok

A feliratfájlok különféle formátumokban kaphatók, mindegyik saját fájltípussal vagy kiterjesztéssel. Íme néhány gyakori feliratfájltípus:

- **SubRip feliratformátum (.srt):** Ez az egyik legszélesebb körben használt feliratformátum. Az SRT fájlok egyszerű szöveges fájlok, amelyek időbélyeggel és megfelelő szöveggel ellátott feliratokat tartalmaznak.
- **SubViewer feliratformátum (.sub):** A SubViewer fájlok hasonlóak az SRT fájlokhoz, időbélyeggel és szöveggel ellátott feliratbejegyzéseket tartalmaznak, támogathatnak további funkciókat, például szövegformázást és színeket.
- **SubStation Alpha (.ssa) és Advanced SubStation Alpha (.ass):** Ezek a formátumok olyan speciális funkciókat támogatnak, mint a szövegformázás, stílus, pozicionálás és animációs effektusok. Az SSA és ASS fájlokat általában az anime-feliratokhoz használják.
- **MicroDVD feliratformátum (.sub):** A MicroDVD formátum .sub fájlokat használ, és minden felirat bejegyzéshez időzítési információkat és szöveget tartalmaz. Gyakran használják médialejátszókkal és videószerkesztő szoftverekkel.
- **DVD-feliratok (.sub és .idx):** A DVD-feliratok általában két fájlból állnak: a .sub fájlból, amely feliratszöveget tartalmaz, és .idx fájlból, amely az időzítési és formázási információkat tartalmazza.
- **WebVTT (.vtt):** A WebVTT egy webes videókhoz használt feliratformátum, amelyet általában HTML5-videólejátszókban használnak, és támogatja az alapvető formázási beállításokat.
- **MPL2 feliratformátum (.mpl):** Az MPL2 fájlok az MPlayerrel, a Unix-szerű rendszerekhez készült médialejátszóval használatosak, és időbélyeggel és szöveggel ellátott feliratokat tartalmaznak.
- **iTunes időzített szöveg (.itt):** Az iTunes időzített szövegfájljait az Apple iTunes és más Apple platformok feliratozására használják. Támogatják az olyan funkciókat, mint a szövegstílus és a pozicionálás.
- **Teletext-feliratformátum (.srt vagy .txt):** A teletext-feliratokat általában a televíziós műsorszórásban használják. Általában egyszerű szöveges fájlokként kerülnek mentésre .srt vagy .txt kiterjesztéssel.

## Hogyan lehet megnyitni a SUB fájlt?

A következő médialejátszók megnyithatják a SUB fájlt feliratsávként.

- VideoLAN VLC médialejátszó
- MPlayer

A SUB fájl VLC lejátszóban való megnyitásához kövesse az alábbi lépéseket

- Nyissa meg a VLC lejátszót, és játssza le a videót
- A VLC Media Player menüsorában válassza a **Feliratok > Feliratfájl hozzáadása...** lehetőséget.
- Keresse meg a SUB fájlt, és nyissa meg

Ha szerkesztenie kell a SUB fájlt, bármelyik szövegszerkesztővel megnyithatja, pl. Microsoft Notepad (Windows) vagy Apple TextEdit (Mac).

## Hivatkozások
* [MicroDVD](https://en.wikipedia.org/wiki/MicroDVD)

