{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTACCESS fájl - Apache HTACCESS fájlformátum",
  "description" :"Az Ön fájlformátumának útmutatója a HTACCESS fájl megismeréséhez",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a HTACCESS fájl?

A HTACCESS fájl egy Apache konfigurációs fájl, amely lehetővé teszi a konfiguráció módosítását a webhelyek különböző mappáiban/könyvtáraiban. Konfigurációs direktívákat tartalmaz, amelyek a címtárra és az alkönyvtárra vonatkoznak.

A HTACCESS fájl számos ellenőrzést végez, például meghatározza a webhely indexoldalát, felsorolja a 404-es (Oldal nem található) hibaoldalt, végrehajtja a 301-es vagy 302-es oldalátirányítást, blokkolja a hozzáférést egy adott IP-címről vagy más webhelyekről. A .htaccess fájlok használata tehát lelassítja az Apache HTTP szerver általános teljesítményét.

## HTACCESS fájlformátum

A HTACCESS fájlok egyszerű szöveges fájlformátumban kerülnek a lemezre. Ez azt jelenti, hogy ezeket a fájlokat bármilyen szövegszerkesztőben megnyithatja és szerkesztheti. A "." előtt nincs név egy .htaccess fájlban, jelezve, hogy ez egy rejtett fájl a mappán belül.

## A HTACCESS fájl gyakori használata

A HTACCESS fájl öt gyakori felhasználási módja a következő.

### Mod_Rewrite

A HTACCESS fájl segítségével kijelölhető és módosítható, hogy a webhelyen lévő URL-ek és weboldalak hogyan jelenjenek meg a felhasználók számára.

### Hitelesítés

A hitelesítés a .htaccess segítségével érhető el egy .htpasswd nevű passowrd fájl létrehozásával. Ez lehetővé teszi a webhely látogatói számára, hogy jelszót adjanak meg, ha meg szeretnének látogatni a weboldal egy bizonyos részét.

### Egyéni hibaoldalak

Létrehozhat egyéni hibaoldalakat, például 400-as hibás kérelem, 401-es engedélyezés szükséges, 403-as tiltott oldal, 404-es fájl nem található és 500-as belső hiba .htaccess fájllal. Ezek azonban lelassítják a szerver teljesítményét, mivel az összes ellenőrzés végrehajtásra kerül az oldalak elérésekor.

### MIME típusok

Az Apache HTACCESS fájlok módosíthatók, hogy tartalmazzák a többcélú internetes levelezési kiterjesztés (MIME) típusait. Ez lehetővé teszi, hogy a szerver támogassa a webhely által nem támogatott alkalmazásfájlok kézbesítését.

### SSI

A Server Side Includes (SSI) nagyszerű időmegtakarítást jelent egy webhelyen. Az SSI engedélyezhető a következő hte kód beszúrásával a .htaccess fájlba.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Apache HTACCESS fájl példa

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## Hivatkozások

* [Apache HTTP Server oktatóanyag: .htaccess fájlok](https://httpd.apache.org/docs/current/howto/htaccess.html)

