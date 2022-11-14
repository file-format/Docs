{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "amf-bestand", "amf-bestandsindeling", "bestandsindeling", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over AMF-bestandsindelingen en API's die AMF-bestanden kunnen openen en maken.",
  "title" :"AMF - Additive Manufacturing File",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een AMF-bestand?
Een AMF-bestand bestaat uit richtlijnen voor objectbeschrijving om te worden gebruikt door Additive Manufacturing-processen. Het bevat een opening<amf> XML-tag en eindigt met a</amf> element. Dit wordt voorafgegaan door een XML-declaratieregel die de XML-versie en codering van het bestand specificeert. De declaraties kunnen informatie over meeteenheden bevatten en, bij gebrek aan dergelijke informatie, worden millimeters als standaardeenheid gebruikt.


## AMF-bestandsindeling

Additive Manufacturing-bestandsindeling (**AMF**) definieert open standaarden voor objectbeschrijving om te worden gebruikt door additive manufacturing-processen zoals 3D-printen. CAD-programma's gebruiken het AMF-bestandsformaat door gebruik te maken van de informatie zoals geometrie, kleur en materiaal van de objecten. AMF is anders dan het STL-formaat omdat de laterale kleur, materialen, roosters en sterrenbeelden niet ondersteunt.

### Elementen van een AMF-bestand

De vijf elementen op het hoogste niveau gedefinieerd met de<AMF> tags zijn zoals hieronder beschreven. De aanwezigheid van een enkel objectelement is een must voor een volledig functioneel AMF-bestand.

`<object> ` - Het objectelement definieert een volume of volumes materiaal, die elk zijn gekoppeld aan een materiaal-ID voor afdrukken. Er moet minimaal één objectelement in het bestand aanwezig zijn. Extra objecten zijn optioneel.

`<material> ` - Het optionele materiaalelement definieert een of meer materialen voor afdrukken met een bijbehorende materiaal-ID. Als er geen materieel element is opgenomen, wordt uitgegaan van één standaardmateriaal.

`<texture> ` - Het optionele textuurelement definieert een of meer afbeeldingen of texturen voor kleur- of textuurmapping, elk met een bijbehorend textuur-ID.

`<constellation> ` - Het optionele constellatie-element combineert hiërarchisch objecten en andere constellaties tot een relatief patroon voor afdrukken.

`<metadata> ` - Het optionele metadata-element specificeert aanvullende informatie over de object(en) en elementen in het bestand.

## AMF-voorbeeld

Hieronder volgt een voorbeeld van een AMF-bestand dat kan worden gekopieerd naar een [text](/nl/word-processing/txt/)-bestand en kan worden opgeslagen als gecomprimeerd [zip](/nl/compression/zip/)-bestand om te openen.
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## Referenties

* [AMF - Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [AMF-specificaties op ISO](https://www.iso.org/standard/67472.html)

