{
  "date" : "2021-28-05",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAR - Archivo de informes de Microsoft Access",
  "keywords" :[ "mar", "archivo mar", "formato de archivo mar", "qué es el informe de acceso", "informe de acceso", "informe de acceso de microsoft"],
  "description":"Obtenga más información sobre el formato de archivo Acess Report (MAR) que utiliza el software Microsoft Access para crear un acceso directo o un enlace a Microsoft Access Report",
  "linktitle" : "MAR",
  "menu" : {
    "docs" : {
    "identifier": "reporting-mar",
      "parent" : "reporting"
}
},
  "lastmod" : "2021-28-05"
}

## ¿Qué es el Informe de acceso (archivo MAR)? ##
Un archivo creado por Microsoft Access como acceso directo de su informe se guarda con la extensión de archivo .mar. Un **informe de Microsoft Access** ofrece una forma de formatear, ver y resumir la información en la base de datos de Microsoft Access. Estos informes le permiten dar formato a sus datos en un diseño preciso e informativo para verlos en pantalla o imprimirlos. El informe solo muestra los datos estáticos, lo que significa que no podemos modificar los datos en las tablas al ver el informe de Access. El informe muestra los datos más recientes cuando se abre.

## Formato de archivo de informe de Microsoft Access (MAR)

El formato de archivo MAR es utilizado por el software de Microsoft Access para crear un acceso directo o enlace a Microsoft Access Report, que es un objeto de base de datos que se vuelve útil cuando necesita presentar la información en su base de datos para cualquiera de los siguientes usos:

- Mostrar un resumen de datos.
- Archivar instantáneas de los datos.
- Mostrar detalles sobre registros individuales.
- Crear etiquetas.

## Informe de partes de acceso
El diseño de un informe de Access se divide en diferentes secciones que se pueden ver en la vista Diseño. La siguiente tabla explica cómo funciona cada sección y puede ayudarlo a crear informes.
| Sección | Cómo se muestra la sección cuando se imprime | Dónde se puede utilizar la sección |
---------|----|------|
| Encabezado de informe | Al comienzo del informe. | Utilice el encabezado del informe para obtener información que normalmente aparece en una portada, como un logotipo, un título o una fecha. Cuando coloca un control calculado que usa la función de agregado Suma en el encabezado del informe, la suma calculada es para todo el informe. El encabezado del informe se imprime antes que el encabezado de la página. |
| Encabezado de página | En la parte superior de cada página. | Utilice un encabezado de página para repetir el título del informe en cada página. |
| Encabezado de grupo | Al comienzo de cada nuevo grupo de registros. | Utilice el encabezado del grupo para imprimir el nombre del grupo. Por ejemplo, en un informe que está agrupado por producto, use el encabezado del grupo para imprimir el nombre del producto. Cuando coloca un control calculado que usa la función de agregado Suma en el encabezado del grupo, la suma es para el grupo actual. Puede tener varias secciones de encabezado de grupo en un informe, según la cantidad de niveles de agrupación que haya agregado. Para obtener más información sobre cómo crear encabezados y pies de página de grupo, consulte la sección Agregar agrupación, clasificación o totales. |
| Detalle | Aparece una vez por cada fila en el origen del registro. | Aquí es donde coloca los controles que componen el cuerpo principal del informe. |
| Pie de página del grupo | Al final de cada grupo de registros. | Use un pie de página de grupo para imprimir información de resumen para un grupo. Puede tener varias secciones de pie de página de grupo en un informe, según la cantidad de niveles de agrupación que haya agregado. |
| Pie de página | Al final de cada página. | Utilice un pie de página para imprimir números de página o información por página. |
| Pie de página del informe | Al final del informe. Nota: en la vista Diseño, el pie de página del informe aparece debajo del pie de página. Sin embargo, en todas las demás vistas (vista Diseño, por ejemplo, o cuando el informe se imprime o tiene una vista previa), el pie de página del informe aparece encima del pie de página, justo después del último pie de página del grupo o línea de detalle en la página final. | Utilice el pie de página del informe para imprimir los totales del informe u otra información de resumen para todo el informe. |






## Referencias ##

- [Introducción a los informes en Access](https://support.microsoft.com/en-us/office/introduction-to-reports-in-access-e0869f59-7536-4d19-8e05-7158dcd3681c)
- [Diseño de informes en Access](https://www.uis.edu/informationtechnologyservices/wp-content/uploads/sites/106/2013/04/DesigningReportsinAccess2010.pdf)

