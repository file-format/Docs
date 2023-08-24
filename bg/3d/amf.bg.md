{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "amf файл", "amf файлов формат", "файлов формат", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Научете за файловия формат AMF и API, които могат да отварят и създават AMF файлове.",
  "title" :"AMF – Файл за адитивно производство",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е AMF файл?
AMF файл се състои от насоки за описание на обекти, за да се използва от процеси на адитивно производство. Съдържа отвор<amf> XML таг и завършва с a</amf> елемент. Това се предшества от ред за XML декларация, указващ XML версията и кодирането на файла. Декларациите могат да включват информация за мерните единици и, при липса на такава информация, милиметрите се използват като единица по подразбиране.


## AMF файлов формат

Файловият формат за адитивно производство (**AMF**) дефинира отворени стандарти за описание на обекти, за да бъдат използвани от процеси на адитивно производство, като 3D печат. CAD програмите използват файловия формат AMF, като използват информацията като геометрия, цвят и материал на обектите. AMF е различен от STL формата, тъй като страничният не поддържа цвят, материали, решетки и съзвездия.

### Елементи на AMF файл

Петте елемента от най-високо ниво, дефинирани с<AMF> етикетите са описани по-долу. Наличието на единичен обектен елемент е задължително за напълно функционален AMF файл.

`<object> ` – Елементът обект дефинира обем или обеми материал, всеки от които е свързан с идентификатор на материал за печат. Във файла трябва да присъства поне един обектен елемент. Допълнителните обекти не са задължителни.

`<material> ` – Незадължителният материален елемент дефинира един или повече материали за печат със свързан идентификатор на материал. Ако не е включен материален елемент, се приема единичен материал по подразбиране.

`<texture> ` – Незадължителният текстурен елемент дефинира едно или повече изображения или текстури за картографиране на цвят или текстура, всяко със свързан идентификатор на текстура.

`<constellation> ` - Незадължителният елемент на съзвездие йерархично комбинира обекти и други съзвездия в относителен модел за отпечатване.

`<metadata> ` – Незадължителният елемент на метаданни указва допълнителна информация за обекта(ите) и елементите, съдържащи се във файла.

## Пример за AMF

Следва пример за AMF файл, който може да бъде копиран в [текст](/bg/word-processing/txt/) файл и записан като компресиран [zip](/bg/compression/zip/) файл за отваряне.
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
## Препратки

* [AMF - Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [AMF спецификации на ISO](https://www.iso.org/standard/67472.html)

