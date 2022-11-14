{
  "date" : "2019-10-11",
  "keywords": [ "pdb file", "pdb", "extension", "format", "What is a pdb file", "pdb file format", "PDB metadata" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo PDB: un archivo de base de datos del programa",
  "description":"Obtenga información sobre el formato de archivo PDB y las API que pueden crear y abrir archivos PDB",
  "linktitle" : "PDB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## ¿Qué es un archivo PDB?

Un archivo con extensión .pdb es un archivo de base de datos de programa que contiene información de depuración para un ejecutable compilado (EXE/DLL). Los compiladores de Microsoft generan archivos PDB cuando un programa de aplicación se compila en modo de depuración. La presencia de un archivo PDB puede ayudar en la ingeniería inversa de un ejecutable, ya que contiene información importante sobre todos los símbolos de los módulos. Es por esta razón que estos archivos se mantienen separados del ejecutable final. La [API DgbHelp] de Microsoft (https://docs.microsoft.com/en-us/windows/win32/debug/dbghelp-functions) puede abrir un archivo PDB para obtener información como públicos y exportaciones, símbolos globales, símbolos locales, escriba datos, archivos fuente y números de línea.

## Formato de archivo PDB

PDB es el formato de archivo propietario de Microsoft y aún no se ha documentado oficialmente en ninguna parte. Sin embargo, hay una documentación inicial disponible [aquí](https://github.com/Microsoft/microsoft-pdb) y se puede consultar.

### Flujos de PDB

Los archivos PDB constan de varias secuencias en las que cada secuencia actúa como un archivo individual virtual y contiene información. Los escritores de archivos PDB pueden escribir en estos archivos y el archivo se finaliza solo después de que se emite una confirmación explícita. Un compilador puede seguir escribiendo en un archivo PDB pero confirmar solo si todo el código de usuario se compila correctamente. Un archivo PDB consta de los siguientes flujos:

|Stream No. |Contenidos |Descripción breve|
---|---|---|
|1| Pdb (encabezado) |Información de la versión e información para conectar este PDB al EXE|
|2| Tpi (Administrador de tipos) |Todos los tipos usados en el ejecutable.|
|3| Dbi (Información de depuración) |Contiene contribuciones de la sección y lista de 'Mods'|
|4| NombreMapa| Contiene una tabla de cadenas hash |
|4-(n+4)| n Mod's (información del módulo)| Cada flujo Mod contiene símbolos y números de línea para un compilando |
|n+4| Hash de símbolo global| Un índice que permite buscar en símbolos globales por nombre|
|n+5| Hash de símbolo público | Un índice que permite buscar en símbolos públicos por direcciones|
|n+6| Registros de símbolos| Registros de símbolos reales de símbolos globales y públicos |
|n+7| Tipo hash| Hash utilizado por el flujo TPI.|

Cada secuencia en un archivo PDB se compone de varias páginas que no necesariamente están numeradas consecutivamente.

### Encabezado PDB

Un archivo PDB comienza con un encabezado que consiste en una firma para identificar y validar el formato específico. La longitud de la firma depende del formato PDB. El encabezado puede ser más largo que una sola página.

### Metadatos PDB
Los metadatos de PDB son responsables de reconocer todos los flujos de componentes, brindando la longitud y la secuencia de páginas para cada flujo. Las órdenes se dan a los flujos de forma consecutiva; comenzando con 0. También hay una secuencia raíz desordenada, que contiene algunos de los metadatos.

## Referencias
* [PDB - Wikipedia](https://en.wikipedia.org/wiki/Program_database)
* [Microsoft PDB](https://github.com/Microsoft/microsoft-pdb)

