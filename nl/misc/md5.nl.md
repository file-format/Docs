{
  "date" : "2021-07-29",
  "keywords" :[ "md5-bestand", "md5-bestandsindeling", "wat is een md5-bestand", "bestand", "md5-voorbeeld", "md5-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD5 - MD5 Checksum-bestand",
  "description":"Meer informatie over MD5-bestanden en API's die MD5-bestanden kunnen maken en openen.",
  "linktitle" : "MD5",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## Wat is een MD5-bestand?

Een MD5-bestand is een controlesombestand dat wordt gebruikt voor de verificatie van de integriteit van een bestand. Het is vergelijkbaar met een vingerafdruk voor het bijbehorende bestand en wordt op unieke wijze gegenereerd met behulp van een algoritme dat het aantal bits in het bestand gebruikt. Het wordt gebruikt om het bestand te verifiëren met software zoals [md5sum](http://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html). Een voordeel van het gebruik van MD5-bestanden is om te controleren of de gedownloade bestanden niet beschadigd zijn.

## MD5-bestandsindeling - Meer informatie

Gewoonlijk wordt een MD5-bestand opgeslagen met dezelfde naam als de oorspronkelijke bestandsnaam, maar met de extensie .md5. Als de bijbehorende bestandsnaam bijvoorbeeld `abc_987_123456.grb` is, is de bijbehorende MD5-bestandsnaam `abc_987_123456.grb.md5`. MD5-bestanden helpen bij het identificeren dat een ontvangen of gedownload bestand niet is beschadigd of aangetast door schadelijke inhoud. Kortom, MD5-bestanden garanderen de volledigheid van een bestand.


## Hoe MD5 Checksum controleren?

Een enkel bestand kan als volgt worden gecontroleerd/geverifieerd voor MD5 met behulp van de [md5sum](https://en.wikipedia.org/wiki/Md5sum) tool.

```
md5sum -c abc_987_123456.grb.md5
```

## Referenties

* [md5sum - Wikipedia](https://en.wikipedia.org/wiki/Md5sum)

