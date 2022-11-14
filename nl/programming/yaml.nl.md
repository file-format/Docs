{
  "date" : "2019-10-11",
  "keywords" :[ "yaml", ".yaml", "wat is een yaml-bestand", "hoe yaml-bestand te openen", "extensie", "bestand", "yaml-bestand", "yaml-bestandsindeling", ".yaml-extensie" , "yaml vs json" ,"YAML-bestandsvoorbeeld", "docker yaml-bestandsvoorbeeld"],
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "description" :" Meer informatie over de YAML-bestandsindeling en API's die een YAML-bestand kunnen maken en openen.",
  "title" :"YAML-bestandsindeling",
  "linktitle" : "YAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-05"
}

## Wat is een YAML-bestand? ##

**YAML-bestand** bestaat uit een taal YAML (YAML Ain't Markup Language), een op Unicode gebaseerde taal voor gegevensserialisatie; gebruikt voor configuratiebestanden, internetberichten, objectpersistentie, enz. YAML gebruikt de .yaml-extensie voor zijn bestanden. De syntaxis is onafhankelijk van een specifieke programmeertaal. Kortom, de YAML is ontworpen voor menselijke interactie en om goed te werken met moderne programmeertalen. Ondersteuning voor het serialiseren van willekeurige native datastructuren verhoogde de leesbaarheid van de YAML-bestanden, maar het maakte het parseren en het genereren van bestanden een beetje ingewikkeld.

## Korte geschiedenis ##

YAML werd voor het eerst voorgesteld in 2001 en werd ontwikkeld door Clark Evans, Ingy döt Net en Oren Ben-Kiki. Van YAML werd voor het eerst gezegd dat het "Nog een andere opmaaktaal" betekende om zijn doel als opmaaktaal aan te geven. Het werd later herbestemd als "YAML Aint Markup Language" om het doel ervan aan te geven als data-georiënteerd.


## YAML-bestandsindeling ##

YAML-bestand bestaat uit de volgende gegevenstypen:

- **Scalars**: Scalars zijn waarden zoals Strings, Integers, Booleans, etc.
- **Sequences**: Sequenties zijn lijsten waarbij elk item begint met een koppelteken (-). Lijsten kunnen ook worden genest.
- **Mappings**: Mapping geeft de mogelijkheid om sleutels met waarden weer te geven.

### Syntaxis ###

- **Witruimte**: Inspringing van witruimte wordt gebruikt om nesting en algemene structuur aan te geven.

```jaml
naam: John Smith
contact:
thuis: 1012355532
kantoor: 5002586256
adres:
straat: |
123 Tornado Alley
Suite 16
stad: East Centreville
staat: KS
```

- **Opmerkingen**: opmerkingen worden geschreven beginnend met het "#"-symbool.

```jaml
# Dit is een YAML-opmerking
```

- **Lijsten**: koppelteken (-) wordt gebruikt om lijstleden aan te geven waarbij elk lid op een aparte regel staat. Lijstleden kunnen ook tussen vierkante haken ([...]) worden geplaatst, waarbij leden worden gescheiden door komma's (,).

```jaml
  - A
  - B
  - C
```

```jaml
[A, B, C]
```

- **Associatieve array**: een associatieve array is omgeven door accolades ({...}). De sleutels en waarden worden gescheiden door een dubbele punt (:) en elk paar wordt gescheiden door een komma (,).

```jaml
  {name: John Smith, age: 20}
```

- **Strings**: String kan worden geschreven met of zonder dubbele aanhalingstekens ("") of enkele aanhalingstekens (').

```jaml
Voorbeeldreeks
"Voorbeeld string"
'Voorbeeldreeks'
```

- **Scalaire blokinhoud**: Scalaire inhoud kan in bloknotatie worden geschreven door het volgende te gebruiken:
  - **|**: All live breaks are significant.
  - **>**: Each line break is folded to space. It removes the leading whitespace for each line.

```jaml
gegevens: |
YAML
(YAML is geen opmaaktaal)
is een taal voor gegevensserialisatie
```

```jaml
gegevens: ?
YAML (YAML is geen opmaaktaal)
is een taal voor gegevensserialisatie
```

- **Meerdere documenten**: meerdere documenten worden gescheiden door drie koppeltekens (---) in een enkele stroom. Koppeltekens geven het begin van het document aan. Koppeltekens worden ook gebruikt om richtlijnen te scheiden van documentinhoud. Het einde van het document wordt aangegeven met drie puntjes (...).

```jaml
  ---
Document 1
  ---
Document 2
...
```

- **Type**: Om het type waarde te specificeren, worden dubbele uitroeptekens (!!) gebruikt.

```jaml
a: !!float 123
b: !!str 123
```

- **Tag**: om een tag aan een notitie toe te wijzen, wordt een ampersand (&) gebruikt en om naar dat knooppunt te verwijzen, wordt een asterisk (*) gebruikt.

```jaml
naam: John Smith
factureren aan: &id01
straat: |
123 Tornado Alley
Suite 16
stad: East Centreville
staat: KS

verzenden naar: *id01
```

- **Richtlijnen**: YAML-documenten kunnen worden voorafgegaan door richtlijnen in een stream. Richtlijnen beginnen met een procentteken (%) gevolgd door de naam en vervolgens de parameters gescheiden door spaties.

```jaml
%YAML 1.2
  ---
Documentinhoud
```
## Voorbeeld YAML-bestand
Hier ziet u een **docker yaml-bestandsvoorbeeld** hieronder:

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML versus JSON
Kortom, zowel JSON als YAML zijn ontwikkeld om een door mensen leesbaar formaat voor gegevensuitwisseling te bieden. De YAML wordt gerealiseerd als een superset van het JSON-formaat. Het betekent dat we JSON kunnen ontleden met behulp van een YAML-parser. Hoewel de praktische implementatie van deze theorie weinig lastig is. Daarom worden hieronder enkele basisverschillen tussen YAML en JSON gegeven:

|YAML| JSON|
---|---|
|Complex en tijdrovend proces voor het ontleden van geserialiseerde gegevens |Snel en eenvoudig JSON-geserialiseerde gegevens ontleden met zijn eenvoudiger ontwerp|
|Minder steun van de gemeenschap| Grotere community-ondersteuning en populariteit|
|Ondersteunt opmerkingen| Ondersteunt geen reacties|
|Mogelijkheid om referentie van andere data-objecten te gebruiken| Onmogelijk om complexe structuren te serialiseren met objectreferenties|
|Hiërarchie wordt aangegeven met dubbele spatietekens. Tabtekens zijn niet toegestaan|Objecten en arrays worden aangegeven tussen accolades en haakjes.|
|Aanhalingstekens voor tekenreeksen zijn optioneel, maar het ondersteunt enkele en dubbele aanhalingstekens.|Tekenreeksen moeten tussen dubbele aanhalingstekens staan.|
|Rootknooppunt kan elk van de geldige gegevenstypen zijn|Rootknooppunt moet een array of een object zijn.|


## Referenties ##

- [YAML - Wikipedia](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)

