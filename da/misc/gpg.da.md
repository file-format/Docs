{
  "date": "2022-02-17",
  "keywords": [
"gpg-fil",
"gpg filformat",
"hvad er en gpg-fil",
"fil",
"gpg eksempel",
"gpg filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GPG-fil - GNU Privacy Guard Public Keyring File",
  "description": "Lær om GPG-filer og API'er, der kan oprette og åbne GPG-filer.",
  "linktitle": "GPG",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-gp-dag"
}
},
  "lastmod": "2022-02-17"
}

## Hvad er en GPG fil?

En GPG-fil er en krypterings-/dekrypteringsnøglefil, der bruges af GNU Privacy Guard (GnuPG) krypteringsprogrammet. Selve GnuPC-programmet er baseret på OpenPGP-standarden som defineret RFC4880 og er også kendt som PGP. Nøglen til vellykket brug af GPG i moderne operativsystemer er dets alsidige nøglestyringssystem. Kommandolinjeværktøjet til GPG lader det nemt integreres med andre applikationer.

## GPG filformat

GPG-filer gemmes som krypterede binære filer, og de er selvfølgelig ikke læselige af mennesker. For at dekryptere en krypteret GPG-fil skal du bruge den samme sikre nøgle. Og derfor er det interne filformat for disse filer ikke kendt.

## Krypter og dekrypter filer med GPG på Linux

GPG-kommandolinjeværktøjet kan bruges til at kryptere og dekryptere filer på Linux.

### Kryptering af en fil

En fil kan krypteres ved hjælp af gpg-kommandoen med -c (create)-indstillingen som vist nedenfor.

```
gpg -c file1.txt
```
Kørsel af denne kommando beder du om en nøglesætning til at kryptere indholdet af den originale fil `fil1.txt`. Dette resulterer i oprettelsen af den krypterede fil file1.txt.gpg.

### Dekryptering og udpakning af en fil

For at dekryptere og udpakke en krypteret fil kan følgende kommando bruges.

```
gpg cfile.txt.gpg
```

## Referencer

* [GNUPG](https://gnupg.org/)

* [HDF - Wikipedia](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)


