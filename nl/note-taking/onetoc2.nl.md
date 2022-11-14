{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONETOC2 - Microsoft OneNote-bestandsindeling",
  "description":"Meer informatie over de ONETOC2-bestandsindeling en API's die ONETOC2-bestanden kunnen maken en openen.",
  "linktitle" : "ONETOC2",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is ONETOC2? ##

Degenen die met de toepassing [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) hebben gewerkt, hebben misschien de aanwezigheid van .onetoc2-bestanden in de notebookmap opgemerkt. Microsoft OneNote maakt een binair .onetoc2-bestand als inhoudsopgave voor het bijhouden van een index over de volgorde van verschillende notitiesecties in een notitieblok. Een notebook is een verzameling sectiebestanden die in dezelfde map zijn opgeslagen. Het .onetoc2-bestand gebruikt een verzameling eigenschappen om instellingen op te geven, zoals de volgorde van secties in het notitieblok en de kleur van het notitieblok.

Wanneer u een notitieblok maakt in OneNote 2016, wordt dit automatisch opgeslagen in de nieuwe bestandsindeling van 2010-2016. U hebt deze indeling nodig als u wilt dat alle functies in OneNote 2016, zoals wiskundige vergelijkingen en gekoppelde notities, correct werken.

## ONETOC2-bestandsindeling ##

De .onetoc2-bestandsindeling wordt weergegeven als OneNote Revision Store File Format en is een verzameling structuren die een revisiearchief specificeren dat is georganiseerd in objectruimten met kruisverwijzingen, objecten met eigenschappensets bevat en een transactielogboek bevat om de bestandsintegriteit over asynchrone schrijft. Volledige specificaties voor het .onetoc2-bestandsformaat zijn [online](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) beschikbaar en er kan naar worden verwezen voor de ontwikkeling van applicaties .

### Bestandsstructuur ###

Een revisiearchiefbestand MOET beginnen met een **Header**-structuur. De rest van het bestand is opgedeeld in blokken van bytes, waarbij de grootte en structuur van elk blok wordt gespecificeerd door het veld dat ernaar verwijst. Een blok is bereikbaar als ernaar wordt verwezen door de **Header**-structuur, of als ernaar wordt verwezen door een veld in een ander bereikbaar blok. Gegevens buiten de **Header**-structuur en alle bereikbare blokken MOETEN worden genegeerd.

Alle structuren zijn uitgelijnd op 1-byte grenzen. Alle gehele getallen zijn ondertekend, tenzij anders aangegeven. Alle velden zijn [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7), tenzij anders aangegeven.

#### Koptekst ####

De header van het .ONE-bestand bestaat uit stukjes die verschillende unieke id's en velden bevatten voor de weergave van bestandsinformatie als volgt:

`guidFileType (16 bytes):` Een GUID die het type van het revisieopslagbestand specificeert. MOET een van de waarden uit de volgende tabel zijn.

|Bestandsindeling|Waarde
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 bytes):` Een GUID die de identiteit van dit revisie-archiefbestand specificeert. MOET wereldwijd uniek zijn.

`guidLegacyFileVersion (16 bytes):` MOET "{00000000-0000-0000-0000-000000000000}" zijn en MOET worden genegeerd.

`guidFileFormat (16 bytes):` Een GUID die aangeeft dat het bestand een revisie-archiefbestand is. MOET "{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}" zijn.

`ffvLastCodeThatWroteToThisFile (4 bytes):` Een geheel getal zonder teken. MOET een van de waarden in de volgende tabel zijn, afhankelijk van het bestandstype.

|Bestandsindeling|Waarde
--- | --- |
|.een|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 bytes):` Een niet-ondertekend geheel getal. MOET een van de waarden in de volgende tabel zijn, afhankelijk van de bestandsindeling van dit bestand.


|Bestandsindeling|Waarde
--- | --- |
|.een|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 bytes):` Een niet-ondertekend geheel getal. MOET een van de waarden in de volgende tabel zijn, afhankelijk van de bestandsindeling van dit bestand.
:


|Bestandsindeling|Waarde
--- | --- |
|.een|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bytes):` Een geheel getal zonder teken. MOET een van de waarden in de volgende tabel zijn, afhankelijk van de bestandsindeling van dit bestand.


|Bestandsindeling|Waarde
--- | --- |
|.een|0x0000002A
|.onetoc2|0x0000001B

## Referenties ##

* [[MS-ONESTORE] - OneNote-bestandsindeling](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

