{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ATOM fájl – Atom szindikációs formátum",
  "description" :"További információ arról, hogy mi az ATOM-fájl és az API-k, amelyek ATOM-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ATOM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## Mi az ATOM fájl?

Az ATOM-fájl egy szindikációs formátum az Atom feed- és bejegyzési dokumentumok szerkezetéhez. Az .RSS fájlokhoz hasonlóan az ATOM fájlformátum egy XML-alapú terjesztési formátum, amely a tartalom közzétételének szabványa. Egy ATOM-fájlt használnak a webes hírcsatornákhoz, amelyek lehetővé teszik a szoftverprogramok számára, hogy ellenőrizzék a webhelyen közzétett frissítéseket. Különböző típusú bejegyzéseket tartalmaz, például címsorokat, teljes szövegű cikkeket, kivonatokat vagy hivatkozásokat a webhely tartalmára

Az **ATOM-fájlokat** megnyitni képes alkalmazások közé tartozik az **Apple Safari**.

## ATOM fájlformátum – További információ

Az ATOM fájlokat a népszerű XML fájlformátumban tárolják és teszik közzé, amely az információcsere univerzális formátuma. Az RSS alternatívájaként fejlesztették ki, szem előtt tartva az RSS fájlformátum korlátait és hibáit.

### Az atomdokumentumok típusai

1. "Atom belépési dokumentumok" - Ez egy XML-dokumentum, amely egyetlen információból, néven bejegyzésből áll az Atom feedhez. Van benne egy atom:entry elem, amely számos gyermek elemet tartalmaz. Az Atom bejegyzés tartalma lehet egyszerű szöveg, HTML, XHTML vagy más IANA (Internet Assigned Numbers Authority) médiatípus.
1. "Atom Feed Documents" – Ez egy XML-dokumentum, amely metaadatokat tartalmaz egy Atom feedről és egy vagy több bejegyzést a hírfolyamhoz. Amikor egy kliens információkérést kér a hírfolyamból, a hírcsatorna-dokumentumot a szerver hozza létre, amely számos Atom-bejegyzést tartalmaz a kérés teljesítéséhez.
1. "Atom Collection" – Ez egy speciális típusú Atom feed dokumentum, amely tartalmazza a szerkeszthető Atom bejegyzések URL-címét.

## Hivatkozások

* [Atom Syndication Format – RFC](https://www.rfc-editor.org/rfc/rfc4287.html)
* [Az Atom feedek áttekintése – IBM](https://www.ibm.com/docs/en/cics-ts/5.4?topic=support-overview-atom-feeds)
* [Atom – Web Standard](https://en.wikipedia.org/wiki/Atom_(web_standard))

