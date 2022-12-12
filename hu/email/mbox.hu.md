{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MBOX - E-mail postafiók fájl",
  "description":"További információ az MBOX fájlformátumról és az MBOX fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "MBOX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az MBOX fájl?

Az MBox fájlformátum egy általános kifejezés, amely az elektronikus levelek gyűjtésére szolgáló tárolót jelöli. Az üzenetek a tárolóban tárolódnak a mellékletekkel együtt. A teljes mappából származó üzenetek egyetlen adatbázisfájlba kerülnek, az új üzenetek pedig a fájl végéhez fűződnek. Számos alkalmazás és API támogatja az MBox fájlformátumokat, például az Apple Mail és a Mozilla Thunderbird.

## MBOX fájlformátum ##

Az MBox fájlformátum meglehetősen hosszú ideig nem szabványosított 2005-ig, amikor is az alkalmazást/mboxot [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) üzenetként szabványosították, RFC 2822 formátumban , egymás után fűződnek össze MBox fájlformátumban. Minden üzenet egy elválasztó sorral kezdődik, amely azonosítja az üzenet feladóját, valamint azt a dátumot és időpontot, amikor az üzenetet a végső címzett megkapta (akár az utolsó ugrás rendszere az átviteli útvonalon, akár a címzett címzettjeként szolgáló rendszer mailstore). Minden üzenetet általában egy üres sor zár le. Az adatbázis végét általában a további adatok hiánya, vagy egy kifejezett fájlvégi jelölő jelenléte jelzi.

## Üzenet olvasása a ## MBox fájlból

Egy olvasó egy mbox fájlt keres, és a From_ sorokat keresi. Bármely From_ sor az üzenet kezdetét jelzi. Az olvasó ne próbálja kihasználni azt a tényt, hogy minden From_ sor (a fájl eleje után) üres sor. Amint az olvasó megtalál egy üzenetet, a Feladó_ sorból kiemeli a boríték feladóját és a kézbesítés dátumát (esetleg sérült). Ezután a következő From_ sorig vagy a fájl végéig olvas, attól függően, hogy melyik következik be előbb. Lehúzza az utolsó üres sort, és törli a >From_ lines és a >>From_ lines idézetét és így tovább. Az eredmény egy RFC 822 üzenet.

## Kódolási szempontok ##

Egy MBox-fájl tartalma visszafordíthatatlanul összekeveredhet, ha egy fogadott e-mail mellékletként Mbox-fájlt tartalmaz, és egy másik Mbox-fájlba menti. Ennek elkerülése érdekében az üzenetkezelő rendszereknek egy mbox adatbázist nem átlátszó átviteli kódolással (például BASE64 vagy Quoted-Printable) kell kódolniuk, amikor egy ilyen objektumot üzenetküldési protokollokon keresztül továbbítanak. Az implementátoroknak fel kell készülniük arra is, hogy az mbox adatokat helyileg kódolják, ha nem megfelelő adat érkezik.

## Hivatkozások ##

* [MBox – RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)
* [Mbox – Wikipédia](https://en.wikipedia.org/wiki/Mbox)

