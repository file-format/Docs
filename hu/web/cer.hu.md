{
  "date" : "2021-07-13",
  "keywords" :[ "CER", "extension", "file", "format", "web", "certificate", "language" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CER - Tanúsítványfájl formátum",
  "description":"További információ a CER fájlformátumról és az API-król, amelyek CER-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CER",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Mi az a CER fájl? ##

A .cer kiterjesztésű fájl a tulajdonosi tanúsítványra és az adott nyilvános kulcsra vonatkozó információk tárolásáért felelős. Ez a fájlformátum nem tudja tárolni a privát kulcsokat, és csak egy tanúsítvány tárolására képes, amely x509. A kifejezetten biztonságos tanúsító hatóságok azok, amelyek a HTTPS-hez, egy megbízható és biztonságos böngészési protokollhoz tartoznak
A CER a szerver tanúsítványa. Általában a domain tanúsító hatósága kapja meg. A CER többnyire megegyezik a [CRT]-vel (/hu/web/crt/), bár mindkettő azonos formátumú SSL-tanúsítvány, de eltérő fájlnévkiterjesztések.
Ezeket az operációs rendszereken úgy lehet használni, hogy egyszerűen megnyit egy böngészőt, és ellenőrzi a használt böngésző vagy webhely biztonságát.

## Rövid története ##

1995-ben Thawte lett az első hitelesítési hatóság az Egyesült Államokon kívüli nyilvános SSL (secure socket link) tanúsítványok kérdésének megoldásában. Ezt követően van egy sor ilyen hatóság, amelyet 1995 és 2020 között alapítottak.

## CER fájlformátum ##

Ezek a fájlok lehetnek egyszerűen
* A PKC S#7 Base64 ASCII kódolást tartalmaz
* Fájlkiterjesztései p7b vagy p7cZ
* Bináris tartalom esetén a tanúsítvány DER vagy pkcs12/pfx.
Sokféle tanúsítványfájl létezik néhány egyedi specifikációval:
* .pem, amikor egy szervezet ezt a formátumot láncolva használja, jól ismert, hogy tanúsítványokat hoz létre
* .arm, amikor a tanúsítvány kinyerésének módja az önaláírást segíti, szükséges, az erre a célra megadott formátum az .arm. Base-64 ASCII kódolásban van ábrázolva.
* .der, Bináris adatokból áll. Ez azt jelenti, hogy csak egyetlen tanúsítványhoz használható
* .pfx (PKC512), A CA által kiadott tanúsítványnak megfelelő privát kulcsból vagy egy önaláírt tanúsítványból áll. Ez a formátum jól ismert az egyik SSL-megvalósítás másikra való átalakításáról.


