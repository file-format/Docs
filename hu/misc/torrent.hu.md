{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Torrent fájlformátum - BitTorrent fájl",
  "description":"További információ a TORRENT fájlokról és API-król, amelyek TORRENT fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
      "identifier":"misc-torrent",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Mi az a TORRENT fájl?

A TORRENT fájl egy szöveges fájl, amelyet a BitTorrent és más P2P (peer-to-peer) programok használnak letöltésre és tartalomcserére. A letölthető tartalom tartalmazhat dokumentumokat, videókat, játékokat, filmeket és más, az interneten elérhető médiát. Metaadat-információkat tartalmaz a letöltendő média tartalmáról és helyéről. A BitTorrenthez hasonló szoftverek a fájlból származó információkat, például nevet, fájlméretet és mappaszerkezetet használnak az adatok letöltéséhez. A Torrent fájlok más fájlformátumokká konvertálhatók, például [PDF](/hu/pdf/) online.

## Mi az a torrentezés? A TORRENT fájlformátum az adatcseréhez

A torrentezés az adatfájlok cseréjének (le- és feltöltésének) fogalma a BitTorrent hálózaton keresztül. Ellentétben a hagyományos szerverekkel, ahol az adatokat feltöltik mások eléréséhez és letöltéséhez, a torrent fájlokat a torrent hálózaton keresztül kérik le és küldik el. Amikor a felhasználó megnyit egy .torrent fájlt olyan alkalmazásokban, mint a BitTorrent, a szoftver megkezdi a fájl tartalmának bitenkénti letöltését. Ha több felhasználó rendelkezik ugyanazzal a fájllal, a BitTorrent felosztja a letöltéseket az összes felhasználó között, hogy felgyorsítsa a letöltési folyamatot. Ezzel egyidejűleg a fájlt letöltő felhasználó számítógépe is a fájl forrásává válik, hogy elküldje azt más felhasználóknak, akik szintén letöltik ugyanazt a fájlt.

### A TORRENT fájl szerkezete

A torrent fájl fájlok listájának és a letöltendő fájl összes részével kapcsolatos metaadat-információ kombinációja. A következő információkat tartalmazza kulcsok formájában.

- "announce" - A nyomkövető URL-címe, amelyet a többi partnernek közölnek, hogy tájékoztassák a fájl elérhetőségéről
- "Infó" - Ez egy olyan szótárhoz kapcsolódik, amelynek kulcsai attól függnek, hogy egy vagy több fájl meg van-e osztva:
  - files—a list of dictionaries each corresponding to a file (only when multiple files are being shared). Each dictionary has the following keys:
- "hosszúság" — a fájl mérete bájtban.
- "elérési út" - az alkönyvtárneveknek megfelelő karakterláncok listája, amelyek közül az utolsó a tényleges fájlnév
- "hosszúság" – a fájl mérete bájtban (csak egy fájl megosztása esetén)
- `név` — fájlnév, ahová a fájlt menteni kell
- "darab hossza" – darabonkénti bájtok száma. Ez általában 28 KiB = 256 KiB = 262 144 B.
- "darabok" – egy hash lista, amely az egyes darabok SHA-1 hasheinek összefűzése.

## A torrentezés biztonságos és legális?

A P2P-felhasználók közötti adatcserére szolgáló torrentezési protokoll biztonságos, mivel ez csak az eszköz bármilyen típusú fájl megosztására. Így maga a protokoll nem biztonságos vagy illegális. A hálózaton keresztül megosztott tartalom azonban olyan fájlokat vagy adathordozókat tartalmazhat, amelyek sérthetik a megosztott dokumentumok jogi státuszát. Ebben az esetben az ilyen adatok cseréje jogi lépéseket vonhat maga után az ilyen fájlok nyilvános megosztásában érintett felekkel szemben.

## Hivatkozások

* [TORRENT-fájl – wikipedia](https://en.wikipedia.org/wiki/Torrent_file)

