{
  "date" : "2021-01-21",
  "keywords" :[ "archivo ai", "formato de archivo ai", "qué es un archivo ai", "archivo", "ejemplo ai", "extensión de archivo ai", "extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AI - Archivo de ilustraciones de Adobe Illustrator",
  "description":"Obtenga información sobre el formato de archivo AI y las API que pueden crear y abrir archivos AI",
  "linktitle" : "AI",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-01-21"
}

## ¿Qué es un archivo AI?

Un archivo con una extensión .ai es un archivo de ilustraciones de Adobe Illustrator que contiene gráficos vectoriales en una sola página. utiliza puntos para crear rutas para mostrar los datos de la imagen, lo que evita que se pierda la calidad de la imagen si se amplía. El formato de archivo AI se basa en el formato de archivo PGF, que es similar a los archivos AI. El formato AI encuentra su uso principal para logotipos y medios impresos, y sus versiones iniciales se consideraron similares a las de los archivos [EPS](/es/image/eps/). Los archivos AI se pueden abrir con las herramientas Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro y CorelDraw Graphics.

## Formato de archivo AI

AI es el formato de archivo patentado de Adobe Illustrator y utiliza un enfoque de doble ruta similar a PGF para guardar archivos compatibles con EPS. Las [especificaciones del formato de archivo de Adobe Illustrator](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) proporcionan una descripción detallada referencia del desarrollador para detalles internos de este formato de archivo. Todos los documentos (archivos) creados por Adobe Illustrator son documentos de lenguaje PostScript y tienen dos partes principales que se ajustan a las convenciones de estructuración de documentos: un 'prólogo' y un 'guión'.

### Prólogo

La sección de prólogo encapsula la información requerida para la interpretación del archivo. Un ejemplo sería el cuadro delimitador que contiene todas las marcas en la página. También contiene información de recursos, como fuentes y definiciones de procedimientos. Estos recursos se agrupan lógicamente en conjuntos llamados procsets y contienen métodos explícitos para inicializar y finalizar sus procedimientos.

### Guion

Los elementos gráficos en la página son descritos por el guión. Un script contiene referencias a los operadores y procedimientos en el prólogo, junto con operandos y datos. Las tres secciones lógicas de un script incluyen:

* Secuencia de configuración - que inicializa y activa los recursos definidos en el prólogo
* Secuencia de operadores descriptivos
* Tráiler que desactiva recursos

Los operadores en el script son secuencias de elementos gráficos escritos en el lenguaje definido por procsets en el prólogo. Estas secuencias consisten en colecciones de elementos de datos, definiciones de atributos gráficos y llamadas a los procedimientos definidos en los procsets.

### Etiquetas de objeto

Las etiquetas de objeto se utilizan para adjuntar información personalizada a un objeto de arte de Adobe Illustrator. Las etiquetas consisten en:

* Identificador de etiqueta
* Tipo de etiqueta
* Datos

## Referencias
* [Especificaciones del formato de archivo de Adobe Illustrator](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)
* [Formato de archivo AI de PaintShopPro](https://www.paintshoppro.com/en/pages/ai-file/)

