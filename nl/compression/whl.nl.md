{
  "date" : "2022-06-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WHL-bestandsindeling - Python Wheel-pakketbestand",
  "description":"Meer informatie over WHL-bestandsindeling en API's die WHL-bestanden kunnen maken en openen.",
  "linktitle" : "WHL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-29"
}

## Wat is een WHL-bestand?

Een WHL-bestand (Wheel) is een distributiepakketbestand dat is opgeslagen in het wielformaat van Python. Het is een standaard installatie van Python-distributies en bevat alle bestanden en metadata die nodig zijn voor de installatie. Het WHL-bestand bevat ook informatie over de Python-versies en platforms die door dit wielbestand worden ondersteund. Net als bij een [MSI](/nl/executable/msi/) installatiebestand, is het WHL-bestandsformaat een kant-en-klaar formaat waarmee het installatiepakket kan worden uitgevoerd zonder de brondistributie te bouwen.

## WHL-bestandsindeling

WHL-bestandsindeling is een [ZIP](/nl/compression/zip/) (.zip)-archief dat alle installatiebestanden en metadata bevat die installatieprogramma's nodig hebben voor de installatie van een pakket. Deze WHL-bestanden kunnen worden uitgepakt met behulp van de unzip-optie of standaard decompressiesoftwaretoepassingen zoals WinZIP en WinRAR.

### WHL-bestandsnaamconventie

Een WHL-bestand wordt genoemd volgens de volgende conventie.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

Een voorbeeld van de WHL-bestandsnaam is als volgt.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

* `cryptografie` is de pakketnaam.
* `2.9.2` is de pakketversie van cryptografie. Een versie is een PEP 440-compatibele string zoals 2.9.2, 3.4 of 3.9.0.a3.
* `cp35` is de Python-tag en geeft de Python-implementatie en -versie aan die het wiel vereist.
* `abi3` is de ABI-tag. ABI staat voor Application Binary Interface.
* `macosx_10_9_x86_64` is de platformtag, wat nogal een mondvol is.

## Referenties

* [Wat zijn Python Wheels en waarom zou het je iets kunnen schelen?](https://realpython.com/python-wheels/)
* [Python-wiel](https://pypi.org/project/wheel/)

