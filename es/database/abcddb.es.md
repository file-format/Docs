{
  "date" : "2023-01-09",
  "keywords" :[ "ABCDDB", "qué es un archivo ABCDDB", "extensión", "archivo", "formato de archivo", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "Archivos de base de datos" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo ABCDDB y las API que pueden crear y abrir archivos ABCDDB",
  "title" :"Formato de archivo ABCDDB - Archivo de base de datos de la lista de contactos de la libreta de direcciones de Apple",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## ¿Qué es un archivo ABCDDB?

El archivo con extensión **.ABCDDB** significa base de datos de la lista de contactos de la libreta de direcciones de Apple. Pertenece a la aplicación **Libreta de direcciones**, también conocida comúnmente como **Contactos**. Es una aplicación integrada e incluida con los sistemas operativos iOS y macOS. La aplicación de contactos permite a los usuarios guardar y organizar información relacionada con sus contactos, incluidos individuos, empresas y organizaciones. Esta aplicación permite a los usuarios realizar un seguimiento de detalles como nombres, direcciones, números de teléfono y direcciones de correo electrónico, así como clasificar sus contactos en grupos.

## Relación con SQLite y ruta típica

La libreta de direcciones de Apple (también conocida como Contactos) almacena información de contacto como vCards en la carpeta de metadatos. **El archivo _ABCDDB_ es en realidad _archivo de datos SQLite 3_**.

SQLite es un popular sistema de gestión de bases de datos que está diseñado para ser ligero y autónomo. Se utiliza en muchos tipos diferentes de software y dispositivos. SQLite es un tipo de RDBMS, lo que significa que almacena datos en tablas que están relacionadas entre sí a través de claves. Puede manejar una variedad de tipos de datos, incluidos números enteros, números de coma flotante, cadenas y datos binarios. Además, SQLite admite transacciones, lo que permite a los usuarios realizar múltiples operaciones de base de datos juntas como una sola unidad de trabajo.

El archivo con la extensión ABCDDB generalmente se almacena aquí

`~/Library/Application Support/AddressBook/AddressBook-v22.abcddb`

## Reparar la base de datos de contactos corrupta

Primero realice la copia de seguridad antes de intentar hacer esto. Entonces por favor navegue a

`~/Biblioteca/Soporte de aplicaciones/Libreta de direcciones`

En ese directorio, encontrará tres archivos, incluido el que tiene la extensión .abcddb

- `libreta de direcciones-v22.abcddb`
- `libreta de direcciones-v22.abcddb-wal`
- `libreta de direcciones-v22.abcddb-shm`

Elimine todos estos archivos y vuelva a abrir los Contactos, comenzará a funcionar nuevamente.

## Restaurar la base de datos de la libreta de direcciones desde la copia de seguridad

Supongamos que los contactos de la base de datos de su libreta de direcciones están almacenados en `addressbook-v22.abcddb`

- Primero haga una copia de seguridad de los datos de su libreta de direcciones y cierre todas las aplicaciones.
- Mueva su archivo de base de datos al subdirectorio `~/Library/Application Support/AddressBook`
- Inicie **Address Book.app**.

## Exportar datos de archivos ABCDDB a Microsoft Access

Dado que el archivo es un archivo de datos SQLite 3, puede exportar los datos dentro del archivo abcddb a Microsoft Access usando el conector ODBC.

El conector SQLite ODBC es una biblioteca de software y un controlador que permite que las aplicaciones que admiten la interfaz ODBC se conecten a una base de datos SQLite. Incluye una biblioteca que define la interfaz ODBC y un controlador que traduce esta interfaz en llamadas a la API de SQLite. Para utilizar el conector ODBC de SQLite, primero debe instalarlo y luego configurar una fuente de datos ODBC en su computadora. Después de completar estos pasos, cualquier aplicación que esté equipada con soporte ODBC podrá conectarse a la fuente de datos y recuperar datos de la base de datos SQLite.

## Referencias
* [Corregir la base de datos de contactos dañada] (https://discussions.apple.com/docs/DOC-10581)
* [Base de datos de contactos para Mac](https://nitroreward.weebly.com/blog/contact-database-for-mac)
* [¿Cómo puedo abrir o exportar un archivo abcddb en Windows 7 Excel?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file- en-windows-7-excel)

