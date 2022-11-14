{
  "date" : "2019-10-11",
  "keywords" :[ "tar-bestand", "tar-bestandsindeling", "wat is een tar-bestand", "bestand", "tar-voorbeeld", "tar-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TAR - Unix-archiefbestandsindeling",
  "description":"Meer informatie over wat een Tar-bestand is en API's die TAR-bestanden kunnen maken en openen.",
  "linktitle" : "TAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een TAR-bestand?

Bestanden met de extensie .tar zijn archieven die zijn gemaakt met een op Unix gebaseerd hulpprogramma voor het verzamelen van een of meer bestanden. Meerdere bestanden worden opgeslagen in een niet-gecomprimeerde indeling met de ondersteuning van het toevoegen van bestanden en mappen aan het archief. Het TAR-hulpprogramma op Unix is gebaseerd op commando's, maar de bestanden die op deze manier worden gemaakt, worden ondersteund door de meeste bestandsarchiveringssystemen op bijna alle besturingssystemen. Het werd voor het eerst gemaakt in 1979 door de AT&T Bell Laboratories en latere versies werden in de loop van de tijd gepubliceerd.

## TAR-bestandsindeling

TAR is een open bestandsformaat met volledige specificaties die beschikbaar zijn voor referentie van de ontwikkelaar. De bestandsstructuur werd gestandaardiseerd in POSIX.1-1988 en later in POSIX.1-2001. De datasets die door tar zijn gemaakt, bevatten informatie over bestandssysteemparameters, zoals:

* Naam
* Tijdstempels
* Eigendom
* Bestandstoegangsmachtigingen
* Directory-organisatie

Een Tar-bestand heeft geen magisch getal. Het bevat een reeks blokken waarbij elk blok BLOCKSIZE-bytes is.

Elk gearchiveerd bestand wordt weergegeven door een kopblok dat het bestand beschrijft, gevolgd door nul of meer blokken die de inhoud van het bestand weergeven. Aan het einde van het archiefbestand bevinden zich twee blokken van 512 bytes gevuld met binaire nullen als einde-bestandsmarkering. Een redelijk systeem zou zo'n einde-bestandsmarkering aan het einde van een archief moeten schrijven, maar mag er niet vanuit gaan dat zo'n blokkering bestaat bij het lezen van een archief. In het bijzonder geeft GNU tar altijd een waarschuwing als het deze niet tegenkomt.

De blokken kunnen worden geblokkeerd voor fysieke I/O-bewerkingen. Elk record van n blokken (waarbij n is ingesteld door de blocking-factor = 512-size optie tot tar) wordt geschreven met een enkele "write()"-bewerking. Op magneetbanden is het resultaat van zo'n schrijven een enkele plaat. Bij het schrijven van een archief moet het laatste record van blokken op volledige grootte worden geschreven, met blokken na het nulblok met allemaal nullen. Bij het lezen van een archief moet een redelijk systeem correct omgaan met een archief waarvan het laatste record korter is dan de rest, of dat afvalrecords bevat na een nulblokkering.

### Teerkoptekst

Net als alle andere bestandsheaders, bevat het tar-bestandsheaderrecord metagegevens over een bestand en wordt weergegeven in de volgende tabel.


|Veldverschuiving|Veldgrootte (bytes)|Veld
---|---|---|
|0|100|Bestandsnaam
|100|8|Bestandsmodus
|108|8|Numerieke gebruikers-ID van de eigenaar
|116|8|Numerieke gebruikers-ID van de groep
|124|12|Bestandsgrootte in bytes (octale grondtal)
|136|12|Laatste wijzigingstijd in numeriek Unix-tijdformaat (octaal)
|148|8|Checksum voor koprecord
|156|1|Link-indicator (bestandstype)
|157|100|Naam van gekoppeld bestand

Ongebruikte velden worden gevuld met NUL-bytes. Een header bestaat uit 257 bytes die is opgevuld met NUL-bytes om het te vullen tot een record van 512 bytes.

## Referenties ##

* [TAR - Door Wikipedia](https://en.wikipedia.org/wiki/Tar_(computing))
* [TAR basisformaat](https://www.gnu.org/software/tar/manual/html_node/Standard.html)

