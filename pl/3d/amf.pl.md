{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "plik amf", "format pliku amf", "format pliku", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku AMF i interfejsy API, które mogą otwierać i tworzyć pliki AMF.",
  "title" :"AMF - plik wytwarzania przyrostowego",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik AMF?
Plik AMF zawiera wytyczne dotyczące opisu obiektów, które mają być wykorzystywane przez procesy Additive Manufacturing. Zawiera otwór<amf> znacznik XML i kończy się na a</amf> element. Jest to poprzedzone linią deklaracji XML określającą wersję XML i kodowanie pliku. Deklaracje mogą zawierać informację o jednostkach miary, aw przypadku braku takiej informacji jako jednostkę domyślną przyjmuje się milimetry.


## Format pliku AMF

Format pliku wytwarzania przyrostowego (**AMF**) definiuje otwarte standardy opisu obiektów, które można wykorzystać w procesach wytwarzania przyrostowego, takich jak drukowanie 3D. Programy CAD używają formatu pliku AMF, wykorzystując informacje, takie jak geometria, kolor i materiał obiektów. AMF różni się od formatu STL, ponieważ format boczny nie obsługuje kolorów, materiałów, krat i konstelacji.

### Elementy pliku AMF

Pięć elementów najwyższego poziomu zdefiniowanych za pomocą<AMF> tagi są wyszczególnione poniżej. Obecność pojedynczego elementu obiektowego jest niezbędna dla w pełni funkcjonalnego pliku AMF.

`<object> ` - Element obiektu definiuje objętość lub objętości materiału, z których każda jest powiązana z identyfikatorem materiału do drukowania. Plik musi zawierać co najmniej jeden element obiektu. Dodatkowe obiekty są opcjonalne.

`<material> ` - Opcjonalny element materiału definiuje jeden lub więcej materiałów do drukowania z powiązanym identyfikatorem materiału. Jeśli nie uwzględniono żadnego elementu materiału, przyjmowany jest pojedynczy materiał domyślny.

`<texture> ` - Opcjonalny element tekstury definiuje jeden lub więcej obrazów lub tekstur do mapowania kolorów lub tekstur, każdy z powiązanym identyfikatorem tekstury.

`<constellation> ` - Opcjonalny element konstelacji hierarchicznie łączy obiekty i inne konstelacje we względny wzór do drukowania.

`<metadata> ` - Opcjonalny element metadanych określa dodatkowe informacje o obiektach i elementach zawartych w pliku.

## Przykład AMF

Poniżej znajduje się przykład pliku AMF, który można skopiować do pliku [text](/pl/word-processing/txt/) i zapisać jako skompresowany plik [zip](/pl/compression/zip/) do otwarcia.
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
## Bibliografia

* [AMF – Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [Specyfikacje AMF dotyczące ISO](https://www.iso.org/standard/67472.html)

