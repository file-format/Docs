{
  "date" : "2019-12-10",
  "keywords" :[ "XLSB", "bestand", "extensie", "bestandsindeling", "Excel binair spreadsheetbestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Uw gids voor bestandsindelingen om te weten wat een XLSB-bestand is en API's die ze kunnen maken en openen.",
  "title" :"Wat is een XLSB-bestand?",
  "linktitle" : "XLSB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Wat is een XLSB-bestand?

XLSB-bestandsindeling specificeert de Excel Binary File Format, een verzameling records en structuren die de inhoud van de Excel-werkmap specificeren. De inhoud kan ongestructureerde of semi-gestructureerde tabellen met getallen, tekst of zowel getallen als tekst, formules, externe gegevensverbindingen, grafieken en afbeeldingen bevatten. In tegenstelling tot [XLSX](/nl/spreadsheet/xlsx/) (dat is gebaseerd op het Open XML-bestandsformaat), vertegenwoordigt de XLSB een binair Excel-werkmapbestand. XLSB-bestanden kunnen sneller worden gelezen en geschreven, waardoor ze handig zijn voor het werken met grote bestanden. XLSB wordt zelden gebruikt om werkmappen op te slaan, aangezien XLSX (en voorheen [XLS](/nl/spreadsheet/xls/)) de meest gebruikte door de gebruiker geselecteerde bestandsindelingen zijn voor het opslaan van werkmappen. Het kan worden geopend door Microsoft Office 2007 en hoger.

## Specificaties XLSB-bestandsindeling ##

De bestandsformaatspecificaties voor het XLSB-bestandsformaat werden in 2008 openbaar gemaakt als versie 1.0. Sindsdien zijn de specificaties verschillende keren herzien en is de nieuwste versie van specificaties (v 10.0) gepubliceerd in april 2018. De specificaties zijn openbaar beschikbaar door Microsoft als [[MS-XLSB] - Excel Binary File Format-specificaties](https:/ /msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx) en moet door iedereen worden geraadpleegd voor het lezen of schrijven van bestanden in XLSB-bestandsindeling.

## XLSB-bestandsstructuur ##

Een XLSB-bestand is een pakket dat bestaat uit een verzameling onderdelen. Deze onderdelen bevatten informatie over de inhoud van een werkmap, inclusief werkmapgegevens en de structuur van het pakket. Sommige delen bevatten informatie die is opgeslagen met behulp van binaire records, sommige als XML, terwijl andere informatie bevatten die is opgeslagen als een binaire stroom van bytes. Elke binaire record bevat nul of meer gestructureerde velden die de werkmapgegevens bevatten.

#### Pakket ####

Een XLSB-pakket is een [ZIP](/nl/compression/zip/)-archief dat precies één werkmapgedeelte moet bevatten. Dit deel moet het doel zijn van een relatie in dit pakketrelatiedeel. Het werkmapgedeelte is het startgedeelte in het XLSB-document.

#### Een deel ####

Een onderdeel is een stroom van bytes met een bijbehorend inhoudstype dat de aard en het type inhoud specificeert dat in het onderdeel is opgeslagen. Sommige delen slaan informatie op in binair formaat, terwijl andere informatie opslaan als XML. De sectie [onderdelenopsomming](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) van het specificatiedocument vermeldt de geldige onderdelen, inhoudstypen en vereiste/optionele relaties tussen alle onderdelen in een pakket.

#### Relatie ####

Een bron en een doelbron zijn verbonden door een relatie. Een relatie kan zijn:

**Pakketrelatie:** waarbij het doel een onderdeel is en de bron het pakket als geheel

**Part-to-part relatie:** waarbij het doel een onderdeel is en de bron een onderdeel van het pakket

**Expliciete relatie:** waarbij naar een resource wordt verwezen vanuit de inhoud van een brongedeelte door te verwijzen naar de ID-kenmerkwaarde van een relatie-element

**impliciete relatie** is een relatie die niet expliciet is

**Interne relatie:** waarbij het doelwit een onderdeel is van het pakket

**Externe relatie:** waarbij het doel een externe bron is die niet in het pakket zit

#### Dossier ####

Een record is de basisbouwsteen die wordt gebruikt om informatie over functies in een werkmap op te slaan. Elk binair record is een reeks bytes met een variabele lengte. Een binair record bestaat uit drie componenten:

* een recordtype
* een recordgrootte, en
* de recordgegevens die specifiek zijn voor dat recordtype.

**Recordtype:** Het recordtype toont het type record dat door het record is opgegeven. Het specificeert ook de structuur van recordgegevens die specifiek zijn voor dit record. De geldige recordtypen worden vermeld in de sectie [Recordenumeratie](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx) van het specificatiedocument. Het recordtype moet één of twee bytes zijn en moet groter zijn dan of gelijk zijn aan 128 en kleiner dan 16384.

**Recordgrootte:** De recordgrootte specificeert het aantal bytes dat de totale grootte van de recordgegevens aangeeft. Deze waarde MOET één tot vier bytes zijn. Deze waarde MOET één byte zijn als de hoge bit in de lage byte gelijk is aan 0; anders MOET deze waarde groter zijn dan één byte. Als het aantal bytes groter is dan één byte, geeft het hoge bit in elke volgende byte aan of een extra byte wordt gebruikt. Als de hoge bit van de tweede byte gelijk is aan 1, dan MOET deze waarde een extra derde byte gebruiken. Als de hoge bit van de derde byte gelijk is aan 1, dan MOET deze waarde een extra vierde byte gebruiken. De hoge bit van de vierde byte MOET worden genegeerd. De waarde bestaat uit de zeven lage bits van elke byte gecombineerd. De lage, minst significante bits bevinden zich in de eerste byte en elke volgende byte bevat bits van hogere orde dan de vorige byte.

**Recordgegevens:** De recordgegevenscomponent bevat velden die overeenkomen met een bepaald recordtype en vormen de rest van het record. De volgorde en structuur van de velden voor een bepaald recordtype dat wordt vermeld in Recordtelling, wordt gespecificeerd in de overeenkomstige sectie voor dat recordtype in Records. De totale omvang van de recorddatacomponent MOET gelijk zijn aan de recordgrootte. Velden in de recordgegevenscomponent kunnen eenvoudige waarden, arrays van waarden, structuren van verschillende velden, arrays van velden en arrays van structuren bevatten.

#### XLSB-opnamevoorbeeld ####

Het volgende recordtype en recordgrootte specificeren een **BrtCommentText**-record met een grootte van 200 bytes:

11111101 00000100 11001000 00000001 [Recordvelden]

De eerste byte is 11111101, wat een lage waarde van 125 aangeeft en dat het recordtype een tweede byte vereist. De tweede byte is 00000100, waarmee een hoge waarde van 4 * 128 wordt opgegeven, wat gelijk is aan 512. De waarde van het recordtype is 125 + 512 of 637, wat overeenkomt met een recordtype **BrtCommentText**. De volgende byte is 11001000, wat een lage waarde van 72 aangeeft en dat de recordgrootte een tweede byte vereist. De tweede byte is 00000001, wat een hogere waarde van 1 * 128 aangeeft en dat de recordgrootte geen extra byte vereist. De recordgrootte is 72 + 128 of 200, wat de totale grootte aangeeft, in bytes, van de recordgegevenscomponent. De velden in de recordgegevenscomponent worden gespecificeerd door **BrtCommentText**.

## Referenties ##

* [[MS-XLSB] - Excel (.xlsb) binaire bestandsindeling](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)

