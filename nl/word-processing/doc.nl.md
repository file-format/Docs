{
  "date" : "2019-12-03",
  "keywords" :[ "doc", "bestand", "extensie", "bestandsindeling", "Word", "Document"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOC - Microsoft Word-documentbestand",
  "description":"Meer informatie over DOC-bestandsindelingen en API's die DOC-bestanden kunnen maken en openen.",
  "linktitle" : "DOC",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Wat is een DOC-bestand?

Bestanden met de extensie .doc vertegenwoordigen documenten die zijn gegenereerd door Microsoft Word of andere tekstverwerkingsdocumenten in binaire bestandsindeling. De extensie werd aanvankelijk gebruikt voor documentatie in platte tekst op verschillende besturingssystemen. Het kan verschillende soorten gegevens bevatten, zoals afbeeldingen, zowel opgemaakte als platte tekst, grafieken, diagrammen, ingesloten objecten, koppelingen, pagina's, pagina-opmaak, afdrukinstellingen en nog veel meer. Het formaat was populair voor allerlei soorten documentatie vanwege de verscheidenheid aan opties die het gebruikers biedt voor het schrijven van handleidingen, voorstellen, specificaties, cv's, artikelen of soortgelijke documenten. De bijgewerkte versie van DOC is [DOCX](/nl/Word%20Processing/DOCX/) die is gebaseerd op Office OpenXML waarvan de specificaties vrij beschikbaar zijn.

## Korte geschiedenis ##

WordPerfect, een product van [Corel](https://www.corel.com/en/), gebruikte DOC als uitbreiding van hun eigen formaat. In de jaren tachtig bleef WordPerfect het meest gebruikte gebruik op de meeste computers vanwege de gemakkelijke beschikbaarheid en conformiteit met de meeste computermachines en besturingssystemen. WordPerfect zag echter zijn ondergang op Windows OS toen Microsoft Microsoft Word introduceerde als het product voor het bestandsformaat voor documenten en de DOC-extensie koos voor hun eigen formaat. Naarmate Microsoft Word steeds populairder werd, onderging het DOC-bestandsformaat verschillende revisies van Microsoft Word 97 - 2003. Het was 2007 toen het standaard DOC-bestandsformaat werd vervangen door het Office Open XML-formaat (bekend als DOCX) en de nieuwe versies van Microsoft Word gebruikt nu deze nieuwe extensie als standaard bestandsformaat.

## Specificaties DOC-bestandsindeling - Meer informatie

Microsoft heeft de specificaties voor het DOC-bestandsformaat pas in 2008 vrijgegeven. In februari 2008 werden formaatspecificaties vrijgegeven voor het .doc-bestandsformaat onder de Microsoft Open Specification Promise. Hoewel de specificatie niet alle functies beschrijft die door het DOC-formaat worden gebruikt, geeft het voldoende informatie over de kennis die nodig is om met dit bestandsformaat te werken. Toch is reverse engineering vereist om gebruik te kunnen maken van de beschikbare informatie. De specificaties zijn verschillende keren bijgewerkt en de nieuwste [revisie](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) is 8.0 die is bijgewerkt vanaf augustus 2018 .

### Enkele fundamentele concepten ###

Voordat we ingaan op details over de bestandsformaatspecificaties voor DOC, zijn enkele fundamentele concepten nodig om te begrijpen om met dit bestandsformaat te kunnen werken.

**File Information Base (Fib):** De Fib-structuur bevat informatie over het document en specificeert de bestandsverwijzingen naar verschillende delen waaruit het document bestaat.
De Fib is een structuur met variabele lengte. Met uitzondering van het basisgedeelte dat een vaste grootte heeft, wordt elke sectie voorafgegaan door een telveld dat de grootte van de volgende sectie aangeeft.

**Tekenpositie:** CP of tekenpositie vertegenwoordigt een niet-ondertekend 32-bits geheel getal dat dient als de op nul gebaseerde index van een teken in de documenttekst. De locatie en grootte van elk teken in het bestand kan niet direct worden opgehaald en moet worden berekend met behulp van een vooraf gespecificeerd algoritme. Karakters zijn onder meer:

* Tekst van het document
* Ankers van objecten zoals voetnoten of tekstvakken
* Controletekens zoals alineamarkeringen en tabelcelmarkeringen

**PLC:** De PLC-structuur is een reeks CP's gevolgd door een reeks gegevenselementen. De data-elementen voor elke PLC moeten dezelfde grootte hebben van nul of meer bytes, en om deze reden moet het aantal CP's één meer zijn dan het aantal data-elementen. PLC-structuren zijn van verschillende typen waarbij elk type aangeeft of dubbele CP's voor dat type zijn toegestaan of niet. Een PLC-structuur bestaat uit:

* **aCP (variabele lengte):** Een array van CP-elementen. Elk type **PLC**-structuur specificeert de betekenis van de CP-elementen en het toegestane bereik.
* **aData (variabele lengte):** Elk type **PLC**-structuur specificeert de structuur en betekenis van de data-elementen, eventuele beperkingen op het aantal data-elementen en eventuele beperkingen op de daarin opgenomen data. Het specificeert ook de relatie tussen de data-elementen en de bijbehorende CP's.

**Geldige selectie:** De .DOC-bestandsconstructies worden voornamelijk beschreven door een reeks CP's. Er zijn een aantal [regels](https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx) gespecificeerd door Microsoft die in een dergelijk geval moeten worden gevolgd.

**STTB:** De STTB is een tekenreekstabel die bestaat uit een kop die wordt gevolgd door een reeks elementen. De waarde **cData** geeft het aantal elementen aan dat zich in de array bevindt.

**Opslag van eigenschappen:** Een Word-bestand kan verschillende elementen hebben, zoals tekst, alinea's, tabellen, afbeeldingen en secties, waarbij elk zijn eigen eigenschappen kan hebben. Eigenschappen hiervan worden in het Word-bestand opgeslagen als verschillen met de standaard. Dergelijke verschillen worden gespecificeerd door PRl dat bestaat uit een Single Property Modifier (Sprm) en zijn operand. Een applicatie kan de uiteindelijke set eigenschappen bepalen door het toepassen van lijsten van **Prl**s.

**Wachtwoordbeveiliging:** Word-bestanden kunnen ook met een wachtwoord worden beveiligd, waarvoor een van de volgende mechanismen kan worden gebruikt.

* XOR-verduistering
* Office binair document RC4-codering
* Office binair document RC4 CryptoAPI-codering

Als FibBase.fEncrypted en FibBase.fObfuscation beide 1 zijn, wordt het bestand versluierd door XOR-verduistering te gebruiken.

Als FibBase.fEncrypted 1 is en FibBase.fObfuscation 0 is, wordt het bestand versleuteld met behulp van Office Binary Document RC4 Encryption of Office Binary Document RC4 CryptoAPI Encryption, waarbij de EncryptionHeader wordt opgeslagen in de eerste FibBase.lKey-bytes van de Table-stroom. De EncryptionHeader.EncryptionVersionInfo geeft aan welk versleutelingsmechanisme is gebruikt om het bestand te versleutelen.

### Bestandsstructuur ###

Een binair Word-bestand in zijn originaliteit is een OLE samengesteld bestand dat uit verschillende opslagplaatsen en streams bestaat. Deze storages en streams hebben hun eigen structuur en grootte, die de parameters voor schrijven en lezen specificeren. Dit zijn:

#### WordDocument-stream ####

Deze stream bevat de documenttekst en andere informatie waarnaar wordt verwezen vanuit andere delen van het bestand. De stream heeft geen andere vooraf gedefinieerde structuur dan de FIB aan het begin, die verplicht is en op offset 0 moet staan. Deze stream mag niet groter zijn dan 2147 MB.

#### 1TableStream of 0TableStream ####

Een binair Word-bestand kan tabelstreams bevatten die bekend staan als 1Table-stream of 0Table-stream. Hiervan moet ten minste één in het document aanwezig zijn. Als een document echter zowel 1Table- als 0Table-streams bevat, wordt alleen de stream waarnaar wordt verwezen door base.fWhichTblStm gebruikt. De niet-verwezen stream MOET worden genegeerd.
De Table Stream MAG NIET groter zijn dan 2147 MB.

#### Data stroom ####

De datastroom heeft geen vooraf gedefinieerde structuur. Het bevat gegevens waarnaar wordt verwezen vanuit de FIB of uit andere delen van het bestand. Deze stream hoeft niet aanwezig te zijn als er geen verwijzingen naar zijn. De datastroom MAG NIET groter zijn dan 2147 MB.

#### Objectpoolopslag ####

De Object Pool-opslag bevat opslagruimten voor ingesloten OLE-objecten. Deze opslag hoeft niet aanwezig te zijn als er geen ingesloten OLE-objecten in het document zijn.

#### Aangepaste XML-gegevensopslag ####

De aangepaste XML-gegevensopslag is een optionele opslag waarvan de naam "MsoDataStore" MOET zijn.

#### Samenvatting informatiestroom ####

De Summary Information-stream is een optionele stream waarvan de naam "\005SummaryInformation" MOET zijn, waarbij \005 het teken met de waarde 0x0005 is, en niet de letterlijke tekenreeks "\005".

#### Document Samenvatting Informatiestroom ####

De Document Summary Information-stream is een optionele stream waarvan de naam "\005DocumentSummaryInformation" MOET zijn, waarbij \005 het teken is met de waarde 0x0005, niet de letterlijke tekenreeks "\005".

#### Encryptiestream ####

De versleutelingsstroom is een optionele stroom waarvan de naam "versleuteling" MOET zijn. Deze stream MOET NIET aanwezig zijn tenzij aan beide van de volgende voorwaarden is voldaan:

* Het document is gecodeerd met Office Binary Document RC4 CryptoAPI-codering.
* De fDocProps-waarde wordt ingesteld in de EncryptionHeader.Flags.

#### Macro's Opslag ####

De macro's-opslag is een optionele opslag die de macro's voor het bestand bevat. Indien aanwezig, MOET het een Project Root Storage zijn.

#### XML-handtekeningen Opslag ####

De opslag voor XML-handtekeningen is een optionele opslag waarvan de naam "_xmlsignatures" MOET zijn.

#### Handtekeningen streamen ####

De handtekeningenstroom is een optionele stroom waarvan de naam "_signatures" MOET zijn. Deze stream bevat digitale handtekeningen.

#### Beheer van informatierechten Opslag van gegevensruimte ####

De Information Rights Management Data Space-opslag is een optionele opslag waarvan de naam "\006DataSpaces" MOET zijn, waarbij \006 het teken met de waarde 0x0006 is en niet de letterlijke tekenreeks "\006". Als deze opslag aanwezig is, MOET ook de Protected Content Stream aanwezig zijn.
Als deze opslag aanwezig is, MOETEN alle gespecificeerde streams en opslagen anders dan deze opslag en de beschermde inhoudstroom worden gelezen uit de beschermde inhoudstroom zoals gespecificeerd in [MS-OFFCRYPTO] en als een van die stromen en opslagen bestaat buiten de beschermde inhoud Stream, ze MOETEN worden genegeerd.

#### Beveiligde contentstream ####

De Protected Content Stream is een optionele stream waarvan de naam "\009DRMContent" MOET zijn, waarbij \009 het teken is met de waarde 0x0009, en niet de letterlijke tekenreeks "\009".
Als deze stream aanwezig is, MOET ook de Information Rights Management Data Space Storage aanwezig zijn.

## Referenties ##

* [MS-DOC-specificaties voor bestandsvorming](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)
* [Doc Computing](https://en.wikipedia.org/wiki/Doc_(computing))

