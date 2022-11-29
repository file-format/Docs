{
  "date" : "2022-02-17",
  "keywords" :["gpg-fil", "gpg-filformat", "vad är en gpg-fil", "fil", "gpg-exempel", "gpg-filtillägg", "tillägg", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPG-fil - GNU Privacy Guard Public Keyring File",
  "description":"Läs mer om GPG-filer och API:er som kan skapa och öppna GPG-filer.",
  "linktitle" : "GPG",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-17"
}

## Vad är en GPG fil?

En GPG-fil är en krypterings-/dekrypteringsnyckelfil som används av krypteringsprogrammet GNU Privacy Guard (GnuPG). Själva GnuPC-programmet är baserat på OpenPGP-standarden enligt definitionen RFC4880 och är även känd som PGP. Nyckeln till framgångsrik användning av GPG i moderna operativsystem är dess mångsidiga nyckelhanteringssystem. Kommandoradsverktyget för GPG låter det enkelt integreras med andra applikationer.

## GPG filformat

GPG-filer sparas som krypterade binära filer och de är naturligtvis inte läsbara för människor. För att dekryptera en krypterad GPG-fil måste du använda samma säkra nyckel. Och det är därför det interna filformatet för dessa filer inte är känt.

## Kryptera och dekryptera filer med GPG på Linux

Kommandoradsverktyget GPG kan användas för att kryptera och dekryptera filer på Linux.

### Kryptera en fil

En fil kan krypteras med kommandot gpg med alternativet -c (skapa) som visas nedan.

```
gpg -c file1.txt
```
Att köra det här kommandot frågar efter en nyckelfras för att kryptera innehållet i originalfilen `fil1.txt`. Detta resulterar i skapandet av den krypterade filen file1.txt.gpg.

### Dekryptera och extrahera en fil

För att dekryptera och extrahera en krypterad fil kan följande kommando användas.

```
gpg cfile.txt.gpg
```

## Referenser

* [GNUPG](https://gnupg.org/)
* [HDF - Wikipedia](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)

