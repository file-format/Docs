{
  "date" : "2021-07-29",
  "keywords" :[ "archivo md5", "formato de archivo md5", "qué es un archivo md5", "archivo", "ejemplo md5", "extensión de archivo md5","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD5 - Archivo de suma de comprobación MD5",
  "description":"Obtenga información sobre el archivo MD5 y las API que pueden crear y abrir archivos MD5",
  "linktitle" : "MD5",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## ¿Qué es un archivo MD5?

Un archivo MD5 es un archivo de suma de comprobación que se utiliza para verificar la integridad de un archivo. Es similar a una huella digital para el archivo asociado y se genera de forma única mediante un algoritmo que utiliza la cantidad de bits del archivo. Se utiliza para verificar el archivo con software como [md5sum](http://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html). Una ventaja de usar archivos MD5 es verificar que los archivos descargados no estén corruptos.

## Formato de archivo MD5 - Más información

Por lo general, un archivo MD5 se guarda con el mismo nombre que el nombre del archivo original pero con la extensión .md5. Por ejemplo, si el nombre del archivo asociado es `abc_987_123456.grb`, el nombre del archivo MD5 correspondiente será `abc_987_123456.grb.md5`. Los archivos MD5 ayudan a identificar que un archivo recibido o descargado no está dañado ni afectado por contenido malicioso. En resumen, los archivos MD5 garantizan la integridad de un archivo.


## ¿Cómo verificar la suma de verificación MD5?

Se puede comprobar/verificar un solo archivo para MD5 usando la herramienta [md5sum](https://en.wikipedia.org/wiki/Md5sum) de la siguiente manera.

```
md5sum -c abc_987_123456.grb.md5
```

## Referencias

* [md5sum - Wikipedia](https://en.wikipedia.org/wiki/Md5sum)

