{
  "date" : "2019-10-11",
  "keywords" :[ "mpx-bestand", "mpx-bestandsformaat", "wat is een mpx-bestand", "bestand", "mpx-voorbeeld", "mpx-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPX - Microsoft Project Exchange-bestandsindeling",
  "description":"Meer informatie over de MPX-bestandsindeling en API's die MPX-bestanden kunnen maken en openen.",
  "linktitle" : "MPX",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## Wat is een MPX-bestand? ##

Een bestand met de extensie .mpx is een Microsoft Exchange-bestandsindeling. Een MPX-bestandsformaat is ontwikkeld door Microsoft Project (MSP) om de uitwisseling van projectinformatie tussen MSP en andere toepassingen die het MPX-bestandsformaat ondersteunen, te vergemakkelijken, waaronder Primavera Project Planner, Sciforma en Timerline Precision Estimating. Met behulp van de MPX-bestanden kunt u allerlei soorten informatie van een project naar een ander systeem overbrengen, zoals gedetailleerde informatie over resourcetoewijzingen, kalenderinformatie of informatie uit het dialoogvenster Projectinfo.

Microsoft Project 4.0 introduceerde ondersteuning voor het maken en lezen van MPX-bestandsindelingen die nog steeds werden gebruikt via Microsoft Project 98. Ondersteuning voor het maken van MPX-bestanden heeft echter de release van Microsoft Project 2000 stopgezet en de versies tot Microsoft Project 2010 ondersteunen alleen MPX-lezen. MPX-bestandsindeling wordt niet ondersteund in versies later dan MSP 2010.

## MPX-bestandsindeling ##

In deze sectie wordt een overzicht gegeven van de specificaties van het MPX-bestand. Volledige specificaties zijn te vinden in deze [Kennisbank](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) artikel en kan worden doorverwezen voor details.

### Records ###

Een Record van het MPX-bestand bestaat uit informatie voor het project. Er zijn verschillende soorten records waarbij elk record zijn eigen volgorde heeft. Elk recordtype wordt geïdentificeerd door zijn recordnummer. Voor een MPX-bestand is het noodzakelijk om het recordtype Bestandscreatie te bevatten. Andere soorten records zijn niet verplicht. De volgende tabel toont alle recordtypen, hun recordnummers en het aantal records dat elk type in het MPX-bestand kan bevatten. Opname van records in het MPX-bestand moet de tabelvolgorde volgen, waarbij opmerkingen overal worden ingevoegd.

|Recordnaam|Recordnummer|Maximum aantal records
---|---|---|
|Bestand aanmaken (vereist)|geen|1
|Valuta-instellingen|10|1
|Standaardinstellingen|11|1
|Datum en tijd instellingen|12|1
|Basiskalenderdefinitie|20|250
|Basis kalenderuren|25| 7 per basiskalenderdefinitierecord
|Basiskalender uitzondering|26| 250 per basiskalenderdefinitierecord
|Projectkoptekst|30|1
|Text Resource Table Definition|140|1- (Of u kunt het record Numeric Resource Table Definition gebruiken)
|Numerieke resourcetabeldefinitie|41|1
|Bron|50|9.999
|Bronnotities|51| 1 per resourcerecord
|Definitie van resourcekalender|55| 1 per resourcerecord
|Bron Kalender Uren|56| 7 per resourcekalender
|Bronkalender uitzondering| 57|250 per resourcekalender
|Text Task Table Definition|60|1 (Of u kunt het record Numeric Task Table Definition gebruiken)
|Numerieke taaktabeldefinitie|61|1
|Taak|70|9
|Taaknotities|71| 1 per taakrecord
|Terugkerende taak|72| 1 per taakrecord
|Resourcetoewijzing|75| 100 per taakrecord
|Opdracht Werkgroepvelden|76| 1 per opdrachtrecord
|Projectnamen|80|500
|DDE- en OLE-clientkoppelingen|81|500
|Opmerkingen|0|onbeperkt

### Bestandsstructuur ###

Een MPX-bestand bestaat uit de hierboven genoemde records die op een vooraf ingestelde manier in het bestand zijn gerangschikt. Details over deze recordtypen worden als volgt besproken:

**File Creation Record (FCR):** Dit is een verplicht record met als doel het identificeren van:

* Bestandsformaat (MPX)
* Lijstscheidingsteken dat in het bestand wordt gebruikt
* Programma- en versienummer gebruikt om het bestand te maken
* Versienummer van het MPX-bestandsformaat dat in het bestand wordt gebruikt
* Codepagina gebruikt om het bestand te maken

Dit moet het eerste record in het bestand zijn. Bij het exporteren vanuit Microsoft Project wordt het lijstscheidingsteken opgegeven in het item Landinstellingen in het Configuratiescherm van Windows. Een FCR-record bevat de volgende velden:

* MPX onmiddellijk gevolgd door het lijstscheidingsteken
* Programmanaam/-ID
* Versienummer van het bestand
* Codepagina (850, 437, MAC, ANSI)

Het record kan bijvoorbeeld informatie **MPX, Microsoft Project, 3.0** bevatten, die aangeeft dat een komma wordt gebruikt als lijstscheidingsteken in dit MPX-bestand. De versie van de MPX-indeling die in het bestand wordt gebruikt, wordt geëxporteerd vanuit Microsoft Project versie 3.0.

**Valuta-instellingen** Deze record, met recordnummer 10, specificeert instellingen voor de valuta-opties in het dialoogvenster Opties. Als dit record niet is opgenomen, worden de huidige instellingen in het dialoogvenster Opties gebruikt. De scheidingstekens voor duizendtallen en decimalen worden gespecificeerd in het item Regionale instellingen in het Configuratiescherm van Windows.
De velden in dit record zijn:

* Symbool van munteenheid
* Symboolpositie (0 # na, 1 # ervoor, 2 # na met een spatie, 3 # ervoor met een spatie)
* Valutacijfers (0,1,2)
* Scheidingsteken voor duizenden
* Decimaalscheidingsteken

**Voorbeeld:** 10,$,1,2,",",.
In dit voorbeeld wordt aangegeven dat valutawaarden een dollarteken ($) ervoor bevatten, dat er twee cijfers achter de komma staan, dat een komma wordt gebruikt om duizendtallen te scheiden en dat een punt wordt gebruikt als de komma. Omdat het lijstscheidingsteken is opgenomen in het veld Scheidingsteken voor duizendtallen, wordt het veld tussen aanhalingstekens geplaatst.

**Standaardinstellingen:** Deze record, met recordnummer 11, specificeert instellingen voor de standaardopties in het dialoogvenster Opties. Als er geen duur is opgegeven, moet de standaardeenheid voor duur worden ingesteld voor correcte berekeningen van de duureenheid. Als dit record niet is opgenomen, worden de huidige instellingen in het dialoogvenster Opties gebruikt.
De velden in dit record zijn:

* Standaard duureenheden (0 # minuten, 1 # uur, 2 # dagen, 3 # weken)
* Standaard duurtype (0 # niet vast, 1 # vast)
* Standaard werkeenheden (0 # minuten, 1 # uur, 2 # dagen, 3 # weken)
* Standaard uren/dag
* Standaard uren/week
* Standaard standaardtarief
* Standaard overurentarief
* Taakstatus bijwerken Updates bronstatus (0 # nee, 1 # ja)
* Gesplitste lopende taken (0 # nee, 1 # ja)

**Datum- en tijdinstellingen:** Deze record, met recordnummer 12, specificeert instellingen voor de datum- en tijdopties in het dialoogvenster Opties en de optie Bartekst Datumnotatie in het dialoogvenster Lay-out. Als dit record niet is opgenomen, worden de huidige instellingen in het dialoogvenster Opties gebruikt.
\\De velden in dit record zijn:

* Datumvolgorde (0 # maand/dag/jaar, 1 # dag/maand/jaar, 2 # jaar/maand/dag)
* Tijdnotatie (0 # 12 uur, 1 # 24 uur)
* Standaardtijd (aantal minuten na middernacht)
* Datumscheidingsteken
* Tijdscheidingsteken
* 0:00 tot 11:59 Tekst
* 12:00 tot 23:59 Sms
* Datumnotatie (0 -14)*
* Staaftekst Datumnotatie (0 -194)*

**Basiskalenderdefinitie:** Deze records, met recordnummer 20, definiëren basiskalenders en hun werk- en niet-werkdagen van de week. De standaardinstellingen worden gebruikt als er een dag geen invoer is. De standaardinstellingen zijn maandag tot en met vrijdag voor werkdagen en zaterdag en zondag voor niet-werkdagen. In deze record is het veld Naam verplicht. Voor elk van de dagen geeft een invoer van 0 aan dat de dag een niet-werkdag is, en een invoer van 1 geeft aan dat de dag een werkdag is.
De velden in dit record zijn:

* Naam
* Zondag
* Maandag
* Dinsdag
* Woensdag
* Donderdag
* Vrijdag
* Zaterdag

**Basis kalenderuren:** Deze records, met recordnummer 25, specificeren de werkuren voor de dagen van de week als deze afwijken van de standaardinstellingen. De standaard werkuren zijn 8.00 uur tot 12.00 uur en 13.00 uur tot 17.00 uur. Elke record basiskalenderuren verwijst naar de voorgaande basiskalenderdefinitierecord. Maximaal zeven van deze records kunnen elk Base Calendar Definition-record volgen.

* Dag van de week (1 - 7, waarbij 1 # zondag en 7 # zaterdag)
* Vanaf Tijd 1
* Naar Tijd 1
* Vanaf Tijd 2
* Tot Tijd 2
* Vanaf tijd 3
* Tot Tijd 3

**Uitzondering basiskalender:** Deze records, met recordnummer 26, definiëren de uitzonderingen op de dagen en uren die zijn opgegeven in de vorige twee recordtypen. Maximaal 250 van deze records kunnen elk Base Calendar Definition-record volgen. Deze records moeten in chronologische volgorde worden vermeld. Als een uitzondering één dag is, kunt u het veld Tot datum leeg laten. Als er geen tijden zijn aangegeven, worden de standaardtijden van 8:00 uur tot 12:00 uur en 13:00 uur tot 17:00 uur gebruikt.
De velden in dit record zijn:

* Van datum
* Tot op heden
* Niet-werkend/werkend (0 # niet-werkend, 1 # werkend)
* Vanaf Tijd 1
* Naar Tijd 1
* Vanaf Tijd 2
* Tot Tijd 2
* Vanaf tijd 3
* Tot Tijd 3

**Projectkoptekst:** Deze record, met recordwaarde 30, stelt globale projectvelden in, zoals de startdatum van het project en de einddatum van het project. De velden in dit record komen overeen met de informatie in de dialoogvensters Projectinfo en Statistieken.
De velden en tabbladen in dit record zijn:

* Project tabblad
* Bedrijf
* Manager
* Kalender (standaard gebruikt als er geen invoer is)
* Startdatum (dit veld of het volgende veld wordt berekend voor een geïmporteerd bestand, afhankelijk van de instelling Schedule From)
* Eind datum
* Schema Van (0 # start, 1 # finish)
* Huidige datum*
* Opmerkingen
* Kosten
* Basiskosten
* Werkelijke kosten
* Werk
* Basislijn werk
* Echt werk
* Werk
* Looptijd*
* Basislijnduur*
* Werkelijke duur
* Percentage compleet
* Basislijn starten
* Basislijn afwerking
* Werkelijke start
* Werkelijke afwerking
* Start variantie
* Afwerkingsvariant
* Onderwerp
* Auteur
* Trefwoorden

**Tekstresourcetabeldefinitie**: deze record geeft de resourcevelden op volgorde weer die worden geïmporteerd of geëxporteerd. Voor geïmporteerde bestanden moeten de namen overeenkomen met de veldnamen die in Microsoft Project worden gebruikt. Voor geëxporteerde bestanden komt dit record uit de resource Export-tabel. Dit record of het record Numerieke resourcetabeldefinitie moet worden gebruikt. Bij het exporteren vanuit Microsoft Project worden beide records opgenomen.

**Numerieke resourcetabeldefinitie:** Met behulp van getallen in plaats van namen geeft dit record de resourcevelden op volgorde weer die worden geïmporteerd of geëxporteerd. Dit is een alternatieve methode voor het identificeren van de resourcevelden die zijn opgenomen in elk resourcerecord en is handig bij het definiëren van een MPX-bestand dat is gemaakt door een product in een vreemde taal.

**Bron:** Deze records bevatten de informatie voor elke bron die wordt geïmporteerd of geëxporteerd. Elk resourcerecord beschrijft één resource. Wanneer u informatie importeert, worden de velden die zijn opgenomen gedefinieerd door het record Definitie tekstbrontabel of het record Numerieke brontabeldefinitie. Wanneer u informatie exporteert, zijn de velden die worden opgenomen de velden die worden vermeld in de tabel Resource Export.

**Bronnotities:** Deze records bevatten opmerkingen over de direct voorafgaande resourcerecord. Voor een nieuwe regel binnen de notitie wordt ASCII-teken 127 gebruikt. Als de notitie het lijstscheidingsteken bevat, plaatst u de notitie tussen aanhalingstekens.

**Definitie van resourcekalender:** Deze records definiëren de werkdagen voor de resource die is opgegeven in de onmiddellijk voorafgaande resourcerecord. Als er voor geïmporteerde bestanden geen invoer is voor het veld Basiskalendernaam, wordt Standaard gebruikt. Geen invoer voor de specifieke dag geeft aan dat de dag is ingesteld op de standaard (2). Als er geen Resource Calendar Definition-records zijn, wordt Standaard gebruikt als de basiskalender voor de resource, met standaard voor de dagen. Voor elk van de dagen geeft een invoer van 0 aan dat de dag een niet-werkdag is, 1 geeft aan dat de dag een werkdag is en 2 geeft aan dat de standaarddag wordt gebruikt.

**Resourcekalenderuren:** Deze records definiëren de werkuren voor de resource die verschillen van de basiskalender die door de resource wordt gebruikt. Deze records zijn van toepassing op het record Resourcekalenderdefinitie onmiddellijk voorafgaand aan dit record. Maximaal zeven van deze records kunnen elk record voor resourcekalenderdefinitie volgen.

**Uitzondering bronkalender:** Deze records definiëren de uitzonderingen op de dagen en uren die zijn opgegeven in de vorige twee recordtypen. Maximaal 250 van deze records kunnen elk Resource Calendar Definition-record volgen. Deze records moeten in chronologische volgorde worden vermeld. Als de uitzondering slechts één dag is, kunt u het veld Tot datum leeg laten. Als er geen tijden zijn aangegeven, worden de standaardtijden van 8:00 uur tot 12:00 uur en 13:00 uur tot 17:00 uur gebruikt.

**Tekst Taaktabel Definitie:** Dit record vermeldt de taakvelden, in volgorde, die worden geïmporteerd of geëxporteerd. Voor geïmporteerde bestanden moeten de namen overeenkomen met de veldnamen die in Microsoft Project worden gebruikt. Als het bestand wordt geëxporteerd, komt dit record uit de tabel Taak Exporteren. Bij het exporteren vanuit Microsoft Project worden beide records opgenomen. Velden die worden berekend door Microsoft Project, zoals Geplande start en Geplande einddatum, worden genegeerd als ze worden geïmporteerd. Als u vaste begin- of einddatums voor taken heeft, gebruikt u de velden Type beperking en Datum beperking.

**Numerieke taaktabeldefinitie:** Met behulp van getallen in plaats van namen, geeft dit record de taakvelden weer, in volgorde, die worden geïmporteerd of geëxporteerd. Dit is een alternatieve methode voor het identificeren van de taakvelden die in elk taakrecord zijn opgenomen en is handig bij het definiëren van een MPX-bestand dat is gemaakt door een product in een vreemde taal.

**Taak:** Deze records bevatten de informatie voor elke taak die wordt geïmporteerd of geëxporteerd. Elk Taakrecord beschrijft één taak. Wanneer u informatie importeert, worden de velden die zijn opgenomen gedefinieerd door het record Teksttaaktabeldefinitie of het record Numerieke taaktabeldefinitie. Wanneer u informatie exporteert, zijn de velden die worden opgenomen in de tabel Taak Exporteren.

**Taaknotities:** Deze records bevatten notities over de onmiddellijk voorafgaande taakrecord. Gebruik ASCII-teken 127 om een nieuwe regel binnen de notitie aan te geven. Als de notitie het lijstscheidingsteken bevat, plaatst u de notitie tussen aanhalingstekens.

**Resourcetoewijzing**: deze records bevatten informatie over de resources die zijn toegewezen aan de taak die is gedefinieerd in de voorgaande taakrecord. Als u bestanden samenvoegt en u wilt dat de informatie over de resourcetoewijzing behouden blijft, moet u de informatie opnemen in het MPX-bestand. Als je samenvoegt, worden alle bestaande toewijzingen op samengevoegde taken verwijderd. Als u bestanden samenvoegt op basis van unieke ID's, worden resources toegewezen met behulp van de Resource Unique ID's in plaats van ID's.

**Werkgroepvelden voor brontoewijzing:** Deze records bevatten de informatie die bij elke toewijzing is opgeslagen voor de werkgroepfuncties van Microsoft Project 4.0 en 4.1. Als u de Workgroup-functies gebruikt, moet u dit record opnemen om ervoor te zorgen dat er geen informatie verloren gaat.

**Projectnamen:** Deze records bevatten alle DDE-linknamen die in het project zijn opgeslagen.

**DDE- en OLE-clientkoppelingen:** Deze records bevatten de DDE-koppelingen naar het project.

**Opmerkingen:** Deze records kunnen worden gebruikt om opmerkingen aan het bestand toe te voegen en kunnen op elke positie in het bestand worden weergegeven. Elke Opmerkingen-record moet beginnen met een '0'.

## Problemen bij het openen van een MPX-bestand ##

Hier is de lijst met enkele veelvoorkomende problemen die zich kunnen voordoen en een slechte werking van het MPX-formaat kunnen veroorzaken:

* Afwezigheid van ondersteunende software
* Corrupt bestand
* Geïnfecteerd bestand door virus
* Geen toegangsrecht in het systeem om de bestanden te openen
* Verouderde schijf in uw systeem
* Extensie van het bestand is hernoemd

## Referenties ##

* [MPX - Microsoft Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)

