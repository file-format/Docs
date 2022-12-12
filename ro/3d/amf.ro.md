{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "fișier amf", "format fișier amf", "format fișier", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier AMF și despre API-urile care pot deschide și crea fișiere AMF.",
  "title" :"AMF – Fișier de fabricație aditivă",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier AMF?
Un fișier AMF constă în linii directoare pentru descrierea obiectelor pentru a fi utilizat de procesele de fabricație aditivă. Conține o deschidere<amf> Eticheta XML și se termină cu a</amf> element. Acesta este precedat de o linie de declarație XML care specifică versiunea XML și codificarea fișierului. Declarațiile pot include informații despre unitățile de măsură și, în absența acestor informații, milimetrii sunt utilizați ca unitate implicită.


## Format de fișier AMF

Formatul de fișier de fabricație aditivă (**AMF**) definește standarde deschise pentru descrierea obiectelor pentru a fi utilizate de procesele de fabricație aditivă, cum ar fi imprimarea 3D. Programele CAD folosesc formatul de fișier AMF utilizând informații precum geometria, culoarea și materialul obiectelor. AMF este diferit de formatul STL, deoarece partea laterală nu acceptă culoare, materiale, zăbrele și constelații.

### Elementele unui fișier AMF

Cele cinci elemente de nivel superior definite cu<AMF> etichetele sunt detaliate mai jos. Prezența unui singur element obiect este obligatorie pentru un fișier AMF complet funcțional.

`<object> ` - Elementul obiect definește un volum sau volume de material, fiecare dintre acestea fiind asociat cu un ID de material pentru imprimare. Cel puțin un element obiect trebuie să fie prezent în fișier. Obiectele suplimentare sunt opționale.

`<material> ` - Elementul material opțional definește unul sau mai multe materiale pentru imprimare cu un ID de material asociat. Dacă nu este inclus niciun element material, se presupune un singur material implicit.

`<texture> ` - Elementul opțional de textură definește una sau mai multe imagini sau texturi pentru maparea culorilor sau a texturii, fiecare cu un ID de textură asociat.

`<constellation> ` - Elementul opțional de constelație combină ierarhic obiecte și alte constelații într-un model relativ pentru imprimare.

`<metadata> ` - Elementul de metadate opțional specifică informații suplimentare despre obiectul(ele) și elementele conținute în fișier.

## Exemplu AMF

Următorul este un exemplu de fișier AMF care poate fi copiat într-un fișier [text](/ro/word-processing/txt/) și salvat ca fișier comprimat [zip](/ro/compression/zip/) pentru deschidere.
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
## Referințe

* [AMF - Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [Specificații AMF pe ISO](https://www.iso.org/standard/67472.html)

