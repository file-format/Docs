{
"fecha": "2023-05-31",
  "keywords": [
"archivo de escritorio",
"¿Qué es un archivo de escritorio?",
"¿Qué contiene el archivo de escritorio?",
"archivo de escritorio de ejemplo",
"cómo abrir un archivo de escritorio",
"¿Cuál es el formato del archivo de escritorio?",
"archivo",
"extensión de archivo de escritorio",
"extensión"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de archivo de ESCRITORIO - Archivo de entrada de escritorio",
  "description":"Obtenga más información sobre el formato DESKTOP y las API que pueden crear y abrir archivos DESKTOP.",
"linktitle": "ESCRITORIO",
  "menu": {
    "docs": {
      "identifier": "settings-desktop",
"parent": "configuración"
}
},
"lastmod": "2023-05-31"
}

## ¿Qué es un archivo de ESCRITORIO?

Un archivo .desktop es un archivo de configuración utilizado por los entornos de escritorio Linux para definir lanzadores y accesos directos a aplicaciones. Proporciona metadatos sobre una aplicación, como su nombre, icono, comando a ejecutar y otras propiedades. Estos archivos se utilizan normalmente para crear accesos directos en menús de aplicaciones, iniciadores de escritorio o paneles en sistemas basados en Linux.

## ¿Qué contiene el archivo DESKTOP?

Un archivo .desktop sigue un formato específico y contiene varios campos clave:

- **[Entrada de escritorio]:** Este es el encabezado de la sección principal del archivo .desktop.
- **Nombre:** Especifica el nombre de la aplicación.
- **Comentario:** Proporciona una breve descripción o comentario sobre la aplicación.
- **Exec:** Define el comando a ejecutar al iniciar la aplicación.
- **Icono:** Especifica la ruta al archivo de icono asociado con la aplicación.
- **Terminal:** Especifica si la aplicación debe ejecutarse en una ventana de terminal.
- **Tipo:** Especifica el tipo de entrada, como "Aplicación" o "Enlace".
- **Categorías:** Especifica categorías o grupos bajo los cuales se debe mostrar la aplicación en el menú.
- **StartupNotify:** Especifica si el entorno de escritorio debe mostrar una notificación de inicio para la aplicación.
- **NoDisplay:** Especifica si la aplicación debe ocultarse de los menús.
- **Acciones:** Define acciones adicionales que se pueden realizar en la aplicación, como abrir un archivo específico.

## Ejemplo de archivo de ESCRITORIO

A continuación se muestra un ejemplo de un archivo .desktop para un editor de texto ficticio llamado "MyTextEditor":

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

En este ejemplo, el archivo .desktop define la aplicación "MyTextEditor" con sus propiedades asociadas. También incluye dos acciones adicionales, "Abrir nueva ventana" y "Abrir archivo existente", a las que se puede acceder desde el menú contextual del iniciador de aplicaciones.

Al colocar un archivo .desktop en directorios específicos como `/usr/share/applications` o `~/.local/share/applications`, el entorno de escritorio lo reconocerá y mostrará la aplicación en consecuencia en los menús o permitirá que se inicie desde escritorio.

## ¿Cómo abrir el archivo ESCRITORIO?

Varios programas de software pueden abrir y manejar archivos .desktop. Estos programas suelen ser administradores de archivos o entornos de escritorio en sistemas basados en Linux. Aquí hay unos ejemplos:

- **Nautilus (Archivos):** El administrador de archivos predeterminado para el entorno de escritorio GNOME.
- **Nemo:** El administrador de archivos para el entorno de escritorio Cinnamon.
- **Dolphin:** El administrador de archivos predeterminado para el entorno de escritorio KDE Plasma.
- **Thunar:** El administrador de archivos predeterminado para el entorno de escritorio Xfce.
- **KDE Menu Editor:** Una herramienta específica del entorno de escritorio KDE Plasma que le permite ver y editar archivos .desktop.

Estos administradores de archivos y entornos de escritorio proporcionan una interfaz gráfica para administrar archivos .desktop. Le permiten ver y editar propiedades de archivos .desktop, crear lanzadores de aplicaciones y organizar accesos directos en los menús de aplicaciones o en el escritorio.

Los archivos .desktop son archivos de texto sin formato, por lo que también puedes abrirlos y editarlos con un editor de texto de tu elección. Simplemente haga clic derecho en el archivo .desktop y seleccione "Abrir con" o "Abrir con otra aplicación" para elegir un editor de texto de la lista de programas instalados.

## ¿Cuál es el formato del archivo de ESCRITORIO?

El formato de archivo .desktop sigue una estructura y formato específicos. Es un archivo de texto sin formato con un conjunto de pares clave-valor organizados en secciones. Aquí hay una descripción general del formato:

- **Encabezados de sección:** Cada sección comienza con un encabezado entre corchetes ([]). La sección principal suele denominarse [Entrada de escritorio] y contiene los metadatos principales de la aplicación o el iniciador.
- **Pares clave-valor:** Dentro de cada sección, usted define propiedades utilizando pares clave-valor. El formato es "Clave=Valor". La clave identifica la propiedad y el valor proporciona los datos correspondientes.
- **Sintaxis de propiedad:** Los valores de propiedad pueden ser de diferentes tipos, incluidas cadenas, valores booleanos, rutas de archivos o listas. El formato de cada valor de propiedad depende de su tipo.
- **Comentarios:** Puede incluir comentarios en el archivo .desktop usando el símbolo '#'. Todo lo que sigue a '#' en línea se considera un comentario y se ignora.

## Referencias
* [Archivos de entrada de escritorio](https://www.baeldung.com/linux/desktop-entry-files)

