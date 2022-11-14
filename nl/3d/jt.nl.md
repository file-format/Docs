{
  "date" : "2019-12-12",
  "keywords" :[ "JT", "bestand", "extensie", "formaat", "3D fbx", "" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over JT-bestandsindeling en API's die JT-bestanden kunnen maken en openen.",
  "title" :"JT - Jupiter Tessellation-bestandsindeling",
  "linktitle" : "JT",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een JT-bestand?

**JT** (Jupiter Tessellation) is een efficiënt, industriegericht en flexibel ISO-gestandaardiseerd 3D-gegevensformaat ontwikkeld door Siemens PLM Software. Mechanische CAD-domeinen van de lucht- en ruimtevaart, auto-industrie en zware apparatuur gebruiken JT als hun meest toonaangevende 3D-visualisatieformaat.

JT-formaat is een scènegrafiek die de attributen en knooppunten ondersteunt die CAD-specifiek zijn. Er worden geavanceerde compressietechnieken gebruikt om facetgegevens (driehoeken) op te slaan. Dit formaat is gestructureerd om visuele attributen, product- en fabricage-informatie (PMI) en metadata te ondersteunen. Er is een goede ondersteuning voor asynchrone streaming van content. In de zware mechanische industrie gebruiken professionals JT-bestanden in hun CAD-oplossingen en softwareprogramma's voor productlevenscyclusbeheer (PLM) om de geometrie van gecompliceerde goederen te onderzoeken.

Omdat JT bijna alle belangrijke 3D CAD-formaten ondersteunt, kan de assemblage een verscheidenheid aan combinaties aan, die bekend staat als "multi-CAD". Deze multi-CAD-assembly is altijd goed beheerd en up-to-date omdat de synchronisatie tussen native CAD-productbeschrijvingsbestanden met de bijbehorende JT-bestanden automatisch plaatsvindt. JT-bestanden zijn oorspronkelijk lichtgewicht, dus geschikt voor internetsamenwerkingen. Bedrijven werken samen door het verzenden van 3D-visualisaties via de media veel gemakkelijker in vergelijking met "zware" originele CAD-bestanden. Bovendien zorgen JT-bestanden voor veel beveiligingsfuncties die het delen van intellectueel eigendom veiliger maken.

## Korte geschiedenis van JT-bestandsindeling

Engineering Animation, Inc. en Hewlett Packard waren de oorspronkelijke ontwerpers van JT, die dat formaat ontwikkelden als de Direct Model-toolkit. Nadat EAI was overgenomen door UGS Corp. werd JT een onderdeel van de suite van UGS. Begin 2007 kondigde UGS JT aan als hun master 3D-formaat. In hetzelfde jaar kocht Siemens AG UGS en bleek Siemens PLM Software te zijn. Siemens gebruikt JT als het gemeenschappelijke formaat voor interoperabiliteit en gegevensarchivering. In 2009 accepteerde ISO de JT-specificatie voor publicatie als een ISO Publicly Available Specification (PAS). Medio 2010 kondigde ProSTEP iViP aan dat op industrieel niveau JT en STEP AP 242 XML samen kunnen worden gebruikt om het maximale voordeel in data te behalen. scenario's uitwisselen. In 2012 is JT officieel uitgeroepen tot een ISO-gestandaardiseerd (ISO 14306:2012 (ISO JT V1)) 3D-visualisatieformaat.

## JT-bestandsindeling ##

Alle objecten in het JT-formaat worden weergegeven door middel van een object-ID en verwijzingen tussen objecten worden afgehandeld door middel van de identificatie van het object waarnaar wordt verwezen. De integriteit van deze objectreferenties kan worden gehandhaafd door middel van pointers die unswizzling/swizzling zijn.

Een JT-bestand is gerangschikt als een reeks blokken en het kopblok is altijd het eerste gegevensblok in het bestand. Een reeks gegevenssegmenten en een TOC-segment volgen onmiddellijk op het kopblok. Het ene gegevenssegment (6 LSG-segment) dat een referentie-compatibel JT-bestand heeft, bestaat altijd. TOC-segment bevat de locatie-informatie van alle andere gegevenssegmenten van dat bestand.

{{< figure src="../JT-1.png" alt="JT-bestandsindeling" >}}

### Bestandskop ###

Bestandskoptekst is het eerste blok in de gegevenshiërarchie van het JT-bestand. Versie-informatie en TOC-locatie-informatie zijn ingesloten in de kop, waardoor laders gemakkelijker bestanden kunnen lezen. De inhoud van de bestandskop is als volgt gerangschikt.

### TOC-segment ###

Het TOC-segment moet in een bestand voorkomen en bevat identificatie- en locatie-informatie van alle andere gegevenssegmenten. De werkelijke locatie van het TOC-segment wordt gespecificeerd door het veld TOC-offset van de bestandskop. Elk afzonderlijk adresseerbaar gegevenssegment wordt vertegenwoordigd door TOC-invoer in een TOC-segment.

### Gegevenssegment ###

JT-bestand definieert alle opgeslagen gegevens binnen een gegevenssegment. Sommige gegevenssegmenten kunnen alle gegevensbytes aan informatie die in het segment zijn achtergebleven, comprimeren. Gegevenssegmenten hebben de volgende structuur:

![alt text](../JT-2.png "JT Data Segment")

De volgende tabel beschrijft verschillende soorten gegevenssegmenten:

|Naam|Beschrijving
---|---|
|LSG-segment|Bestaat uit een verzameling objecten die zijn verbonden via gerichte verwijzingen om LSG (gerichte acyclische grafiekstructuur) te vormen
|Shape LOD-segment|bevat de bepalende gegevens voor de geometrische vormen (bijv. hoekpunten, normalen, polygonen, enz.)
|JT B-Rep Segment|Met een element voor de gegevens om de precieze geometrische grens voor een individueel gedeelte in JT B-Rep-formaat weer te geven.
|XT B-Rep segment|Met een element voor de gegevens om de precieze geometrische grens voor een individueel gedeelte in grensweergaveformaat weer te geven
|Wireframe-segment|De gegevens vertegenwoordigen een nauwkeurig 3D-draadframe voor een bepaald gedeelte dat wordt gedefinieerd door een element in dit segment.
|Metagegevenssegment|Hiermee kunnen metagegevens in verschillende adresseerbare segmenten worden opgeslagen.
|JT ULP-segment|Het hebben van een element voor de gegevens om de semi-nauwkeurige geometrische grens voor een individueel gedeelte in JT ULP-formaat weer te geven.
|JT LWPA-segment|Bevat een element dat analytische gegevens voor een bepaald onderdeel definieert. LWPA omvat de verzameling analytische oppervlakken in de b-rep-definitie van het onderdeel.

## Compressie ##

De transmissie- en opslagvereisten van 3D-modellen zijn veeleisender, dus JT-bestanden kunnen profiteren van compressie. Een JT-gegevensmodel kan zijn samengesteld uit verschillende bestanden met verschillende compressietechnieken, maar het compressieproces is transparant voor de JT-gegevensgebruiker.

Tot dusver zijn JT Open Toolkit (als standaard) en geavanceerde compressie twee compressietechnieken die door JT-bestanden worden gebruikt. JT Open Toolkit maakt gebruik van een eenvoudig, verliesloos compressie-algoritme, terwijl de geavanceerde compressie een meer verfijnde, domeinspecifieke compressietechniek gebruikt die leidt tot compressie met verlies van geometrie. Clienttoepassingen geven de voorkeur aan geavanceerde compressie boven het gebruik van standaardcompressie, omdat geavanceerde compressie vrij hoge compressieverhoudingen oplevert. Achterwaartse compatibiliteit met gewone JT-toepassingen voor het bekijken van bestanden wordt gehandhaafd door middel van standaardcompressie. De compressievorm moet compatibel zijn met de JT-bestandsformaatversie die kan worden gezien wanneer een JT-bestand wordt geopend met een teksteditor en wordt ingesloten in ASCII-headerinformatie.

## Referenties ##

* [JT-bestandsindelingreferentie](https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)
* [JT (visualisatieformaat)](https://en.wikipedia.org/wiki/JT_(visualization_format)#Data_model)

