{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRL fájl – Tanúsítvány visszavonási lista",
  "description":"További információ a CRL-fájlformátumról és az API-król, amelyek CRL-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CRL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-01"
}

## Mi az a CRL fájl?

A CRL (Certificate Revocation List) fájl az X.509 digitális tanúsítványok feketelistája, amelyet a tanúsító hatóság (CA) a hozzárendelt visszavonási dátum előtt visszavon. Információkat tartalmaz a problémáról és a visszavonás dátumáról, amely lehetővé teszi a biztonsági rendszergazdák számára, hogy blokkolják az érintett digitális tanúsítványokat. A CRL nem tartalmazza a lejárt tanúsítványokat, mivel fő célja a nem megbízható és érvénytelen tanúsítványok értesítése.

A **CRL-fájlok megnyitására** képes alkalmazások közé tartozik az OpenSSL, a Microsoft IIS Server és a Citrix NetScaler.

## CRL fájlformátum – További információ

A CRL fájlok az X.509 szabványban foglalt információkat tartalmaznak, amely meghatározza a nyilvános kulcsú információk megosztásának szemantikáját is. A CRL-fájlban található egyéb információk magukban foglalhatják a tanúsítványok visszavonásának időtartamát, a visszavonás indokát, a visszavont tanúsítvány sorozatszámát és az időbélyeget.


### A tanúsítványok CRL-hez való hozzáadásának legfőbb okai

Számos oka lehet annak, hogy webhelye tanúsítványát visszavonják, és hozzáadják a CRL-hez. Némelyikük lehet;

1. Tanúsítványának privát kulcsát feltörték
1. Az Ön tanúsítványa nem érvényes, vagy a CA tévesen állította ki
1. A tanúsítvánnyal kapcsolatos szervezeti adatok módosulnak, és a CA új tanúsítványt ad ki
1. Minden egyéb elháríthatatlan ok, amely miatt a tanúsítványt visszavonták

## Hivatkozások

* [National Institute of Standards and Technology (NIST)](https://csrc.nist.gov/glossary/term/CRL)
* [Internet Engineering Task Force (IETF) RFC 5280](https://tools.ietf.org/html/rfc5280)
* [A tanúsítványok visszavonási listája](https://en.wikipedia.org/wiki/Certificate_revocation_list)

