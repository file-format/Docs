{
  "date" : "2022-06-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo WHL - Archivo de paquete de rueda de Python",
  "description":"Obtenga información sobre el formato de archivo WHL y las API que pueden crear y abrir archivos WHL",
  "linktitle" : "WHL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-29"
}

## ¿Qué es un archivo WHL?

Un archivo WHL (Wheel) es un archivo de paquete de distribución guardado en el formato de rueda de Python. Es una instalación de formato estándar de las distribuciones de Python y contiene todos los archivos y metadatos necesarios para la instalación. El archivo WHL también contiene información sobre las versiones y plataformas de Python compatibles con este archivo de rueda. Similar a un archivo de instalación [MSI](/es/ejecutable/msi/), el formato de archivo WHL es un formato listo para instalar que permite ejecutar el paquete de instalación sin compilar la distribución de origen.

## Formato de archivo WHL

El formato de archivo WHL es un archivo [ZIP](/es/compression/zip/) (.zip) que contiene todos los archivos de instalación y metadatos requeridos por los instaladores para la instalación de un paquete. Estos archivos WHL se pueden extraer usando la opción de descomprimir o aplicaciones de software de descompresión estándar como WinZIP y WinRAR.

### Convención de nombres de archivo WHL

Un archivo WHL se nombra según la siguiente convención.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

Un ejemplo del nombre de archivo WHL es el siguiente.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

* `criptografía` es el nombre del paquete.
* `2.9.2` es la versión del paquete de criptografía. Una versión es una cadena compatible con PEP 440, como 2.9.2, 3.4 o 3.9.0.a3.
* `cp35` es la etiqueta de Python y denota la implementación y versión de Python que exige la rueda.
* `abi3` es la etiqueta ABI. ABI significa interfaz binaria de aplicación.
* `macosx_10_9_x86_64` es la etiqueta de la plataforma, que resulta ser bastante complicada.

## Referencias

* [¿Qué son Python Wheels y por qué debería importarle?](https://realpython.com/python-wheels/)
* [Rueda de Python](https://pypi.org/project/wheel/)

