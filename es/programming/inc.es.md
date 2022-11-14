{
  "date" : "2022-07-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Extensión de archivo INC - ¿Qué es un archivo INC?",
  "description":"Obtenga más información sobre el formato de archivo INC Incluir y las API que pueden crear y abrir archivos INC",
  "linktitle" : "INC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-07-14"
}

## ¿Qué es un archivo INC?

Un archivo INC es un archivo de inclusión que utiliza el código fuente del programa de software para hacer referencia a la información de los encabezados. Es similar al [formato de archivo .h](/es/programación/h/) y contiene declaraciones, funciones, encabezados o macros que pueden ser reutilizados por archivos de código fuente como C++. Los archivos INC son utilizados por una variedad de lenguajes de programación como C, [C++](/es/programming/cpp/), Pascal, [PHP](/es/programming/php/) y [Java](/es/programming/java/). Se pueden usar editores de texto como Microsoft Notepad, Notepad ++ y TextEdit para abrir archivos INC.

## Formato de archivo INC - Más información

Un archivo INC se guarda como archivo de texto sin formato con todas las declaraciones incluidas según la sintaxis de declaración. Un archivo INC también puede hacer referencia a otros archivos INC. Una vez creado, el archivo INC se convierte en parte del proyecto y se puede hacer referencia a él desde archivos fuente como C++. Puede ser referenciado por múltiples archivos fuente para evitar cualquier duplicación.

## Contenido del archivo INC

Los archivos INC pueden incluir la siguiente información.

**`Variables`**: en el caso de la programación orientada a objetos (OOP), un archivo de encabezado de clase contiene definiciones de todas las variables de nivel de clase a las que se puede acceder a través de los archivos de código fuente de implementación.

**`Declaración de métodos`**: todas las declaraciones de métodos se incluyen en los archivos de encabezado .h para que sean accesibles a través de múltiples archivos de implementación.

**`Definiciones de funciones no en línea`**: los archivos de encabezado también pueden contener definiciones de métodos no en línea.

## Desventaja de usar el archivo INC en PHP

PHP son scripts del lado del servidor que se ejecutan en el servidor y devuelven los resultados a las páginas web que llaman. Si un archivo PHP hace referencia a un archivo INC y el servidor no está configurado para analizar archivos .inc (que es muy común), un usuario puede ver el código fuente php en el archivo .inc visitando el directorio URL. Por lo tanto, se debe tener cuidado al usar archivos INC como archivos de inclusión en PHP.

## Referencias

* [Usando INC en PHP](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)

