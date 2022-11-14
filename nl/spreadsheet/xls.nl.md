{
  "date" : "2019-12-16",
  "keywords" :[ "XLS", "bestand", "extensie", "bestandsindeling", "Excel", "Spreadsheet"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Uw gids voor bestandsindelingen om te weten wat een XLS-bestand is en API's die ze kunnen maken en openen.",
  "title" :"Wat is XLS-bestandsindeling? Leer van File Format Experts!",
  "linktitle" : "XLS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-16"
}

## Wat is een XLS-bestand?

Bestanden met de XLS-extensie vertegenwoordigen Excel Binary File Format. Dergelijke bestanden kunnen worden gemaakt door Microsoft Excel en andere vergelijkbare spreadsheetprogramma's zoals OpenOffice Calc of Apple Numbers. Bestand opgeslagen door Excel staat bekend als werkmap, waarbij elke werkmap een of meer werkbladen kan hebben. Gegevens worden opgeslagen en weergegeven aan gebruikers in tabelindeling in werkblad en kunnen numerieke waarden, tekstgegevens, formules, externe gegevensverbindingen, afbeeldingen en grafieken omvatten. Met toepassingen zoals Microsoft Excel kunt u werkmapgegevens exporteren naar verschillende formaten, waaronder [PDF](/nl/pdf/), [CSV](/nl/spreadsheet/csv/), [XLSX](/nl/spreadsheet/xlsx/), [TXT](/nl/ tekstverwerking/txt/), [HTML](/nl/web/html/), [XPS](/nl/page-description-language/xps/), en verschillende andere. Het XLS-bestandsformaat werd vervangen door een meer open en gestructureerd formaat, XLSX, met de release van Microsoft Excel 2007. De nieuwste versies bieden nog steeds ondersteuning voor het maken en lezen van XLS-bestanden, hoewel XLSX nu de eerste keuze is voor gebruik.

## Korte geschiedenis

XLS is door Microsoft gemaakt voor gebruik met Microsoft Excel en staat ook bekend als Binary Interchange File Format (BIFF). Dit bestandstype werd voor het eerst geïntroduceerd door het onderdeel te maken van Excel voor Windows in 1987. De specificaties van het XLS-bestandsformaat werden in juni 2008 voor het eerst openbaar gemaakt als Revisie 1. Daarna werden de specificaties voortdurend bijgewerkt en was de laatste revisie beschikbaar. is vanaf augustus 2018 en is gemarkeerd als Revisie 8.0. Een korte geschiedenis van verschillende versies van het XLS-bestandsformaat is als volgt:

* Versie 7.0 (uitgebracht met office 95): deze versie van Excel was de meest robuuste en snellere van alle versies en interne herschrijvingen van streams werden bijgewerkt naar 32 bits.
* Versie 8 (uitgebracht met office 97): VBA werd geïntroduceerd als een standaardtaal en verwijderde natuurlijke taallabels werden voor het eerst in deze versie opgenomen. Het introduceerde ook voor het eerst een paperclip-kantoorassistent.
* Versie 9 (uitgebracht met office 2000): Er waren slechts kleine wijzigingen in versie 9, waarbij de paperclip office-assistent tegelijkertijd meerdere objecten kon vasthouden die voorheen niet mogelijk waren.
* Versie 10 (Uitgebracht met office XP): Deze versie bevatte geen merkbare verbetering.
* Versie 11 (uitgebracht met office 2003): Grote update in versie 11, Excel 2003 was de introductie van nieuwe tabellen.

## Specificaties XLS-bestandsindeling ##

Gegevens worden in een XLS-bestand als binaire streams gerangschikt in de vorm van een samengesteld bestand zoals beschreven in [MS-CFB]. Gegevens worden opgeslagen in het samengestelde bestand met behulp van opslagplaatsen, streams en substreams die informatie bevatten over de inhoud en structuur van een werkmap, inclusief werkmapgegevens zoals werkbladdefinities. Elke stream of substream bevat een reeks binaire records. Elke binaire record bevat nul of meer gestructureerde velden die de werkmapgegevens bevatten. Dit gedeelte geeft een kort overzicht van de XLS-bestandsstructuur, maar voor gedetailleerde specificaties voor bestandsindelingen moet u de [XLS-bestandsformatiespecificaties](https://msdn.microsoft.com/en-us/library/cc313154(v#office .12).aspx) document door Microsoft.

#### Stream en substream ####

Een werkmap wordt vertegenwoordigd door de werkmapstroom. Elk werkblad in een werkmap wordt vertegenwoordigd door Substreams. Bovendien heeft het een substroom van een grafiekblad, een substroom van een macroblad of een substroom van een dialoogvensterblad die de globale substroom volgt. Elke binaire stream of substream die werkmapgegevens bevat, MOET worden geschreven als een reeks binaire records.

#### Dossier ####

Informatie over functies in een werkmap wordt opgeslagen als een record dat een reeks bytes met variabele lengte is. Een binair record bestaat uit de volgende drie componenten:

**Recordtype:** Het recordtype is een niet-ondertekend geheel getal van twee bytes dat aangeeft welk type informatie door het record wordt gespecificeerd en hoe de structuur van de recordgegevens die specifiek zijn voor dit record, is geordend en gestructureerd. Record type waarden MOETEN een waarde zijn uit de Record Enumeration (paragraaf 2.3) of het record MOET gebruik maken van de toekomstige record architectuur (paragraaf 2.1.6).

**Recordgrootte**: de recordgrootte is een niet-ondertekend geheel getal van twee bytes dat het aantal bytes aangeeft dat de totale grootte van de recordgegevens aangeeft. De recordgrootte MOET groter zijn dan of gelijk zijn aan 0 en MOET kleiner zijn dan of gelijk zijn aan 8224.

**Recordgegevens:** De recordgegevenscomponent bevat velden die overeenkomen met een bepaald recordtype en vormen de rest van het record. De volgorde en structuur van de velden voor een bepaald recordtype worden gespecificeerd in de overeenkomstige sectie voor dat recordtype. De grootte van de recorddatacomponent MOET gelijk zijn aan de recordgrootte. Velden in de recordgegevenscomponent kunnen eenvoudige waarden, arrays van waarden, structuren van verschillende velden, arrays van velden en arrays van structuren bevatten.

#### Cellentabel ####

Cellen zijn de fundamentele blokken van een werkmap waarin de inhoud van de werkmap wordt opgeslagen, zoals tekst, formules en numerieke gegevens. Cellen houden de opgeslagen gegevens bij via een gegevensstructuur die de celtabel wordt genoemd. De celtabel zelf wordt opgeslagen in de volgorde van records die voldoen aan de CELLTABLE-regels die zijn gedefinieerd in het specificatiedocument. Het bestaat uit een reeks rijblokken waarbij de rijen in rijblokken zijn gerangschikt. Elk rijblok bevat rijen vanaf de eerste rij die gegevens bevat tot de laatste rij die gegevens bevat.

Gegevens of rijopmaak worden voor elk rijblok opgeslagen in een rijrecord. Elke cel die gegevens of individuele celopmaak bevat, wordt vertegenwoordigd door een record. Opmaak die aan een cel is gekoppeld, kan worden afgeleid van individuele celopmaak, rijopmaak, kolomopmaak of de standaard celopmaak. De prioriteitsvolgorde voor opmaak is individuele celopmaak met de hoogste prioriteit, gevolgd door rijopmaak, dan kolomopmaak en vervolgens de standaardcelopmaak. Cellen die geen gegevens bevatten en geen individuele opmaak bevatten, worden niet opgeslagen.

#### Formules ####

Een formule is een reeks waarden, celverwijzingen, namen, functies of operators in een cel die samen een nieuwe waarde produceren. Formules worden opgeslagen in een tokenized representatie die bekend staat als 'geparseerde expressies'. Een ontlede uitdrukking wordt tijdens runtime omgezet in een tekstuele formule voor weergave en bewerking door de gebruiker. Celformules worden gespecificeerd door de formulerecord. Matrixformules worden gespecificeerd door het matrixrecord. Gedeelde formules worden gespecificeerd door het ShrFmla-record.

#### Grafieken ####

Het kaartblad specificeert een kaart, een afbeelding die gegevens of de relaties tussen gegevenssets in een visuele vorm weergeeft, en een gegevenscache van een kaart, een lokale kopie van de gegevens die in de kaartgegevens worden gebruikt, of als koppelingen naar externe gegevensbronnen zijn verbroken. Het diagram specificeert groepen met één of twee assen, een set assen waartegen de diagramgegevens worden uitgezet en de reeks series, trendlijnen en foutbalken die in het diagram zijn gespecificeerd. Elke asgroep specificeert één tot vier diagramgroepen die het type visualisatie specificeren dat wordt gebruikt om de gegevens weer te geven. Elke reeks, trendlijn en foutbalk specificeert een grafiekgroep waaraan deze is gekoppeld.

#### Metagegevens ####

Metadata zijn aanvullende gegevens die zijn gekoppeld aan een bepaalde cel of de inhoud ervan. Metagegevens worden alleen voor toekomstige uitbreidbaarheid in BIFF8 vastgelegd.

#### Draaitabellen ####

Een draaitabel is een mechanisme voor het samenvatten van brongegevens om een overzicht te krijgen van de distributie van die gegevens. In een draaitabel worden toepasselijke kolommen van de brongegevens velden die kunnen worden gebruikt om gegevens samen te vatten. Wanneer de brongegevens van de draaitabel OLAP-brongegevens zijn, worden OLAP-hiërarchieën en sommige andere OLAP-entiteiten velden in de draaitabel.
Een draaitabel bestaat uit twee hoofdonderdelen, een draaitabelweergave en een draaitabelweergave. Er kunnen meerdere draaitabelweergaven zijn op basis van één niet-OLAP PivotCache.

#### Stijlen ####

Dit overzicht beschrijft hoe opmaak- en beveiligingsinformatie voor cellen in een blad (1) wordt gespecificeerd. Celopmaak bestaat uit verschillende sets eigenschappen:

* Lettertype-eigenschappen (vet, cursief, letterkleur, lettergrootte, enz...)
* Vuleigenschappen (voorgrondkleur, achtergrondkleur, patroon, verloop, enz...)
* Uitlijningseigenschappen (links, midden, rechts uitlijning, enz ...)
* Randeigenschappen (links, rechts, boven, onder, dik of dun, kleur, enz...)
* Eigenschappen voor nummeropmaak (datum, tijd, aantal decimalen, enz...)
* Beveiligingseigenschappen (vergrendeld, verborgen, enz ...)

Deze eigenschappen beschrijven in hun geheel hoe een bepaalde cel wordt weergegeven en afgedrukt.

## Referenties ##

* [[MS-XLS] - Excel binaire bestandsindelingsstructuur](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [[MS-CFB] - Samengesteld bestand binair bestandsformaat](https://msdn.microsoft.com/en-us/library/dd942138.aspx)

