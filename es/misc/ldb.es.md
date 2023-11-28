{
"fecha": "2023-04-20",
  "keywords": [
"archivo ldb",
"¿Qué es un archivo LDB?",
"Qué información contiene LDB",
"¿Cuál es el propósito del archivo ldb?",
"extensión ldb",
"archivo",
"extensión"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de archivo LDB - Archivo de bloqueo de Microsoft Access",
  "description":"Aprende sobre el formato LDB y qué información contiene.",
"linktitle": "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb",
"parent" : "misc"
}
},
"última modificación": "2023-04-20"
}

## ¿Qué es un archivo LDB?

Un archivo LDB es un archivo de bloqueo utilizado por Microsoft Access para evitar que varios usuarios editen la misma base de datos simultáneamente. Cuando el usuario abre una base de datos de Access, Access crea un archivo LDB correspondiente en el mismo directorio que la base de datos. Este archivo contiene información sobre quién está utilizando actualmente la base de datos y qué registros están editando.

Microsoft Access crea automáticamente el archivo LDB cuando se abre la base de datos y se elimina cuando se cierra la base de datos. Es importante tener en cuenta que el archivo LDB nunca debe eliminarse manualmente porque esto puede causar problemas con la base de datos.

Si tiene problemas con la base de datos de Microsoft Access, una posible solución es intentar eliminar el archivo LDB asociado con esa base de datos. Esto liberará cualquier bloqueo que pueda impedirle acceder a la base de datos. Sin embargo, asegúrese de hacer una copia de seguridad de la base de datos antes de intentar esto, ya que eliminar el archivo LDB puede causar pérdida o corrupción de datos si se hace incorrectamente.

## Formato de archivo LDB - Más información

Un archivo LDB en Microsoft Access contiene información sobre los usuarios que actualmente acceden a la base de datos, como su nombre de usuario, nombre de computadora y hora de inicio de sesión. El archivo LDB también contiene información sobre los bloqueos que se han colocado en la base de datos, como qué registros están siendo editados por qué usuario.

Aquí hay una lista más detallada de los tipos de información que se puede encontrar en un archivo LDB:

- **Nombre de usuario**: el nombre del usuario que actualmente accede a la base de datos.
- **Nombre de la computadora**: el nombre de la computadora desde donde el usuario accede a la base de datos.
- **Hora de inicio de sesión**: la hora en que el usuario abrió la base de datos por primera vez
- **Bloqueos de registros**: información sobre qué registros están siendo editados actualmente por cada usuario
- **Bloqueos de objetos**: información sobre qué objetos de la base de datos (como tablas, formularios o informes) están siendo editados actualmente por qué usuario.
- **Información de conexión**: información sobre cómo el usuario está conectado a la base de datos (por ejemplo, si está utilizando una conexión local o de red)

Microsoft Access utiliza la información del archivo LDB para evitar que varios usuarios realicen cambios conflictivos en la misma base de datos al mismo tiempo. Cuando el usuario intenta editar un registro u objeto que ya está bloqueado por otro usuario, Microsoft Access mostrará un mensaje indicando que el objeto ya está en uso. El archivo LDB se actualiza a medida que los usuarios abren y cierran la base de datos y realizan cambios en los objetos bloqueados.

## Referencias
* [¿Qué es un archivo LDB?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)

