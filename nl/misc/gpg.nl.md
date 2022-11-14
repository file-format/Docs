{
  "date" : "2022-02-17",
  "keywords" :["gpg file", "gpg file format", "wat is een gpg file", "file", "gpg example", "gpg file extension","extension", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPG-bestand - GNU Privacy Guard openbaar sleutelhangerbestand",
  "description":"Meer informatie over GPG-bestanden en API's die GPG-bestanden kunnen maken en openen.",
  "linktitle" : "GPG",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-17"
}

## Wat is een GPG-bestand?

Een GPG-bestand is een coderings-/decoderingssleutelbestand dat wordt gebruikt door het coderingsprogramma GNU Privacy Guard (GnuPG). Het GnuPC-programma zelf is gebaseerd op de OpenPGP-standaard zoals gedefinieerd in RFC4880 en staat ook bekend als PGP. De sleutel tot succesvol gebruik van GPG in een modern besturingssysteem is het veelzijdige sleutelbeheersysteem. Met het opdrachtregelhulpprogramma van GPG kan het eenvoudig worden geïntegreerd met andere applicaties.

## GPG-bestandsindeling

GPG-bestanden worden opgeslagen als versleutelde binaire bestanden en zijn natuurlijk niet door mensen leesbaar. Om een versleuteld GPG-bestand te decoderen, moet u dezelfde beveiligde sleutel gebruiken. En daarom is het interne bestandsformaat van deze bestanden niet bekend.

## Versleutel en ontsleutel bestanden met GPG op Linux

Het GPG-opdrachtregelhulpprogramma kan worden gebruikt om bestanden op Linux te coderen en te decoderen.

### Een bestand versleutelen

Een bestand kan worden versleuteld met behulp van het gpg-commando met de -c (create) optie zoals hieronder getoond.

```
gpg -c file1.txt
```
Het uitvoeren van dit commando vraagt om een sleutelzin waarmee de inhoud van het originele bestand `file1.txt` moet worden versleuteld. Dit resulteert in het aanmaken van het versleutelde bestand file1.txt.gpg.

### Een bestand decoderen en uitpakken

Om een versleuteld bestand te decoderen en uit te pakken, kan de volgende opdracht worden gebruikt.

```
gpg cfile.txt.gpg
```

## Referenties

* [GNUPG](https://gnugg.org/)
* [HDF - Wikipedia](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)

