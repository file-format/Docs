{
  "date" : "2021-08-09",
  "keywords" :[ "cso-bestand", "cso-bestandsindeling", "wat is een cso-bestand", "bestand", "cso-voorbeeld", "cso-bestandsextensie", "extensie", "formaat", "iso", "DAX-compressie "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Meer informatie over CSO-bestandsindeling en API's die CSO-bestanden kunnen maken en openen.",
  "title" :"CSO - Gecomprimeerde ISO-schijfkopie",
  "linktitle" : "CSO",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-09"
}

## Wat is een CSO-bestand?

Een bestand met de extensie .cso is een gecomprimeerd ISO-imagebestand. De CSO is een alternatief voor de DAX-compressiemethode; ook bekend als CISO; was de eerste methode om de [ISO](/nl/compression/iso/)-bestanden te comprimeren en is meestal een voorkeursmethode voor het archiveren van PlayStation Portable-dingen. Deze indeling maakt gebruik van Deflate-compressie, die maximaal negen compressielagen kan bevatten. Software zoals Prometheus en YACC worden gebruikt om de afbeeldingen te maken.

## CSO-bestandsindeling

Het CSO-bestandsformaat was de eerste compressiemethode voor ISO om meer geheugenruimte te besparen. De verbeteringen werden van tijd tot tijd aangebracht voor een betere compressie. De CSO gebruikt Deflate-compressie met negen niveaus van voorinstellingen, meestal kan elk niveau 2 KiB-blokken afzonderlijk verwerken. Hoewel de hoogste niveaus van compressie de laadtijden kunnen vertragen en lange laadtijden in software die sterk afhankelijk is van schijfstreaming, kunnen ook de lagere niveaus aanzienlijke compressie uitvoeren.

### CSO-bestandsstructuur

Het CSO-bestandsformaat bevat een 24-byte header, datablokken en een indextabel. Little-endian wordt aangenomen voor velden groter dan een byte. De architectuur endianness van PlayStation Portable wordt hieronder gegeven.

#### Koptekst

| Offset (bytes) | Naam | Grootte (bytes) | Doel |
----------|----------|--------------|---------|
| 0x0 | Magie | 4 | Altijd CISO, of 0x4F534943 wanneer gelezen als een 32-bits geheel getal. Dit veld wordt gebruikt om een CSO-bestand te identificeren. Merk op dat dit veld anders kan zijn voor de andere afgeleiden van CSO, ZSO gebruikte bijvoorbeeld de magische code ZISO. |
| 0x4 | Kopgrootte | 4 | Voor de oorspronkelijke CSO "v1"-bestandsindeling wordt dit veld genegeerd en hoeft het daarom niet nauwkeurig te zijn. De "v2"- en ZSO-indeling vereisen echter dat dit veld altijd 0x18 (24 bytes) is. |
| 0x8 | Niet-gecomprimeerde grootte | 8 | De grootte van de originele ongecomprimeerde ISO in bytes. |
| 0x10 | Blokgrootte | 4 | De grootte van elk gegevensblok in bytes vóór compressie. Gewoonlijk 2048 bytes, hetzelfde als de grootte van elke ISO 9660-sector. |
| 0x14 | Versie | 1 | De versie van de bestandsindeling die wordt gebruikt. Voor het "v1"-formaat kan de waarde 0 of 1 zijn. Voor het "v2"-formaat moet dit 2 zijn. Bovendien vereist het ZSO-formaat dat dit 1 is. |
| 0x15 | Indexuitlijning | 1 | De uitlijning van elk indexitem, gespecificeerd in bits. |
| 0x16 | Gereserveerd | 2 | Dit veld is ongebruikt. In de "v1"-indeling wordt dit veld genegeerd en kan het willekeurige waarden bevatten. In de "v2"-indeling moet dit veld nul zijn. |

#### Indextabel

De indextabel bevat verschillende 4-byte-items, die de positie van elk gegevensblok aangeven, en een extra, laatste item dat naar het einde van het bestand wijst.
De inhoud van elk item is als volgt:
| Beetje | Lengte | Masker | Naam | Doel |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFFFF | Positie | Dit veld geeft, wanneer het naar links wordt verschoven door de indexuitlijning in de kop, de positie weer waar het gegevensblok begint. |
| 31 | 1 | 0x80000000 | Compressietype | Het ZSO-formaat heeft vergelijkbare semantiek, alleen dat 0 LZ4 vertegenwoordigt in plaats van Deflate. In het "v2"-formaat. Het blok wordt impliciet als niet-gecomprimeerd beschouwd als de blokgrootte gelijk is aan of groter is dan de blokgrootte die is opgegeven in de bestandskop. |

#### Gegevensblokken

De datablokken bestaan uit de ongecomprimeerde of gecomprimeerde data. De grootte van een blok wordt berekend door zijn positie te krijgen en deze vervolgens af te trekken van de positie van het volgende blok. Als de indexuitlijning groter is dan nul, is het waarschijnlijk dat de blokgrootte groter is dan de gegevens die erin staan.


## Referenties

* [CSO - door Wikipedia](https://en.wikipedia.org/wiki/.CSO)


