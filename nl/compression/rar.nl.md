{
  "date" : "2019-10-11",
  "keywords" :[ "rar-bestand", "rar-bestandsformaat", "wat is een rar-bestand", "bestand", "rar-voorbeeld", "rar-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RAR",
  "description":"Wat is een RAR-bestandsextensie en API's die RAR-bestanden kunnen maken en openen.",
  "linktitle" : "RAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een RAR-bestand?

Bestanden met de extensie .rar zijn archiefbestanden die zijn gemaakt voor het opslaan van informatie in gecomprimeerde of normale vorm. RAR, wat staat voor Roshal ARchive-bestandsindeling, is een eigen bestandsindeling die in 1995 is gemaakt door Eugene Roshal, een Russische software-ingenieur. Het formaat wordt gebruikt om bestanden te archiveren met verschillende methoden, waaronder verschillende compressietechnieken. Er zijn verschillende applicatiesoftware beschikbaar voor Windows, Linux en MacOS voor het extraheren van RAR-bestanden. WinRAR-software, van RARLab, is het shareware-hulpprogramma voor het archiveren van bestanden (40 dagen gratis) voor het Microsoft Windows-platform; de software werd geport naar Linux (alleen als extractor) door dezelfde auteur, Eugene Roshal.

## Versiegeschiedenis van RAR-bestandsindeling

* v1.3 (origineel, heeft geen "Rar!" handtekening)
* v1.5
* v2.0 - uitgebracht met WinRAR 2.0 en Rar voor MS-DOS 2.0
* v2.9 - uitgebracht in WinRAR versie 3.00
* v5.0 - ondersteund door WinRAR 5.0 en hoger

## Belangrijkste kenmerken van het RAR-formaat

RAR is al heel lang in het veld en is een van de favoriete bestandsindelingen voor archivering. De belangrijkste kenmerken van het RAR-formaat zijn:

**`Hoge compressieverhouding:`** Superieur vergeleken met [ZIP](/nl/compression/zip/), vergelijkbaar met 7z- en zipx-formaat.

**'Sterke bestandscodering door ontwerp:'** Versleutelde RAR4-archieven vertrouwen op AES-128-gebaseerde codering, terwijl versleutelde RAR5-archieven vertrouwen op AES-256-codering met verbeterde sleutelplanning

**`Geavanceerde mogelijkheden voor foutcorrectie en gegevensherstel:`** optionele herstelrecords tijdens het maken van archieven

**`Bestandsgrootte:`** Minimum 20 bytes en maximum 2^63 bytes (8 exabytes van de totale grootte van het archief)

**`Multi-volume RAR-archieven:`** Mogelijkheid om grote archieven op te splitsen in verschillende kleinere bestanden om overdracht via het netwerk te vergemakkelijken. In dat geval worden de bestandsextensies met 1 verhoogd om gesplitste volumes weer te geven

## RAR-bestandsindeling

Volledige specificaties van het RAR-formaat zijn niet publiekelijk beschikbaar en daarom kunnen details over het formaat niet op een beknopte manier worden geformuleerd.

### Algemene archiefindeling

De algemene lay-out van een RAR-bestandsindeling die in versie 5.0 is geïntroduceerd, is als volgt:

|Bestandsindeling
---|
|Zelfuitpakkende module (optioneel)
|RAR 5.0-handtekening
|Archief versleutelingskop (optioneel)
| Hoofdarchiefkoptekst
|Archief commentaar service header (optioneel)
Bestandskop 1
|Service Headers (NTFS ACL, streams, etc.) voor vorig bestand (optioneel)
|...
|Bestandskop nr
|Service Headers (NTFS ACL, streams, etc.) voor vorig bestand (optioneel)
|Herstelrecord (optioneel)
|Einde van archiefkop

Informatie over elk hierboven vermeld gedeelte van het RAR-bestand is te vinden in het document [RAR 5.0-bestandsindelingsspecificaties](https://www.rarlab.com/technote.htm#arcstruct).

#### Zelfuitpakkende RAR-archieven

Als het RAR-bestand zelf uitpakkend is, staat de zelfuitpakkende informatie aan het begin van het bestand voorafgaand aan de archiefhandtekening. De grootte en inhoud zijn niet gedefinieerd.

#### RAR 5.0-handtekening

De RAR-handtekening is een header van 8 bytes die bestaat uit het volgende magische getal:

0x 52 61 72 21 1A 07 00

waar

0x6152 - HEAD_CRC

0x72 - HEAD_TYPE

0x1A21 - HEAD_FLAGS

0x0007 - HEAD_SIZE

## Referenties

* [RAR 5.0-archiefindeling](https://www.rarlab.com/technote.htm)
* [RAR - Door Wikipedia](https://en.wikipedia.org/wiki/RAR_(file_format))

