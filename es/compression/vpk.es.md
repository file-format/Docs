{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo VPK: formato de archivo del paquete de aplicaciones de PlayStation Vita",
  "description":"Obtenga información sobre el formato de archivo VPK y las API que pueden crear y abrir archivos VPK",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-01"
}

## ¿Qué es un archivo VPK?

Un archivo con extensión .vpk es un archivo de paquete de almacenamiento comprimido que se utiliza para instalar aplicaciones de terceros en la consola de juegos Sony PlayStation Vita. Estos archivos se pueden instalar solo en jailbreak Vita PlayStation de HENkaku que permitió que PS Vita y PSTV usaran contenido personalizado creado por el usuario. Un archivo VPK contiene todos los contenidos que componen el juego, incluidas imágenes como archivos [PNG](/es/image/png/), archivos de configuración como [.bin](/es/disc-and-media/bin/) y cualquier configuración en formato de archivo [XML](/es/web/xml/).

## Formato de archivo VPK

Los archivos VPK se guardan en el disco como archivos estándar comprimidos [ZIP](/es/compression/zip/). Estos pueden contener varias carpetas y otros archivos asociados para que las aplicaciones de terceros se instalen en Vita Gaming Console. Para ver el contenido del archivo del paquete VPK, cambie el nombre de su extensión de .vpu a .zip y extraiga el contenido utilizando utilidades de descompresión estándar como WinZip o WinRAR.

Valvesoftware tiene información detallada sobre el [formato de archivo VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format) que se puede consultar desde la perspectiva del desarrollador.

## ¿Cómo instalar archivos VPK?

Los archivos VPK se pueden instalar desde la utilidad de línea de comandos VPK.exe. En el sistema operativo Windows, los archivos se pueden colocar en el archivo vpk.exe, que devuelve un \*.vpk que contiene todos los archivos empaquetados. Alternativamente, la herramienta de línea de comando se puede usar de la siguiente manera.

### Crear VPK y agregar archivos

```
vpk <dirname>
```

### Extraer archivos VPK

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## Visor de VPK

* [Visor de VRF VPK](https://github.com/SteamDatabase/ValveResourceFormat)

## Referencias

* [Formato de archivo VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [Archivos VPK](https://developer.valvesoftware.com/wiki/VPK)

