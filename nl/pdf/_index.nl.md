{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" :[ "grondbeginselen" ],
  "description":"Portable Document Format (PDF) is een standaardweergave van documenten onafhankelijk van software, hardware en besturingssysteem. PDF-standaarden omvatten PDF/A, PDF/E, PDF/UA, PDF/VT en PDF/X.",
  "title" :"PDF-bestandsindeling - Wat is een PDF-bestand?",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
      "weight" : "01"
}
},
  "lastmod" : "2019-09-10"
}

Portable Document Format (PDF) is een type document dat in de jaren negentig door Adobe is gemaakt. Het doel van dit bestandsformaat was om een standaard te introduceren voor de weergave van documenten en ander referentiemateriaal in een formaat dat onafhankelijk is van applicatiesoftware, hardware en besturingssysteem. Het PDF-bestandsformaat heeft volledige mogelijkheden om informatie zoals tekst, afbeeldingen, hyperlinks, formuliervelden, rich media, digitale handtekeningen, bijlagen, metadata, geospatiale functies en 3D-objecten erin te bevatten die als onderdeel van het brondocument kunnen worden gebruikt.

In de meeste gevallen worden bestaande documenten geconverteerd naar PDF in plaats van een geheel nieuwe PDF te maken. Maar dat betekent niet dat er geen software is voor het maken of manipuleren van PDF-bestanden.

