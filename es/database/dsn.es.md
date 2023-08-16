{
  "date" : "2023-01-17",
  "keywords" :[ "DSN", "qué es un archivo DSN", "extensión", "archivo", "formato de archivo", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "Archivos de base de datos" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga más información sobre el formato de archivo DSN y las API que pueden crear y abrir archivos DSN",
  "title" :"Formato de archivo DSN: archivo de nombre de origen de la base de datos",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## ¿Qué es un archivo DSN?

DSN significa "Nombre de fuente de datos" y es un formato de archivo que se utiliza para almacenar información de conexión a la base de datos. Los archivos DSN generalmente se usan junto con ODBC (Open Database Connectivity) y permiten un fácil acceso a una base de datos específica al proporcionar la información necesaria para conectarse, como el nombre del servidor, el nombre de usuario y la contraseña. El archivo suele estar en texto sin formato y se puede crear y editar con un editor de texto. Se puede utilizar en varios sistemas operativos como Windows, Linux y Mac.

## ¿Cómo crear un archivo DSN?

El método para crear un archivo DSN puede variar según el sistema operativo y las herramientas disponibles. Los siguientes pasos brindan una descripción general del proceso para crear un archivo DSN en un sistema Windows.

1. Abra el Administrador de fuente de datos ODBC buscando "Fuentes de datos ODBC" en el menú de inicio.
2. Seleccione la pestaña "DSN del sistema" y haga clic en el botón "Agregar".
3. Seleccione el controlador apropiado para la base de datos a la que desea conectarse y haga clic en "Finalizar".
4. Complete la información necesaria para conectarse a la base de datos, como el nombre del servidor, el nombre de usuario y la contraseña.
5. Haga clic en "Aceptar" para guardar el archivo DSN.

Alternativamente, puede crear un archivo DSN manualmente creando un archivo de texto sin formato con la extensión .dsn e ingresando la información de conexión necesaria en el formato:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

Luego puede usar la ruta de este archivo como el DSN en su código/script para conectarse a la base de datos.

## Programas que abren archivos DSN

Un archivo DSN es un archivo de texto sin formato que almacena información utilizada para conectarse a una base de datos, como el nombre del servidor, el nombre de usuario y la contraseña. Por lo general, se usa junto con ODBC (Conectividad abierta de base de datos) para proporcionar un fácil acceso a una base de datos específica.

Para abrir y ver el contenido de un archivo DSN, puede usar cualquier editor de texto como Notepad, Sublime Text, Atom, etc. Estos programas le permitirán abrir el archivo DSN y ver la información de conexión almacenada en él.

Sin embargo, para usar el archivo DSN para conectarse a una base de datos y ejecutar operaciones como SELECCIONAR, INSERTAR, ACTUALIZAR, ELIMINAR, etc., un programa compatible con ODBC, como un lenguaje de programación como Python, Java, C# o una herramienta de administración de bases de datos como Microsoft Access , se requiere SQL Server Management Studio. Estos programas pueden utilizar la información del archivo DSN para conectarse a la base de datos y realizar la operación deseada.

## Referencias

* [¿Qué es un DSN (nombre de origen de datos)?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30-606e-2436fe26e89f)


