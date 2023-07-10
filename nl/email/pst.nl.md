{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST - Outlook Personal Information Store-bestandsindeling",
  "description":"Meer informatie over PST-bestandsindeling en API's die PST-bestanden kunnen maken en openen.",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een PST-bestand?

Bestanden met de extensie .pst vertegenwoordigen Outlook Personal Storage Files (ook wel Personal Storage Table genoemd) waarin verschillende gebruikersinformatie is opgeslagen. Gebruikersinformatie wordt opgeslagen in verschillende soorten mappen, waaronder e-mails, agenda-items, notities, contacten en verschillende andere bestandsindelingen. PST-bestanden worden gebruikt voor het offline archiveren van e-mailgegevens die later in verschillende toepassingen kunnen worden geladen en bekeken.

## Specificaties PST-bestandsindeling

PST-bestandsindeling [specificaties](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546) zijn verkrijgbaar bij Microsoft als gratis en onherroepelijke gratis patentlicentie via de Open Specification Promise .

### Type PST-formaten

PST-bestandsindelingen zijn onderverdeeld in twee typen op basis van de codering van het bestandstype. ANSI-gecodeerde PST-bestanden zijn oudere bestandsindelingen en worden alleen ondersteund door Outlook 2002 en eerdere versies. Dergelijke bestanden hebben een maximale grootte van 2 GB (2^^31^^ Bytes) en bieden geen ondersteuning voor Unicode. Een moderner type bestandsindeling, gebaseerd op Unicode-codering, verwijdert de beperking van de bestandsgrootte en kan een maximale gegevensgrootte van 50 GB bereiken.

### Logische organisatie van PST-bestandsindeling

Aan de basis van het PST-bestandsformaat ligt B-Tree dat gegevens gesorteerd houdt en zoekopdrachten, opeenvolgende toegang, invoegingen, verwijderingen enz. in logaritmische tijd mogelijk maakt. De algemene structuur van een PST-bestand is georganiseerd in drie lagen.

![Logical layers of a PST file](/nl/email/PST-1.png "Logical layers of a PST file")

`Node Database (NDB) Layer` - De knooppuntdatabaselaag bevindt zich op het lagere niveau van een PST-bestand en bevat een database met knooppunten. Deze knooppunten vertegenwoordigen in feite opslagfaciliteiten op een lager niveau van het PST-bestandsformaat. NDB-laag bestaat uit header, bestandstoewijzingsinformatie, blokken en BTrees (Node BTree en Block BTree) vanuit het oogpunt van opslag. Knooppunten en blokken van de NDB-laag zijn gekoppeld via Data BID, wat een van de vier eigenschappen van Node-referentie is, namelijk NID (Node ID), Parent NID, Data BID (Block BID) en SubNode BID.

`Lijsten, tabellen en eigenschappenlaag -` De LTP-laag biedt het logische begrip van concepten op een hoger niveau bovenop NDB. Naast andere elementen bestaat de LTP-laag voornamelijk uit Property Context (PC) en Table Context (TC). PC is een verzameling eigenschappen, terwijl TC een tweedimensionale matrix vertegenwoordigt van verzameling eigenschappen versus de aanwezigheid hiervan. Efficiënte implementatie van pc's en TC's, de LTP-laag gebruikt de volgende twee soorten datastructuren bovenop NDB Node:

* Heap On Node (HN) - maakt het mogelijk om de gegevensstroom van een knooppunt in kleine fragmenten van variabele grootte toe te wijzen.
* BTree on Heap (BTH) - BTH biedt een gemakkelijke en praktische manier om door data te zoeken. PC's, hierboven beschreven, zijn geïmplementeerd als BTH's en daarom wordt het geïmplementeerd door in een HN-structuur te bouwen.

`Messaging Layer -` Regels op een hoger niveau en bedrijfslogica voor het werken met PST-bestanden zijn op deze laag geïmplementeerd. De logische uitvoer van deze laag resulteert als mapobjecten, berichtobjecten, bijlageobjecten en eigenschappen, wat mogelijk wordt gemaakt door LTP- en NDB-lagen te combineren. Regels en vereisten die moeten worden gevolgd bij het wijzigen van de PST-inhoud, worden ook op deze laag gedefinieerd.

### Fysieke organisatie van PST-bestandsindeling

Het hoge niveau van bestandsorganisatie van het PST-bestand is zoals weergegeven in de onderstaande afbeelding. Dit is slechts een overzicht van verschillende concepten van logische elementen van het PST-bestand.

![Physical organization of the PST file format](/nl/email/PST-2.png "Physical organization of the PST file format")


#### PST Header-informatie

De HEADER-structuur van het PST-bestand bevindt zich helemaal aan het begin van het bestand op 0 offset. Het bevat metadata-informatie over het PST-bestand en de ROOT-informatie om toegang te krijgen tot de hierboven beschreven NDB Layer-gegevensstructuren. De HEADER-structuur verschilt voor de Unicode- en ANSI-versies van het PST-bestandsformaat.

De header begint met een toverwoord van 4 bytes **!BDN** vertegenwoordigd door bytes (0x21, 0x42, 0x44, 0x4E). Een ander magisch getal van 2 bytes, **SM** (0x53, 0x4D), bevindt zich op offset 8 vanaf het begin van het bestand. Versie-informatie (ANSI of Unicode) ligt op een offset van 10 vanaf het begin van het bestand. Hex-waarde (0x17) geeft het Unicode PST-bestand aan, terwijl 0x0E of 0x0F het ANSI-bestandsformaat vertegenwoordigt.

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

### Gegevensbescherming ###

Om veiligheidsredenen kunnen PST-bestanden ook met een wachtwoord worden beveiligd, waardoor de laadtoepassing een wachtwoord moet toepassen voordat het kan worden bekeken. Wachtwoord toegepast op het PST-bestand wordt opgeslagen in het berichtenarchief. Dit biedt echter geen sterke gegevensbescherming, aangezien het wachtwoord kan worden verwijderd door beschikbare tools. Het door de gebruiker opgegeven wachtwoord wordt ook niet gebruikt als onderdeel van de sleutel voor het coderen en decoderen van coderingsalgoritmen. Het heeft dus geen zin om gegevens te beschermen waartoe onbevoegde partijen toegang hebben. Opslag van wachtwoord als CRC-32-hash van de originele string maakt het ook een zwakke methode voor gegevensbeveiliging tegen brute-force-aanpak.

## Referenties ##

* [Bestandsindeling Outlook Personal Folders (.pst)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [specificaties bestandsindeling persoonlijke map](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

