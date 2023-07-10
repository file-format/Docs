{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OST - Outlook-opslagbestandsindeling",
  "description":"Meer informatie over OST-bestandsindelingen en API's die OST-bestanden kunnen maken en openen.",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een OST-bestand?

OST- of offline opslagbestanden vertegenwoordigen de mailboxgegevens van de gebruiker in de offlinemodus op de lokale computer na registratie bij Exchange Server met Microsoft Outlook. Het wordt automatisch aangemaakt bij het eerste gebruik van Microsoft Outlook bij verbinding met de server. Nadat het bestand is gemaakt, worden de gegevens gesynchroniseerd met de e-mailserver, zodat deze ook offline beschikbaar is in geval van ontkoppeling van de e-mailserver. OST-bestanden kunnen mailbox-items zoals e-mails, contacten, agenda-informatie, notities, taken en andere soortgelijke gegevens gebruiken. Gebruikers kunnen e-mails en andere gegevensitems in het OST-bestand maken, zelfs als er geen verbinding met de server is, maar deze worden niet gesynchroniseerd met de server. Zodra de verbinding tot stand is gebracht, wordt het lokale bestand opnieuw gesynchroniseerd met de server, zodat zowel de server als de lokale kopie op hetzelfde informatieniveau staan.

## OST-bestandsindeling

De bestandsindelingen OST (Offline Storage Table) en [PST](/nl/email/pst/) (Personal Storage Table) bestaan uit de indeling Personal Folder File (PFF) die overeenkomt met het opslaan van e-mails, contacten en afspraken van gebruikers. Gegevens in een PFF-bestand worden opgeslagen in little-endian waarbij alle datums en tijden worden weergegeven als FILETIME in UTC. [MS-PST] definieert twee soorten PFF:

* 32-bits ANSI-indeling
* 64-bits Unicode-indeling

PST-bestandsformaat [specificaties](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546), zoals beschikbaar bij Microsoft, zijn ook van toepassing op het OST-bestandsformaat als gratis en onherroepelijke patentlicenties via de Open Specification Promise. Het bestaat uit de volgende te onderscheiden elementen:

* Fles kop
* Bestandskopgegevens
* Indextakknooppunt
* Indexbladknooppunt
* (Bestand) offset-index
* (Artikel) descriptor index
* Lokale beschrijvingen
* Type artikeltabel

### Koptekstinformatie

De HEADER-structuur van het OST-bestand bevindt zich helemaal aan het begin van het bestand op 0 offset. Het bevat metadata-informatie over het OST-bestand en de ROOT-informatie om toegang te krijgen tot de hierboven beschreven NDB Layer-gegevensstructuren. De HEADER-structuur verschilt voor de Unicode- en ANSI-versies van het OST-bestandsformaat.

De header begint met een toverwoord van 4 bytes **!BDN** vertegenwoordigd door bytes (0x21, 0x42, 0x44, 0x4E). Een ander magisch getal van 2 bytes, **SM** (0x53, 0x4D), bevindt zich op offset 8 vanaf het begin van het bestand. Versie-informatie (ANSI of Unicode) ligt op een offset van 10 vanaf het begin van het bestand. Hex-waarde (0x17) geeft het Unicode OST-bestand aan, terwijl 0x0E of 0x0F het ANSI-bestandsformaat vertegenwoordigt.

|Veld|Beschrijving
---|---|
|dwMagic (4 bytes)|MOET "{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")" zijn
|dwCRCPartial (4 bytes)|De 32-bits CRC-waarde van de 471 bytes aan gegevens vanaf wMagicClient (0ffset 0x0008)
|wMagicClient (2 bytes)|MOET "{ 0x53, 0x4D }" zijn.
|wVer (2 bytes)|Bestandsformaatversie. Deze waarde MOET 14 of 15 zijn als het bestand een ANSI PST-bestand is, en MOET 23 zijn als het bestand een Unicode PST-bestand is.
|wVerClient (2 bytes)|Versie van clientbestandsformaat. De versie die overeenkomt met het formaat dat in dit document wordt beschreven, is 19. Makers van een nieuw PST-bestand op basis van dit document MOETEN deze waarde initialiseren op 19.
|bPlatformCreate (1 byte)|Deze waarde MOET worden ingesteld op 0x01.
|bPlatformAccess (1 byte)|Deze waarde MOET worden ingesteld op 0x01.
|dwGereserveerd (8 bytes)|
|bidUnused (alleen 8 bytes Unicode)|Ongebruikte opvulling toegevoegd toen het Unicode PST-bestandsformaat werd gemaakt.
|bidNextP (Unicode: 8 bytes; ANSI: 4 bytes)|Volgende pagina BID. Pagina's hebben een speciale teller voor het toewijzen van bidIndex-waarden. De waarde van bidIndex voor BID's voor pagina's wordt toegewezen vanuit deze teller.
|bidNextB (alleen 4 bytes ANSI): |Next BID. Deze waarde is de monotone teller die de BID aangeeft die moet worden toegewezen voor het volgende toegewezen blok. BID-waarden lopen op in stappen van 4. Voor meer details, zie paragraaf 2.2.2.2.
|dwUnique (4 bytes)|Dit is een monotoon toenemende waarde die elke keer dat de HEADER-structuur van het PST-bestand wordt gewijzigd, wordt gewijzigd. De functie van deze waarde is om een unieke waarde te bieden en om ervoor te zorgen dat de HEADER CRC's na elke kopwijziging anders zijn.
|rgnid[](128 bytes)|Een vaste array van 32 NID's, die elk overeenkomen met een van de 32 mogelijke NID_TYPE's (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_TYPE_ASSOC_MESSAGE)
|qwOngebruikt (8 bytes)|Ongebruikte ruimte; MOET op nul staan. Alleen Unicode PST-bestandsindeling.
|root (Unicode: 72 bytes; ANSI: 40 bytes)|Een ROOT-structuur (paragraaf 2.2.2.5).
|dwAlign (4 bytes)|Ongebruikte uitlijnbytes; MOET op nul staan. Alleen Unicode PST-bestandsindeling.
|rgbFM (128 bytes)|Verouderde FMap. Deze wordt niet meer gebruikt en MOET gevuld worden met 0xFF. Lezers MOETEN de waarde van deze bytes negeren.
|rgbFP (128 bytes)|Verouderde FPMap. Deze wordt niet meer gebruikt en MOET gevuld worden met 0xFF. Lezers MOETEN de waarde van deze bytes negeren.
|bSentinel (1 byte)|MOET ingesteld zijn op 0x80.
|bCryptMethod (1 byte)|Geeft aan hoe de gegevens in het PST-bestand zijn gecodeerd. MOET worden ingesteld op een van de vooraf gedefinieerde waarden (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbGereserveerd (2 bytes)| Gereserveerd; MOET op nul staan.
|bidNextB (8 bytes)|Geeft de volgende beschikbare BID-waarde aan. Alleen Unicode PST-bestandsindeling.
|bidNextB (ALLEEN Unicode: 8 bytes)|Volgend BID. Deze waarde is de monotone teller die de BID aangeeft die moet worden toegewezen voor het volgende toegewezen blok. BID-waarden lopen op in stappen van 4. Voor meer details, zie paragraaf 2.2.2.2.
|dwCRCFull (4 bytes)|De 32-bits CRC-waarde van de 516 bytes aan gegevens vanaf wMagicClient tot en met bidNextB. Alleen Unicode PST-bestandsindeling.
|ullGereserveerd (8 bytes)|Gereserveerd; MOET op nul staan. Alleen ANSI PST-bestandsindeling.
|dwGereserveerd (4 bytes)|Gereserveerd; MOET op nul staan. Alleen ANSI PST-bestandsindeling.
|rgbReserved2 (3 bytes)|
|bGereserveerd (1 byte) |
|rgbReserved3 (32 bytes) |

## Referenties

* [Bestandsindeling Outlook Personal Folders (.ost)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [specificaties bestandsindeling persoonlijke map](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

