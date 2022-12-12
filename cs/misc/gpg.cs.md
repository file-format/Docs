{
  "date" : "2022-02-17",
  "keywords" :["soubor gpg", "formát souboru gpg", "co je soubor gpg", "soubor", "příklad gpg", "přípona souboru gpg", "přípona", "formát"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPG File - GNU Privacy Guard Public Keyring File",
  "description":"Další informace o souboru GPG a rozhraních API, která mohou vytvářet a otevírat soubory GPG.",
  "linktitle" : "GPG",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-17"
}

## Co je soubor GPG?

Soubor GPG je soubor šifrovacího/dešifrovacího klíče, který používá šifrovací program GNU Privacy Guard (GnuPG). Samotný program GnuPC je založen na standardu OpenPGP definovaném RFC4880 a je také známý jako PGP. Klíčem k úspěšnému použití GPG v moderním operačním systému je jeho všestranný systém správy klíčů. Nástroj příkazového řádku GPG umožňuje snadnou integraci s jinými aplikacemi.

## Formát souboru GPG

Soubory GPG se ukládají jako zašifrované binární soubory a samozřejmě nejsou čitelné pro člověka. Chcete-li dešifrovat zašifrovaný soubor GPG, musíte použít stejný bezpečnostní klíč. A to je důvod, proč není znám vnitřní formát souborů těchto souborů.

## Šifrujte a dešifrujte soubory pomocí GPG v systému Linux

Nástroj příkazového řádku GPG lze použít k šifrování a dešifrování souborů v systému Linux.

### Šifrování souboru

Soubor lze zašifrovat pomocí příkazu gpg s volbou -c (vytvořit), jak je uvedeno níže.

```
gpg -c file1.txt
```
Spuštění tohoto příkazu vyžaduje klíčovou frázi, pomocí které se zašifruje obsah původního souboru `file1.txt`. Výsledkem je vytvoření zašifrovaného souboru file1.txt.gpg.

### Dešifrování a rozbalení souboru

K dešifrování a extrahování zašifrovaného souboru lze použít následující příkaz.

```
gpg cfile.txt.gpg
```

## Reference

* [GNUPG](https://gnupg.org/)
* [HDF – Wikipedie](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)

