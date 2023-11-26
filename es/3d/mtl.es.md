{
"fecha": "2023-10-11",
   "keywords":[
"mtl",
"archivo mtl",
"archivo de biblioteca de plantilla de material mtl obj",
"cómo abrir un archivo mtl",
"archivo",
"extensión de archivo mtl",
"extensión",
"archivo"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de archivo MTL: archivo de biblioteca de plantillas de materiales OBJ",
   "description":"Obtenga más información sobre el formato de archivo de la biblioteca de plantillas de materiales MTL OBJ y las API que pueden crear y abrir archivos MTL.",
"linktitle":"MTL",
   "menu":{
      "docs":{
         "identifier":"3d-mtl",
"parent": "3d"
}
},
"último mod": "2023-10-11"
}

## ¿Qué es un archivo MTL?

El archivo MTL, abreviatura de **Biblioteca de plantillas de materiales**, es un formato de archivo complementario que se utiliza en modelado y gráficos por computadora en 3D. A menudo se asocia con el **formato de archivo Wavefront OBJ**, que es un formato común para almacenar modelos 3D y sus materiales y texturas asociados.

## Biblioteca de plantillas de materiales

Aquí encontrará información importante sobre los archivos MTL:

1. **Definiciones de materiales**: el archivo ".mtl" contiene definiciones de materiales que se aplican a objetos 3D en el archivo OBJ correspondiente. Cada definición de material especifica varias propiedades, como color, brillo, transparencia y mapas de textura.
    





2. **Formato basado en texto**: los archivos ".mtl" suelen ser archivos de texto sin formato, lo que significa que se pueden editar fácilmente con un editor de texto. Cada definición de material consta de un conjunto de declaraciones y estas declaraciones definen los atributos del material.
    





3. **Mapeo de texturas**: Una de las funciones esenciales de un archivo ".mtl" es definir cómo se asignan las texturas (archivos de imagen) a las superficies del modelo 3D. Especifica la ruta del archivo de textura y cómo se debe ajustar o aplicar al modelo.
    





4. **Ejemplos de declaraciones MTL**: A continuación se muestran algunos ejemplos de declaraciones que puede encontrar en un archivo ".mtl":
    





- `newmtl MaterialName`: define un nuevo material con el nombre "MaterialName".
- `Ka rgb`: Color ambiental del material, especificado en valores RGB.
- `Kd rgb`: Color difuso del material, especificado en valores RGB.
- `Ks rgb`: Color especular del material, especificado en valores RGB.
- `Valor Ns`: Brillo o exponente especular del material.
- `map_Kd Texturefile.jpg`: especifica el mapa de textura difusa para el material.
5. **Múltiples materiales**: un archivo OBJ puede hacer referencia a varios materiales y cada material se define dentro del archivo ".mtl". Esto permite modelos 3D complejos con diferentes materiales aplicados a diferentes piezas.
    





6. **Compatibilidad**: los archivos ".mtl" son ampliamente compatibles con el software de modelado 3D y los motores de renderizado, lo que permite transferir modelos 3D y sus materiales entre diferentes aplicaciones de software.

## ¿Cómo abrir un archivo MTL?

Los archivos MTL son archivos basados en texto, por lo que se pueden abrir con cualquier editor de texto, incluido

- Bloc de notas (Windows)
- Bloc de notas++ (Windows)
- Código de estudio visual
- Texto sublime
- Átomo
- Edición de texto (macOS)

Los programas que abren o hacen referencia a archivos MTL incluyen

-Adobe Photoshop 2023
- Autodesk Maya 2023
-MallaLab
- guepardo3D

**Subtipo:** Archivos de imágenes 3D

## Referencias
* [Archivo Wavefront .obj](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

