{
  "date" : "2020-03-16",
  "keywords" :[ "DXF-bestand", "Bestandsindeling", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over DXF-bestandsindelingen en API's die DXF-bestanden kunnen maken en openen.",
  "title" :"DXF-bestandsindeling",
  "linktitle" : "DXF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een DXF-bestand?

DXF, Drawing Interchange Format, of Drawing Exchange Format, is een gelabelde gegevensweergave van een AutoCAD-tekeningbestand. Elk element in het bestand heeft een prefix geheel getal dat een groepscode wordt genoemd. Deze groepscode vertegenwoordigt eigenlijk het element dat volgt en geeft de betekenis aan van een data-element voor een bepaald objecttype. DXF maakt het mogelijk om bijna alle door de gebruiker gespecificeerde informatie in een tekeningbestand weer te geven.

Het DXF-bestandsformaat is door Autodesk ontwikkeld als CAD-gegevensbestandsformaat voor gegevensinteroperabiliteit tussen AutoCAD en andere toepassingen. Zo kunnen gegevens van andere formaten naar DXF naar AutoCAD worden geïmporteerd volgens de specificaties voor interoperabiliteit van het DXF-bestandsformaat.

## Korte geschiedenis ##


De geschiedenis van het DXF-bestandsformaat gaat terug tot 1982 toen het werd geïntroduceerd als onderdeel van AutoCAD 1.0. De eerste versies van AutoCAD ondersteunen alleen het ASCII-bestandsformaat van DXF. Met de release 10 van AutoCAD (en hoger) in 1988, werd ondersteuning voor zowel ASCII- als binaire DXF-bestandsindelingen geïntroduceerd in AutoCAD. In de eerdere stadia deelde Autodesk geen bestandsformaatspecificaties en daardoor was het niet eenvoudig om DXF-bestanden correct te importeren. Autodesk publiceert nu echter de DXF-specificaties en is beschikbaar voor het grote publiek.

## Specificaties bestandsindeling ##

Het DXF-bestandsformaat gebruikt de groepscode en waardeparen om de inhoud in secties te ordenen. Elke sectie is samengesteld uit records waarbij elk record bestaat uit een groepscode en een gegevensitem. Elke groepscode en waarde staan op een eigen regel in het DXF-bestand. Elke sectie begint met een groepscode 0 gevolgd door de tekenreeks SECTION. Dit wordt gevolgd door een groepscode 2 en een tekenreeks die de naam van de sectie aangeeft (bijvoorbeeld SECTIE1). Elke sectie is samengesteld uit groepscodes en waarden die de elementen ervan definiëren. Een sectie eindigt met een 0 gevolgd door de string ENDSEC.

DXF-bestandsindeling beschouwt objecten die verschillen van entiteiten. Objecten hebben hier geen grafische weergave, maar entiteiten wel. Zo wordt naar items in DXF verwezen als grafische objecten, terwijl objecten naar objecten worden aangeduid als niet-grafische objecten. De secties BLOCK en ENTITIES van het DXF-bestand bevatten entiteiten en het gebruik van groepscodes in deze twee secties is identiek. Het einde van een entiteit wordt aangegeven door de volgende 0-groep, die de volgende entiteit begint of het einde van de sectie aangeeft.

### Bestandsstructuur ###

Secties in een DXF-bestand zijn in de volgende volgorde gerangschikt:

|Sectie|Basisbeschrijving
---|---|
|Header|Deze sectie bevat algemene informatie over de tekening. Het is net als de functie Instellingen op uw telefoon, die de verschillende variabelen bevat die aan de tekening zijn gekoppeld en de bijbehorende waarden. De sectie Header definieert bijvoorbeeld welke AutoCAD-versie het DXF-bestand gebruikt (de $ACADVER-variabele) of de eenheid die wordt gebruikt om hoeken in het bestand te meten (de $AUNITS-variabele)
|Classes|De sectie CLASSES bevat de informatie voor door de toepassing gedefinieerde klassen waarvan de instanties verschijnen in de secties BLOCKS, ENTITIES en OBJECTS van de database.
|Tabellen|Deze sectie bevat definities voor verschillende tabellen, die elk een aantal verschillende symboolitems bevatten. Bijvoorbeeld het [regeltype](https://help.autodesk.com/view/ACD/2016/ENU/?guid=GUID-20B4D4B3-1220-426A-847B-5BBE36EC6FDF) tabel (LTYPE) definieert het patroon van streepjes, punten, tekst en symbolen in het DXF-bestand en hoe ze worden geschaald. Hier is een volledige lijst met tabellen in deze sectie:<ul><li> Tabel Applicatie-ID (APPID)</li><li> Blok Record (BLOCK_RECORD) tabel</li><li> Dimensiestijl (DIMSTYPE) tabel</li><li> Laag (LAAG) tabel</li><li> Lijntype (LTYPE) tabel</li><li> Tekststijl (STYLE) tabel</li><li> Tabel met gebruikerscoördinatensysteem (UCS)</li><li> Bekijk (VIEW) tabel</li><li> Viewport-configuratietabel (VPORT)</li></ul>
|Blokken|Deze sectie bevat de grafische objecten en tekenentiteiten waaruit elke blokverwijzing in de tekening bestaat.
|Entiteiten|Deze sectie bevat de actuele objectgegevens en grafische entiteiten van de tekening. Dit kunnen onbewerkte gegevens zijn - een cirkelentiteit wordt bijvoorbeeld gedefinieerd door de dikte, het middelpunt, de straal en de extrusierichting.
|Objecten|Hier vind je de niet-grafische delen van de tekening. Hier worden bijvoorbeeld AutoCAD-woordenboeken opgeslagen.

## Referenties ##

* [DXF-bestandsspecificaties](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [AutoCAD DXF door Wikipedia](https://en.wikipedia.org/wiki/AutoCAD_DXF)

