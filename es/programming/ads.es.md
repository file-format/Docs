
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo ADS - Formato de archivo de especificación Ada",
  "description":"Aprenda qué es el formato de archivo ADS con ejemplos y API que pueden crear y abrir archivos ADS",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## ¿Qué es un archivo ADS?

Un archivo ADS es un archivo de especificación para un proyecto de programación de Ada. Es similar a una clase para Java, o al par de encabezado e implementación en el caso de C++. Las especificaciones públicas y privadas del paquete Ada se almacenan en el archivo .ads. El archivo .adb, por el contrario, contiene la implementación o los cuerpos de Ada. Al igual que [C++](/es/programming/cpp/), Ada ofrece separación entre especificaciones e implementaciones independientes de OOP.

Los archivos ADS se pueden abrir en cualquier editor de texto, como Microsoft Notepad, Notepad ++ y Atom.

## Formato de archivo de anuncios

Los archivos ADS tienen un formato de archivo de texto sin formato simple y se pueden abrir/editar con cualquier editor de texto. Los paquetes de Ada se pueden organizar en jerarquías. Una unidad secundaria se puede declarar de la siguiente manera:

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## Referencias

* [Paquetes de Ada](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

