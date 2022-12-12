{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "amf fájl", "amf fájlformátum", "fájlformátum", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ az AMF fájlformátumról és az API-król, amelyek képesek megnyitni és létrehozni AMF fájlokat.",
  "title" :"AMF - Additív gyártási fájl",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az AMF fájl?
Az AMF-fájl az additív gyártási folyamatok által használható objektumok leírására vonatkozó irányelveket tartalmazza. Nyílást tartalmaz<amf> XML címke és a végződik</amf> elem. Ezt egy XML deklarációs sor előzi meg, amely megadja a fájl XML verzióját és kódolását. A nyilatkozatok tartalmazhatnak mértékegységre vonatkozó információkat, és ilyen információ hiányában a millimétert használják alapértelmezett mértékegységként.


## AMF fájlformátum

Az Additive Manufacturing fájlformátum (**AMF**) nyílt szabványokat határoz meg az objektumok leírására, hogy azokat az additív gyártási folyamatok, például a 3D nyomtatás során is felhasználják. A CAD programok az AMF fájlformátumot használják az olyan információk felhasználásával, mint az objektumok geometriája, színe és anyaga. Az AMF eltér az STL formátumtól, mivel az oldalsó nem támogatja a színeket, az anyagokat, a rácsokat és a csillagképeket.

### Az AMF fájl elemei

Az öt legfelső szintű elem, amelyet a<AMF> címkék az alábbiak szerint vannak részletezve. Egyetlen objektumelem jelenléte elengedhetetlen egy teljesen működőképes AMF-fájlhoz.

`<object> ` - Az objektum elem egy vagy több anyagmennyiséget határoz meg, amelyek mindegyike egy anyagazonosítóval van társítva a nyomtatáshoz. Legalább egy objektum elemnek jelen kell lennie a fájlban. A további objektumok nem kötelezőek.

`<material> ` - Az opcionális anyagelem egy vagy több nyomtatandó anyagot határoz meg egy társított anyagazonosítóval. Ha nem tartalmaz anyagelemet, a rendszer egyetlen alapértelmezett anyagot feltételez.

`<texture> ` - Az opcionális textúraelem egy vagy több képet vagy textúrát határoz meg a szín- vagy textúra-leképezéshez, mindegyikhez hozzárendelt textúraazonosító tartozik.

`<constellation> ` - Az opcionális konstellációs elem hierarchikusan egyesíti az objektumokat és más konstellációkat egy relatív mintává a nyomtatáshoz.

`<metadata> ` - Az opcionális metaadat elem további információkat ad meg a fájlban található objektum(ok)ról és elemekről.

## AMF példa

Az alábbiakban egy példa látható az AMF fájlra, amely egy [text](/hu/word-processing/txt/) fájlba másolható, és megnyitáshoz tömörített [zip](/hu/compression/zip/) fájlként menthető.
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
## Hivatkozások

* [AMF – Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [AMF-specifikációk az ISO-n](https://www.iso.org/standard/67472.html)

