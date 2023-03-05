{
  "date" : "2019-10-11",
  "keywords" :[ "mhtml", "mhtml fájl", "mhtml fájlformátum", "mhtml fájltípus", "fájl", "típus", "mi az mhtml fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHTML - MIME HTML fájl",
  "description":"További információ az MHTML fájlformátumról és az MHTML-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "MHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az MHTML fájl?

Az MHTML kiterjesztésű fájlok olyan weboldal-archívum formátumot képviselnek, amelyet számos különböző alkalmazás hozhat létre. A formátumot archív formátumnak nevezik, mivel egyetlen fájlba menti a web **[HTML](/hu/web/html/)** kódot és a kapcsolódó erőforrásokat. Ezek az erőforrások magukban foglalnak mindent, ami a weboldalhoz kapcsolódik, például képeket, kisalkalmazásokat, animációkat, hangfájlokat és így tovább. Az MHTML-fájlok számos alkalmazásban megnyithatók, például az Internet Explorerben és a Microsoft Wordben. A Microsoft Windows MHTML fájlformátumot használ a problémákat felvető Windows-alkalmazások használata során észlelt problémák forgatókönyveinek rögzítésére. Az MHTML fájlformátum az oldal tartalmát az message/rfc822-ben meghatározott specifikációkhoz hasonlóan kódolja, amely egyszerű szöveges e-mailekkel kapcsolatos specifikációk. A formátum tényleges specifikációit az [RFC 2557](https://tools.ietf.org/html/rfc2557) részletezi.

## MHTML fájlformátum

Az MHTML az összesített HTML dokumentumok MIME Encapsulation néven is ismert, mivel képes HTML weboldalakat és erőforrásait egyetlen webarchívumba kódolni. Az RFC 2557 specifikációi szerint az összesített dokumentum egy MIME-kódolású üzenet, amely tartalmaz egy gyökér erőforrást (objektumot), valamint más erőforrásokat, amelyek URI-kon keresztül kapcsolódnak hozzá. Ilyen egyéb források lehetnek beágyazott képek, stíluslapok, kisalkalmazások stb. megjelenítése. Ezen túlmenően ezek más multimédiás dokumentumok gyökerei is lehetnek. Az MHTML-fájlformátumra vonatkozó teljes dokumentumspecifikáció az [RFC 2557]-ben (https://tools.ietf.org/html/rfc2557) található, és az ilyen fájlformátum olvasásához/írásához szükséges bármilyen alkalmazásfejlesztéshez hivatkozni kell rá. A szabvány előírja, hogy a hivatkozni kívánt testrészek vagy Content-ID, vagy Content-Location segítségével azonosíthatók.

### MIME tartalomfejlécek

A MIME tartalomfejléce, a Content-Location, a más törzsrészekben található erőforrásokra mutató URI hivatkozások feloldására szolgál. Ez a fejléc bármely üzenet vagy tartalom fejlécében előfordulhat.

### Tartalom-hely fejléc

A Content-Location egy URI reprezentációja, amely felcímkézi egy testrész tartalmát, ahol elhelyezték. Értéke lehet abszolút vagy relatív URI. Használható olyan erőforrások címkézésére, amelyeket az üzenet egyes vagy valamennyi címzettje nem tud visszakeresni. Egyetlen üzenetnek csak egyetlen Content-Location fejléce lehet. Példa egy többrészes/kapcsolódó szerkezetre, amely testrészeket tartalmaz Content-Location és Content-ID címkékkel is:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### MHTML-aggregátumok URI-i

Az MHTML aggregátum URI-ja eltér a gyökér-URI-étól. A Content-Location fejléc mezőt a teljes összesítésre kell alkalmazni, ha többrészes/kapcsolódó címsor fejlécében használják. Hasonlóképpen, a beolvasott erőforrások halmaza eltérhet a részei Content-Locations használatával lekért erőforráskészlettől, ha az MHTML-aggregátumra hivatkozó URI-t használják ennek az aggregátumnak a lekérésére. Például egy MHTML aggregátum lekérése egy régi verziót ad vissza, míg a gyökér URI és a soron belüli linkelt objektumok lekérése egy újabb verziót.

## Hivatkozások

* [Aggregate Documents MIME Encapsulation of Aggregate Documents – RFC 2557](https://tools.ietf.org/html/rfc2557)
* [MHTML fájlformátum – a Wikipédia által](https://en.wikipedia.org/wiki/MHTML)

