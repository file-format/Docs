{
  "date" : "2021-05-03",
  "keywords" :[ "SDF", "archivo sdf","qué es un archivo sdf","cómo abrir un archivo sdf", "extensión", "archivo", "formato de archivo sdf", "Tipo de archivo de base de datos", "Formato de archivo de base de datos ", "Archivos de base de datos" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga más información sobre el formato de archivo SDF y las API que pueden crear y abrir archivos SDF",
  "title" :"SDF - Archivo de base de datos compacto de SQL Server",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-05-03"
}

## ¿Qué es un archivo SDF?
Un archivo con extensión .sdf contiene la base de datos Microsoft SQL Server Compact (SQL CE), que también se conoce como base de datos relacional compacta; producido por Microsoft para las aplicaciones hechas para dispositivos móviles y computadoras de escritorio. Admite sistemas operativos de 32 y 64 bits y el contenido completo de la base de datos se incluye en un solo archivo SDF y puede ocupar más de 4 GB de espacio en disco. Por motivos de seguridad, un archivo .sdf se puede cifrar con un cifrado de 128 bits. El tiempo de ejecución de SQL CE establece el acceso multiusuario paralelo al archivo .sdf. El archivo SDF se puede copiar a través de **QuickOnce** o simplemente se puede copiar al destino para la implementación del sistema.

## Formato de archivo SDF
Un archivo SDF contiene una base de datos que generalmente se denomina base de datos relacional compacta. Un archivo SDF contiene toda la información relacionada con la base de datos y SQL Server Compact es un motor de base de datos ligero y gratuito que se utiliza para administrar los archivos .sdf. El tamaño del archivo .sdf no debe exceder el límite de 4 GB de tamaño. Los archivos SDF no almacenan información sobre procedimientos almacenados, disparadores o vistas. Las aplicaciones que usan una base de datos SQL CE no necesitan especificar la ruta a un archivo SDF en la cadena de conexión ADO.NET, en su lugar, se puede mencionar como |DataDirectory|\database_name.sdf, definiendo el directorio de datos que se define en el manifiesto de ensamblado para la aplicación.
La convención de nomenclatura .sdf es opcional y se puede usar cualquier extensión para guardar el archivo. Configurar una contraseña para el archivo de la base de datos es un paso opcional. Para comprimir o reparar la base de datos se debe guardar el archivo con la opción de **base de datos compactada/reparada**.

## Referencias

* [SQL Server Compact - Wikipedia](https://en.wikipedia.org/wiki/SQL_Server_Compact)
* [Uso de SQL Server Compact para aplicaciones web ASP.NET](https://docs.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


