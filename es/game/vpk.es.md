{
  "date" : "2023-01-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga más información sobre el formato de archivo VPK de Unreal Static Meshes y las API que pueden crear y abrir archivos VPK",
  "title" :"Archivo VPK - Archivo de mallas estáticas irreales",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "identifier":"game-vpk",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-16"
}

## ¿Qué es un archivo VPK?

Un archivo .vpk es un formato de archivo utilizado por **Source Engine**, un motor de juegos desarrollado por Valve Corporation. Los archivos VPK se usan para empaquetar el contenido del juego, como modelos, texturas y sonidos, y se usan comúnmente en juegos como Team Fortress 2, Left 4 Dead y Counter-Strike: Global Offensive. Los archivos se pueden abrir y extraer utilizando una variedad de herramientas, como GCFScape y VPK Tool.

## Formato de archivo VPK: más información

Los archivos VPK se almacenan en el disco como archivos binarios. Un solo archivo vpk puede ser parte de un paquete VPK o puede actuar como un archivo VPK sin procesar independiente. La información que se puede almacenar dentro de un archivo VPK incluye mapas, materiales, contenido del juego y escenas de coreografía.

### ¿Cómo crear un archivo VPK?

Hay varias formas de crear un archivo .vpk, según las herramientas disponibles.

1. `Uso de la herramienta VPK:` Esta es una herramienta de línea de comandos que se puede usar para crear y extraer archivos VPK. Se puede crear un archivo VPK usando el siguiente comando:
```
"vpk.exe -M <directory> <output_file.vpk>"
```
Esto creará un archivo VPK desde el directorio especificado y lo guardará como el archivo de salida especificado.

1. `Uso del editor Hammer:` El editor Hammer es una herramienta incluida con Source SDK que se puede usar para crear y editar niveles para juegos que usan el motor Source. También incluye la capacidad de crear archivos VPK, haciendo clic con el botón derecho en una carpeta en la pestaña "Sistema de archivos" y seleccionando "Crear VPK".

1. `Uso del creador de VPK de Valve:` Esta es una herramienta desarrollada por Valve que se usa para empaquetar y distribuir contenido de juegos. Esta herramienta se puede utilizar para crear archivos VPK y también es la herramienta oficial para crear archivos VPK.

## Referencias

* [Software de válvula](https://www.valvesoftware.com/en/)
* [Recursos para desarrolladores de VPK](https://developer.valvesoftware.com/wiki/GCF)

