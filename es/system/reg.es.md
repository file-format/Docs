{
"fecha": "2023-03-07",
  "keywords": [
"archivo de registro",
"¿Qué es un archivo de registro?",
"archivo",
"extensión de archivo reg",
"extensión"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de archivo REG - Archivo de registro de Windows",
  "description":"Obtenga información sobre el formato REG y las API que pueden crear y abrir archivos REG.",
"título del enlace": "REG",
  "menu": {
    "docs": {
      "identifier": "system-reg",
"parent": "sistema"
}
},
"lastmod": "2023-03-07"
}

## ¿Qué es un archivo REG?

Un archivo REG es un formato de archivo utilizado para importar o exportar datos del Registro de Windows. El Registro de Windows es una base de datos jerárquica que almacena ajustes de configuración y opciones para el sistema operativo Windows y las aplicaciones instaladas. El registro contiene información como preferencias del usuario, configuración de aplicaciones, datos de configuración de hardware y software, y más.

Un archivo REG normalmente tiene una extensión de archivo ".reg" y es un archivo de texto sin formato que contiene una serie de entradas y valores de registro en un formato específico. El formato consta de una sección de encabezado que identifica el archivo como un archivo de registro, seguida de una serie de pares de clave y valor que representan entradas de registro.

## Formato de archivo REG - Más información

A continuación se muestra un ejemplo de un formato de archivo de registro:

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

La primera línea del archivo especifica la versión del editor de registro. Las siguientes líneas contienen las entradas del registro en el formato de una ruta de clave seguida de un nombre de valor y datos de valor. En este ejemplo, el archivo de registro contiene dos entradas: una que agrega un programa llamado "Example.exe" a la lista de inicio de Windows y otra que establece el valor "Oculto" en la configuración avanzada del Explorador de Windows en "verdadero".

Los archivos de registro se pueden crear y editar utilizando un editor de texto como el Bloc de notas. A menudo se utilizan para realizar copias de seguridad y restauración, así como para configurar varias computadoras con la misma configuración de registro.

## Importar o exportar el registro de Windows

Un archivo REG es un tipo de archivo utilizado para importar o exportar datos del Registro de Windows. El Registro de Windows es una base de datos jerárquica que almacena ajustes de configuración y opciones para el sistema operativo Windows y las aplicaciones instaladas. El registro contiene información como preferencias del usuario, configuración de aplicaciones, datos de configuración de hardware y software, y más.

Los archivos de registro se pueden usar para crear o modificar entradas de registro y, a menudo, se usan con fines de copia de seguridad y restauración, así como para configurar varias computadoras con la misma configuración de registro. A continuación se explica cómo utilizar un archivo reg para agregar una nueva entrada de registro al Registro de Windows:

1. Cree un nuevo archivo de texto usando un editor de texto como el Bloc de notas.
2. Escriba la entrada del registro en el formato correcto. El formato consta de una sección de encabezado que identifica el archivo como un archivo de registro, seguida de una serie de pares de clave y valor que representan entradas de registro. He aquí un ejemplo:

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

Esto crea una nueva clave llamada "Ejemplo" bajo la clave "Software" en el subárbol de registro del usuario actual y establece el valor "Configuración1" en "Valor1".

3. Guarde el archivo con una extensión de archivo .reg.
4. Haga doble clic en el archivo .reg para agregar la nueva entrada del registro al Registro de Windows.

Se le pedirá que confirme que desea agregar la entrada al registro. Una vez que confirme, la nueva entrada se agregará al registro y podrá verificarla utilizando la herramienta Editor del Registro.

## Referencias
* [Registro de Windows](https://en.wikipedia.org/wiki/Windows_Registry)