**(Wilt u iets delen over de PDF-bestandsindeling? U kunt uw bevindingen posten in het gedeelte [PDF File Format News](https://news.fileformat.com/t/PDF).)**

## PDF-bestandsindeling - korte geschiedenis

Een snelle doorloop van de tijdlijn over de vorming van PDF-bestanden in termen van tijdlijn is als volgt:

**1993** - Adobe Systems stelt de PDF-specificaties gratis ter beschikking

**2008** - PDF is op 1 juli 2008 als open standaard uitgebracht en door de International Organization for Standardization gepubliceerd als **ISO 32000-1:2008**.

**2008** - Adobe heeft een openbare patentlicentie gepubliceerd voor royaltyvrije rechten in ISO 32000-1-indeling voor alle patenten die eigendom zijn van Adobe en die nodig zijn om PDF-compatibele implementaties te maken, gebruiken, verkopen en distribueren.

De eerste versie van PDF aangeduid als PDF 1.0 die later werd herzien tot PDF 1.7. PDF 1.7, dat de ISO 32000-1 werd, bevat een aantal niet-gestandaardiseerde eigen technologieën, evenals Adobe XML Forms Architecture (XFA) en JavaScript-extensie voor Acrobat. Het was op 28 juli 2017 toen PDF 2.0, bekend als ISO 32000-2:2017, werd gepubliceerd, waarin geen niet-gestandaardiseerde technologieën zijn opgenomen.

## Specificaties PDF-bestandsindeling

Een PDF-bestand is een set bytes die kan worden gegroepeerd in tokens volgens syntaxisregels die zijn gedefinieerd door PDF-specificaties. Een of meer tokens worden gecombineerd om syntactische entiteiten van een hoger niveau te vormen, voornamelijk objecten, die de basisgegevenswaarden zijn waaruit een PDF-document is opgebouwd.

### Bestandsstructuur van PDF-bestanden

De inhoud van het PDF-bestand is in de volgende volgorde in het bestand gerangschikt.

|Koptekst
|Lichaam
|Kruisverwijzingstabel
|Aanhangwagen

#### Koptekst PDF-bestand ####

Ongeacht de PDF-versie begint een PDF-bestand met een koptekst die een unieke identifier voor PDF bevat en de versie van het formaat zoals %PDF-1.x waarbij x varieert van 1-7.

#### Bestandstekst ####

De hoofdtekst van een PDF-bestand bestaat uit een reeks indirecte objecten die de inhoud van een document vertegenwoordigen. De objecten, zoals hierboven beschreven, vertegenwoordigen componenten van het document, zoals lettertypen, pagina's en voorbeeldafbeeldingen. Vanaf PDF 1.5 kan de body ook objectstromen bevatten, die elk een reeks indirecte objecten bevatten.

#### Kruisverwijzingstabel ####

De kruisverwijzingstabel bevat informatie die willekeurige toegang tot indirecte objecten in het bestand mogelijk maakt, zodat het hele bestand niet hoeft te worden gelezen om een bepaald object te lokaliseren. De tabel bevat een invoer van één regel voor elk meewerkend voorwerp, waarin de byte-offset van dat object in de hoofdtekst van het bestand wordt gespecificeerd. (Vanaf PDF 1.5 kunnen sommige of alle kruisverwijzingsinformatie ook in kruisverwijzingsstromen zijn opgenomen.

#### Bestandstrailer ####

De trailer van een PDF-bestand stelt een conforme lezer in staat om snel de kruisverwijzingstabel en bepaalde speciale objecten te vinden. Conforme lezers zouden een PDF-bestand vanaf het einde moeten lezen. De laatste regel van het bestand bevat alleen de markering voor het einde van het bestand, %%EOF. De twee voorgaande regels bevatten, één per regel en in volgorde, het trefwoord startxref en de byte-offset in de gedecodeerde stroom vanaf het begin van het bestand tot het begin van het xref-trefwoord in de laatste kruisverwijzingssectie.

### PDF-objecten ###

Een PDF-bestand bevat verschillende typen objecten die van de volgende typen zijn:

* Booleaanse waarden - die voorwaardelijk waar of onwaar vertegenwoordigen
* Getallen - Integer en reële waarden
* Strings - bevat tekens tussen haakjes
* Namen - begin met een voorwaarts / teken bijv. /ASomewhatLongerName resulteert in ASomewhatLongerName
* Arrays - PDF ondersteunt eendimensionale arrays. Arrays met hogere afmetingen kunnen worden geconstrueerd door arrays als geneste elementen te gebruiken
* Woordenboeken - verzameling objecten als sleutel-waardeparen. Het kan nul items bevatten.
* Streams - vertegenwoordigt een reeks bytes die ook van onbeperkte lengte kan zijn
* Null-object - vertegenwoordigt een null-waarde

Er kunnen andere andere objecten zijn, zoals opmerkingen, die worden geïntroduceerd met het %-teken en die 8-bits tekens kunnen bevatten.

### Indirecte objecten ###

Elk object in een PDF-bestand kan worden gelabeld als een indirect object. Indirecte objecten krijgen een unieke object-ID waarmee andere objecten ernaar kunnen verwijzen. Kruisverwijzingen naar deze worden bijgehouden in een indextabel en gemarkeerd met het xref-sleutelwoord dat de hoofdtekst volgt en de byte-offset geeft van elk indirect object vanaf het begin van het bestand.

### Lineaire en niet-lineaire PDF-lay-outs ###

PDF-lay-outs worden gecategoriseerd als bijna en niet-lineair, afhankelijk van de doeltoepassingen en andere factoren.

Niet-lineair - Niet-lineaire PDF-bestanden gebruiken minder schijfruimte in vergelijking met lineaire PDF-bestanden. PDF-pagina's van het document bevinden zich verspreid over het PDF-bestand en daarom zijn niet-lineaire bestanden langzamer in vergelijking met lineaire bestanden.

Lineaire PDF - Lineaire PDF-bestanden zijn gericht op online PDF-viewers en zijn zo geconstrueerd dat ze op een lineaire manier naar schijf worden geschreven. Dit vereist geen browser-plug-ins om het hele document eerst te laden voordat het wordt weergegeven.

### Objectenoverzicht ###

Zoals vermeld, is de PDF-body een verzameling van bovengenoemde objecten. PDF is grotendeels gebaseerd op PostScript zonder de besturingsfuncties van programmeertalen zoals if- en loop-opdrachten. Commando's uitgegeven door Postscript-code om grafische inhoud te genereren, worden verzameld en getokeniseerd naast alle bestanden, afbeeldingen of lettertypen waarnaar in het document wordt verwezen. Al deze inhoud wordt verzameld in één enkel bestand, wat resulteert in samengestelde PostScript-uitvoer.

#### Tekst ####

Tekst in PDF wordt weergegeven door tekstelementen die daadwerkelijk worden weergegeven met glyphs uit lettertypen. Een glyph is een grafische vorm en is onderhevig aan alle grafische manipulaties, zoals coördinatentransformatie. Vanwege het belang van tekst in de meeste paginabeschrijvingen, biedt PDF faciliteiten op een hoger niveau om glyphs gemakkelijk en efficiënt te beschrijven, selecteren en weergeven.

#### Grafisch ####

De grafische operators die in PDF-inhoudsstromen worden gebruikt, beschrijven het uiterlijk van pagina's die moeten worden gereproduceerd op een rasteruitvoerapparaat. De faciliteiten zijn bedoeld voor zowel printer- als displaytoepassingen. De grafische operators vormen zes hoofdgroepen:

* Operators voor grafische toestanden manipuleren de gegevensstructuur die de grafische toestand wordt genoemd, het globale raamwerk waarbinnen de andere grafische operators worden uitgevoerd. De grafische status omvat de huidige transformatiematrix (CTM), die de coördinaten van de gebruikersruimte die in een PDF-inhoudsstroom worden gebruikt, in kaart brengt in de coördinaten van het uitvoerapparaat. Het bevat ook de huidige kleur, het huidige uitknippad en vele andere parameters die impliciete operanden zijn van de schilderoperators.
* Padconstructieoperators specificeren paden, die vormen, lijntrajecten en verschillende soorten gebieden definiëren. Ze bevatten operators om een nieuw pad te beginnen, er lijnsegmenten en curven aan toe te voegen en het te sluiten.
* Path-painting-operators vullen een pad met een kleur, tekenen er een lijn langs of gebruiken het als een uitknipgrens.
* Andere tekenaars schilderen bepaalde zelfbeschrijvende grafische objecten. Deze omvatten gesamplede afbeeldingen, geometrisch gedefinieerde arceringen en volledige inhoudsstromen die op hun beurt reeksen grafische operators bevatten.
* Tekstoperators selecteren en tonen tekenglyphs uit lettertypen (beschrijvingen van lettertypen voor het weergeven van teksttekens). Omdat PDF glyphs behandelt als algemene grafische vormen, kunnen veel van de tekstoperatoren worden gegroepeerd met de grafische status- of tekenoperatoren. De datastructuren en mechanismen voor het omgaan met glyph- en lettertypebeschrijvingen zijn echter voldoende gespecialiseerd.
* Operators met gemarkeerde inhoud koppelen logische informatie op een hoger niveau aan objecten in de inhoudsstroom. Deze informatie heeft geen invloed op het weergegeven uiterlijk van de inhoud; het is handig voor toepassingen die PDF gebruiken voor het uitwisselen van documenten.

## Referenties ##

* [PDF-bestandsindeling: basisstructuur](https://resources.infosecinstitute.com/topics/hacking/pdf-file-format-basic-structure/)
* [PDF - Wikipedia](https://en.wikipedia.org/wiki/PDF)
* [PDF-referentie - Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

