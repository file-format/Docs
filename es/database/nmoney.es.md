{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga más información sobre el formato de archivo NMONEY y las API que pueden crear y abrir archivos NMONEY.",
  "title" :"Archivo NMONEY - Formato de archivo de cuenta Denaro",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## ¿Qué es un archivo NMONEY?

Un archivo NMONEY es un archivo de base de datos de almacenamiento de datos financieros que contiene un historial de transacciones financieras. Fue desarrollado por Nickvision y se utilizó en el software Nickvision Denaro, que es una aplicación de software de finanzas personales. Los datos almacenados dentro de un archivo NOMONEY incluyen información de transacciones de crédito y débito de una cuenta.

Los archivos NOMONEY se pueden abrir con la aplicación [Github](https://github.com/NickvisionApps/Denaro).

## Acerca del software Denaro

Denaro fue desarrollado inicialmente por [Nickvision](https://nickvision.org/) como un producto que luego se convirtió en una aplicación de software de código abierto alojada en [Github](https://github.com/NickvisionApps/Denaro) . Desde entonces, la aplicación se ha modificado y actualizado únicamente en Github. La aplicación está desarrollada en C# en la interfaz de usuario de Windows con el SDK de aplicaciones de Windows (WinUI 3 en este momento).

### Funciones ofrecidas por Denaro

* Administre varias cuentas simultáneamente con su interfaz de pestañas más popular y familiar
* Filtrar transacciones por tipo, grupo o fecha
* Repetir transacciones como facturas que ocurren todos los meses.
* Transferir dinero de una cuenta a otra
* Exporte los datos de una cuenta como un archivo CSV e importe un archivo CSV, OFX o QIF para agregar transacciones a una cuenta

## Formato de archivo Denaro - Más información

Los archivos Denaro se guardan en el disco en formato de archivo binario. Los datos financieros se almacenan como un archivo de base de datos en formato de archivo **.SQLITE3**. SQLITE es un archivo de base de datos SQL liviano creado con el software SQLite. Proporciona un motor de base de datos autónomo que es capaz de proporcionar una base de datos altamente confiable y con todas las funciones. Los archivos de base de datos SQLite se pueden utilizar para compartir contenidos enriquecidos entre sistemas simplemente intercambiando estos archivos a través de la red. Existen enlaces SQLite para lenguajes de programación como C, [C#](/es/programming/cs/), [C++](/es/programming/cpp/), [Java](/es/programming/java/), [PHP](/es/programming/php/), y muchos otros.

## Referencias

* [Nickvision](https://nickvision.org/)
* [NIckVision - Github](https://github.com/NickvisionApps/Denaro)

