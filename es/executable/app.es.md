{
"fecha": "2023-02-02",
  "keywords": [
"archivo de aplicación",
"¿Qué es un archivo de aplicación?",
"archivo",
"cómo abrir el archivo de la aplicación",
"extensión de archivo de aplicación",
"extensión"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
  "description":"Obtenga más información sobre el formato de archivo APP y las API que pueden crear y abrir archivos APP.",
"title": "Formato de archivo APP - Paquete de aplicaciones macOS",
"linktitle": "APLICACIÓN",
  "menu": {
    "docs": {
      "identifier": "executable-app",
"parent": "ejecutable"
}
},
"lastmod": "2023-02-02"
}

## ¿Qué es un archivo APP?

Un archivo .app en macOS es un tipo especial de directorio que contiene todos los archivos necesarios para ejecutar una aplicación específica, incluido el código ejecutable, los recursos y los metadatos. La extensión .app indica al sistema operativo que este directorio debe tratarse como una sola unidad, en lugar de una colección de archivos separados, y que se puede iniciar directamente desde el Finder o el Dock.

Finder es la aplicación de administración de archivos predeterminada en macOS. Le permite explorar y organizar los archivos y directorios de su computadora. El Dock es una función de macOS que proporciona acceso rápido a aplicaciones y documentos de uso frecuente. Tanto Finder como Dock le permiten iniciar aplicaciones haciendo clic en sus archivos .app, lo que abrirá el paquete de aplicaciones correspondiente. Cuando inicia una aplicación, se ejecuta el código ejecutable dentro del paquete .app, lo que hace que la aplicación esté disponible para su uso. El archivo .app es la representación de la aplicación en el sistema de archivos y proporciona una forma para que el usuario acceda e inicie la aplicación.

Cuando haces clic derecho en un archivo .app en Finder en un sistema macOS y seleccionas "Mostrar contenido del paquete", podrás ver la estructura interna del paquete de aplicaciones. Esto es útil si desea acceder a recursos o archivos utilizados por la aplicación, o si desea inspeccionar el contenido de la aplicación para solucionar problemas. El contenido del paquete de un archivo .app normalmente incluye directorios de recursos como imágenes y sonidos, así como el código ejecutable de la aplicación. Al explorar el contenido de un archivo .app, puede obtener información más profunda sobre cómo se crea la aplicación y qué hace.

## ¿Cómo abrir el archivo APP?

Para abrir un archivo .app en macOS, simplemente haga doble clic en el archivo en Finder. Esto iniciará la aplicación contenida en el paquete .app. Si la aplicación está instalada en su sistema y se ha asociado con el tipo de archivo .app, al hacer doble clic en el archivo se debería iniciar la aplicación automáticamente. Si la aplicación no está asociada con el tipo de archivo .app, es posible que deba hacer clic derecho en el archivo y seleccionar "Abrir con" para elegir una aplicación adecuada para abrirlo.

Puede abrir un archivo .app en la Terminal en macOS usando el comando "abrir". Para hacer esto, navegue hasta el directorio donde se encuentra el archivo .app usando el comando "cd" y luego ejecute el siguiente comando:

```
open <AppName>.app 
```

dónde<AppName> es el nombre de la aplicación que desea iniciar. Esto iniciará la aplicación como si hubiera hecho doble clic en ella en Finder. El comando "abrir" es una utilidad de propósito general que se puede utilizar para abrir muchos tipos diferentes de archivos, incluidas aplicaciones, documentos y directorios. Cuando utiliza el comando "abrir" en un archivo .app, se inicia la aplicación contenida en el paquete.

## Referencias
* [Bundle (macOS)](https://en.wikipedia.org/wiki/Bundle_(macOS))
