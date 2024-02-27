{
  "date": "2021-04-08",
  "keywords": [
"dar fil",
"dar filformat",
"hvad er en dar-fil",
"fil",
"dar eksempel",
"dar filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DAR - Disk Archiver File Format",
  "description": "Lær om DAR-filformat og API'er, der kan oprette og åbne DAR-filer.",
  "linktitle": "DAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-da-dar"
}
},
  "lastmod": "2021-04-09"
}

## Hvad er en DAR fil?

En fil med filtypen .dar er et komprimeret arkiv, der er oprettet ved hjælp af DAR Disk-arkivet. Det kan oprette backup/arkiv til fuld disk eller en gruppe filer. Det blev oprettet for at erstatte filformatet [TAR](/compression/tar/) på UNIX OS og kan oprettes som delte arkivfiler for et stort antal filer. DAR-arkiv understøtter mulighed for at slette filer fra systemet, som er knyttet til hovedfilerne i arkivet. Dens muligheder for at levere differentiel, inkrementel og dekrementel backup gør den overlegen end TAR-filer.

## DAR filformat

DAR-filer er komprimerede arkiver, der kan bruge enhver komprimering pr. fil, såsom [gzip](/compression/gz/), [bzip2](/compression/bz2/), lzo, xz eller lzma. Det nøjagtige filformat for en DAR-fil afhænger af, hvilken type formatering der bruges til at komprimere indholdet af arkivet. Det tillader også valgfri Blowfish, Twofish, AES, Serpent, Camellia-kryptering og offentlig nøglekryptering og signatur (OpenPGP).

### DAR-funktioner

Nogle af funktionerne i DAR-filformatet er som følger.

 * Tager sig af enhver form for inode (mappe, almindelige filer, symbolske links, specielle enheder, navngivne rør, stikkontakter, døre, ...)
 * Tager sig af hårdt-linkede inoder (hard-linkede almindelige filer, char-enheder, blokenheder, hard-linkede symlinks)
 * Tager sig af sparsomme filer
 * Tager sig af Linux-fil Extended Attributes,
 * Tager sig af Linux-fil ACL
 * Tager sig af Mac OS X-filgafler
 * Tager sig af nogle filsystemspecifikke attributter som fødselsdato for HFS+ filsystem og uforanderlige, datajournalføring, sikker-sletning, no-tail-fletning, undeleteable, noatime-attributter for ext2/3/4 filsystem.
 * Per-fil komprimering med gzip, bzip2, lzo, xz eller lzma (i modsætning til at komprimere hele arkivet). En person kan vælge ikke at komprimere allerede komprimerede filer baseret på deres filnavnsuffiks.
 * Hurtig udpakning af filer fra hvor som helst i arkivet
 * Hurtig liste over arkivindhold ved at gemme kataloget over filer i arkivet
 * Live filsystem backup: registrerer, når en fil er blevet ændret, mens den blev læst til backup, og kan prøve at gemme den op til et givet maksimalt antal genforsøg
 * Hash-fil (MD5, SHA1 eller SHA-512) genereret on-fly for hver skive, den resulterende fil er kompatibel med md5sum eller sha1sum, for hurtigt at kunne kontrollere hver skives integritet
 * Filsystemuafhængig: det kan bruges til at gendanne et system til en partition af en anden størrelse og/eller til en partition med et andet filsystem[5]

## Referencer

* [DAR](http://dar.linux.free.fr/)

* [DAR Disk Archiver](https://en.wikipedia.org/wiki/Dar_(disk_archiver))


