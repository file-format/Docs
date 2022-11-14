{
  "date" : "2019-10-11",
  "keywords" :[ "archivo obj", "formato de archivo obj", "qué es un archivo obj", "archivo", "ejemplo de obj", "extensión de archivo obj","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo OBJ",
  "description":"Obtenga información sobre el formato de archivo OBJ y las API que pueden abrir y crear archivos OBJ",
  "linktitle" : "OBJ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo OBJ?

Los archivos **OBJ** son utilizados por la aplicación Advanced Visualizer de Wavefront para definir y almacenar los objetos geométricos. La transmisión hacia adelante y hacia atrás de datos geométricos es posible a través de archivos OBJ. Tanto la geometría poligonal como puntos, líneas, vértices de textura, caras y geometría de forma libre (curvas y superficies) son compatibles con el formato OBJ. Este formato no admite animación ni información relacionada con la luz y la posición de las escenas.

Un archivo OBJ suele ser un producto final del proceso de modelado 3D generado por un CAD (diseño asistido por computadora). El orden predeterminado para almacenar los vértices es en sentido contrario a las agujas del reloj, lo que evita la declaración explícita de caras normales. Aunque los archivos OBJ declaran información de escala en una línea de comentario, aún no se han declarado unidades para las coordenadas OBJ.

## Historia del formato 3D OBJ

Wavefront Technologies creó el formato de archivo OBJ para su aplicación Advanced Visualizer para almacenar objetos geométricos y datos 3D. Su versión 2.11 es reemplazada por una versión 3 recientemente documentada. El formato de archivo es abierto y ha sido implementado por otros proveedores para su aplicación de gráficos 3D. Wavefront Technologies mantuvo este formato de archivo de fuente abierta y neutral.

## Formato de archivo OBJ

En objetos 3D, codificar la geometría de la superficie es un trabajo desafiante que el formato de archivo OBJ logró muy bien. Este formato es bastante versátil ya que ofrece varias opciones para codificar la geometría de la superficie. Los siguientes son tres formatos permitidos que tienen sus propias ventajas y desventajas:

### Teselado con caras poligonales

El formato de archivo OBJ facilita al usuario la creación de mosaicos en la superficie de un modelo 3D utilizando formas geométricas simples o complejas. Para la codificación de la geometría de superficie de un modelo, un archivo almacena los vértices y la normal a cada polígono. Aunque el teselado aumenta la tosquedad del modelo, es necesario descubrir el equilibrio correcto entre el tamaño de un archivo y su calidad de impresión.

### Curva de forma libre

El formato de archivo OBJ permite que las curvas de superficie de forma libre definidas por el usuario especifiquen la geometría de la superficie de un modelo. Como las curvas de forma libre son más complejas que las caras poligonales, con pocos parámetros matemáticos, las líneas curvas se pueden definir mejor mediante curvas de forma libre. Por lo tanto, con menos datos en comparación con las teselaciones poligonales, las curvas de forma libre se utilizan para generar una codificación de alta calidad de cualquier modelo 3D sin expandir el tamaño del archivo.

### Superficies de forma libre

El formato de archivo OBJ también especifica el mosaico de la geometría de la superficie con parches de superficie de forma libre. Este tipo de parches de superficie de forma libre (NURBS) es muy adecuado para superficies sin dimensiones radiales rígidas como el cuerpo de un camión, las alas de un helicóptero o el casco de un barco. El uso de superficies de forma libre es muy ventajoso ya que son más precisos para mantener los tamaños de archivo más pequeños con mayor precisión. Estas superficies son una parte esencial de la industria aeroespacial y automotriz donde la baja precisión es implacable.

Las siguientes palabras clave están ordenadas por tipo de datos para definir la geometría de la superficie.


|Elementos|Declaraciones de cuerpo de superficie/curva de forma libre|Atributos de superficie/curva de forma libre
---|---|---|
|p|Punto|parm|Valores de parámetro|grado|Grado
|l|Línea|recorte|Bucle de recorte exterior|bmat|Matriz base
|f|Cara|agujero|Bucle de recorte interior|paso|Tamaño del paso
|curv|Curva|scrv|Curva especial|cstype|Curva o tipo de superficie
|curv2|curva 2D|sp|Punto especial|**Conectividad y Agrupación de superficies**
|navegar|Superficie|fin|Fin de declaración|con|conectar
|**Atributos de visualización/renderización**|g|Nombre del grupo
|bevel|Interpolación de bisel|shadow_obj|Proyección de sombras|s|Grupo de suavizado
|lod|Nivel de detalle|trace_obj|Trazado de rayos|mg|Grupo de fusión
|d_interp|Disolver interpolación|ctech|Técnica de aproximación de curvas|o|Nombre del objeto
|c_interp|Interpolación de color|stech|Técnica de aproximación de superficies|
|usemtl|Nombre del material|mtllib|Biblioteca de materiales|
|**Vértices geométricos**|
|v|Vértices geométricos|vn|Vértices normales|
|vt|Vértices de textura|vp|Vértices de espacio de parámetros|

### Color y textura

El archivo OBJ permite que la información de color y textura se almacene en un formato de archivo asociado llamado Biblioteca de plantillas de materiales (MTL). Los modelos geométricos multicolores se renderizan usando estos dos archivos juntos. Los archivos MTL están basados en ASCII y facilitan la representación por computadora al describir las propiedades de reflexión de la luz de una superficie utilizando el modelo de reflexión de Phong. El estándar ha sido adoptado por un gran número de proveedores de software que aprovechan su ventaja para el intercambio de materiales. El formato MTL está ligeramente desactualizado por no tener soporte en las últimas tecnologías, como mapas especulares y de paralaje.

## Referencias

* [Archivo .obj de frente de onda] (https://en.wikipedia.org/wiki/Wavefront_.obj_file)

