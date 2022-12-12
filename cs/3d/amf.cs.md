{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "soubor amf", "formát souboru amf", "formát souboru", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru AMF a rozhraních API, která mohou otevírat a vytvářet soubory AMF.",
  "title" :"AMF - Aditivní výrobní soubor",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor AMF?
Soubor AMF obsahuje pokyny pro popis objektů, které mají být použity procesy aditivní výroby. Obsahuje otvor<amf> XML tag a končí a</amf> živel. Tomu předchází řádek deklarace XML specifikující verzi XML a kódování souboru. Deklarace mohou obsahovat informace o měrných jednotkách, a pokud takové informace chybí, použijí se jako výchozí jednotky milimetry.


## Formát souboru AMF

Formát souboru Additive Manufacturing (**AMF**) definuje otevřené standardy pro popis objektů, aby mohly být využity aditivními výrobními procesy, jako je 3D tisk. CAD programy používají formát souboru AMF tím, že využívají informace, jako je geometrie, barva a materiál objektů. AMF se liší od formátu STL, protože laterální nepodporuje barvy, materiály, mřížky a konstelace.

### Prvky souboru AMF

Pět prvků nejvyšší úrovně definovaných pomocí<AMF> značky jsou popsány níže. Pro plně funkční soubor AMF je nezbytná přítomnost jednoho elementu objektu.

'<object> ` - Element object definuje objem nebo objemy materiálu, z nichž každý je spojen s ID materiálu pro tisk. V souboru musí být přítomen alespoň jeden prvek objektu. Další objekty jsou volitelné.

'<material> ` - Volitelný prvek materiálu definuje jeden nebo více materiálů pro tisk s přidruženým ID materiálu. Pokud není zahrnut žádný materiálový prvek, předpokládá se jeden výchozí materiál.

`<texture> ` - Volitelný prvek textury definuje jeden nebo více obrázků nebo textur pro mapování barev nebo textur, každý s přiřazeným ID textury.

`<constellation> ` - Volitelný prvek konstelace hierarchicky kombinuje objekty a další konstelace do relativního vzoru pro tisk.

`<metadata> ` - Volitelný prvek metadat specifikuje další informace o objektu (objektech) a prvcích obsažených v souboru.

## Příklad AMF

Následuje příklad souboru AMF, který lze zkopírovat do souboru [text](/cs/word-processing/txt/) a uložit jako komprimovaný soubor [zip](/cs/compression/zip/) pro otevření.
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
## Reference

* [AMF – Wikipedie](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [Specifikace AMF na ISO](https://www.iso.org/standard/67472.html)

