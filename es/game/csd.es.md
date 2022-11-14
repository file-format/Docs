{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga más información sobre las API y el formato de archivo de copia de seguridad de datos de juegos CSD Steam",
  "title" :"Formato de archivo CSD: archivo de copia de seguridad de datos de juegos de Steam",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
      "identifier": "game-csd",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## ¿Qué es un archivo CSD?

Un archivo CSD es un archivo de copia de seguridad del juego generado por el servicio de juegos **Steam** que permite a los usuarios descargar y administrar juegos de **Valve**. Contiene los datos de respaldo relacionados con los juegos que se pueden usar para restaurar un juego eliminado. Steam solo puede restaurar el juego desde un archivo CSD si el juego se descargó, instaló y parchó por completo a través de Steam. Para restaurar el juego desde un archivo CSD, use la opción de Steam → Backup and Restore Gamesteam y seleccione el archivo.

## Formato de archivo CSD: más información

La estructura interna del formato de archivo CSD no está disponible públicamente y sus especificaciones de formato de archivo no están disponibles para referencia del desarrollador. Los archivos CSD van acompañados de los archivos CSM e ISS, que también son formatos de archivo de juegos de Steam.

### ¿Dónde encontrar archivos de copia de seguridad de Steam?

Todos los archivos de copia de seguridad de Steam se pueden encontrar en las siguientes ubicaciones:

* C:\Archivos de programa (x86)\Steam\steamapps\common\<game name> \ :
* \cfg\ - Configuraciones personalizadas y scripts de configuración
* \descargas\ - Contenido personalizado para juegos multijugador
* \maps\ - Mapas personalizados que han sido instalados o descargados durante partidas multijugador
* \materials\ - Texturas y pieles personalizadas
* \SAVE\ - Partidas guardadas para un solo jugador

Sin embargo, la ubicación de los juegos creados por terceros puede ser diferente y la determina el desarrollador del juego.

### Restauración desde el archivo de copia de seguridad CSD

Instale Steam e inicie sesión en la cuenta de Steam correcta (consulte Instalación de Steam para obtener más instrucciones)
* Lanzamiento de vapor
* Haga clic en "Steam" en la esquina superior izquierda de la aplicación Steam
* Seleccione "Copia de seguridad y restauración de juegos..."
* Seleccione "Restaurar una copia de seguridad anterior"
* Busque la ubicación de los archivos de copia de seguridad del juego
* Continúe a través de las ventanas de Steam para instalar los juegos necesarios.

## Referencias

* [Uso de la función de copia de seguridad de Steam](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

