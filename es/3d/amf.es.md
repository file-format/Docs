{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "archivo amf", "formato de archivo amf", "formato de archivo", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo AMF y las API que pueden abrir y crear archivos AMF",
  "title" :"AMF - Archivo de fabricación aditiva",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo AMF?
Un archivo AMF consta de pautas para la descripción de objetos para ser utilizados por los procesos de fabricación aditiva. Contiene una abertura<amf> etiqueta XML y termina con un</amf> elemento. Está precedido por una línea de declaración XML que especifica la versión XML y la codificación del archivo. Las declaraciones pueden incluir información sobre unidades de medida y, en ausencia de dicha información, se utilizan milímetros como unidad predeterminada.


## Formato de archivo AMF

El formato de archivo de fabricación aditiva (**AMF**) define estándares abiertos para la descripción de objetos para ser utilizados por procesos de fabricación aditiva como la impresión 3D. Los programas CAD utilizan el formato de archivo AMF al hacer uso de información como la geometría, el color y el material de los objetos. AMF es diferente al formato STL ya que el lateral no admite color, materiales, entramados ni constelaciones.

### Elementos de un archivo AMF

Los cinco elementos de nivel superior definidos con el<AMF> las etiquetas son como se detalla a continuación. La presencia de un solo elemento de objeto es imprescindible para un archivo AMF totalmente funcional.

`<object> ` - El elemento de objeto define un volumen o volúmenes de material, cada uno de los cuales está asociado con un ID de material para imprimir. Al menos un elemento de objeto debe estar presente en el archivo. Los objetos adicionales son opcionales.

`<material> `: el elemento de material opcional define uno o más materiales para imprimir con un ID de material asociado. Si no se incluye ningún elemento de material, se asume un solo material predeterminado.

`<texture> `: el elemento de textura opcional define una o más imágenes o texturas para el mapeo de color o textura, cada una con una ID de textura asociada.

`<constellation> ` - El elemento de constelación opcional combina jerárquicamente objetos y otras constelaciones en un patrón relativo para la impresión.

`<metadata> `: el elemento de metadatos opcional especifica información adicional sobre los objetos y elementos contenidos en el archivo.

## Ejemplo de AMF

El siguiente es un ejemplo de archivo AMF que se puede copiar a un archivo [texto](/es/word-processing/txt/) y guardar como archivo comprimido [zip](/es/compression/zip/) para abrirlo.
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
## Referencias

* [AMF - Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [Especificaciones AMF en ISO](https://www.iso.org/standard/67472.html)

