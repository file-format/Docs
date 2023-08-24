{
  "date" : "2019-10-11",
  "keywords" :[ "clase", ".clase","qué es un archivo de clase","cómo abrir un archivo de clase", "extensión", "archivo", "archivo de clase","formato de archivo de clase", "extensión .class ", "archivo de clase en java" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Clase - Formato de archivo de clase Java",
  "description":"Obtenga más información sobre el formato de archivo de clase y las API que pueden crear y abrir archivos de clase",
  "linktitle" : "Class",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## ¿Qué es un archivo de clase?

Un **archivo de clase en Java** es la salida compilada de la clase [.java](/es/programming/java/) que en realidad ejecuta una máquina virtual Java (JVM). Los archivos de clase se pueden ejecutar individualmente y también pueden ser parte de un archivo [JAR](/es/programming/jar/) como un paquete junto con otros archivos de paquete. Estos se pueden crear usando el comando **`javac`** desde la interfaz de línea de comandos. Algunos IDE de Java como [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/Eclipse-ide-java-developers) y NetBeans proporcionan crear archivos de salida .class desde el Java del proyecto. archivos

## Formato de archivo de clase

Un archivo de clase Java se compone de un código de bytes que es un código intermedio que debe ejecutar JVM. Un archivo de clase consta de un flujo de bytes de 8 bits y los elementos de datos multibyte siempre se almacenan en orden big-endian.

### Estructura del archivo de clase

La estructura del archivo de clase es como se muestra a continuación.
```
ClassFile {
    u4             magic;
    u2             minor_version;
    u2             major_version;
    u2             constant_pool_count;
    cp_info        constant_pool[constant_pool_count-1];
    u2             access_flags;
    u2             this_class;
    u2             super_class;
    u2             interfaces_count;
    u2             interfaces[interfaces_count];
    u2             fields_count;
    field_info     fields[fields_count];
    u2             methods_count;
    method_info    methods[methods_count];
    u2             attributes_count;
    attribute_info attributes[attributes_count];
}
```
dónde:

* u1 = cantidad de un byte sin signo
* u2 = cantidad de dos bytes sin signo
* u4 = cantidad de cuatro bytes sin signo

Los detalles de la estructura del archivo .class también se explican en el [formato de archivo de clase] de Oracle (https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) y pueden ser consultados por desarrolladores como referencia. Un resumen de estos campos es el siguiente.

* `mágico`: el elemento mágico proporciona el número mágico que identifica el formato del archivo de clase; tiene el valor 0xCAFEBABE.
* `minor_version`, `major_version`: los valores de los elementos minor_version y major_version son los números de versión principal y secundaria de este archivo de clase.
* `constant_pool_count`: el valor del elemento constant_pool_count es igual al número de entradas en la tabla constant_pool más uno. Un índice constant_pool se considera válido si es mayor que cero y menor que constant_pool_count, a excepción de las constantes de tipo long y double.
* `constant_pool[]` - Constant_pool es una tabla de estructuras (§4.4) que representa varias constantes de cadenas, nombres de clases e interfaces, nombres de campos y otras constantes a las que se hace referencia dentro de la estructura ClassFile y sus subestructuras. El formato de cada entrada de la tabla constant_pool se indica mediante su primer byte de "etiqueta".
* `access_flags`: el valor del elemento access_flags es una máscara de banderas que se utiliza para indicar los permisos de acceso y las propiedades de esta clase o interfaz.
* `this_class`: el valor del elemento this_class debe ser un índice válido en la tabla constant_pool.
* `super_class`: para una clase, el valor del elemento super_class debe ser cero o debe ser un índice válido en la tabla constant_pool.
* `interfaces_count`: el valor del elemento interfaces_count proporciona el número de superinterfaces directas de esta clase o tipo de interfaz.
* `interfaces[]`: cada valor en la matriz de interfaces debe ser un índice válido en la tabla constant_pool.
* `fields_count`: el valor del elemento field_count proporciona el número de estructuras field_info en la tabla de campos.
* `fields[]` - Cada valor en la tabla de campos debe ser una estructura field_info que proporcione una descripción completa de un campo en esta clase o interfaz.
* `methods_count`: el valor del elemento method_count proporciona el número de estructuras method_info en la tabla de métodos.
* `methods[]` - Cada valor en la tabla de métodos debe ser una estructura method_info que proporcione una descripción completa de un método en esta clase o interfaz. Si ninguno de los indicadores ACC_NATIVE y ACC_ABSTRACT se establece en el elemento access_flags de una estructura method_info, también se proporcionan las instrucciones de la máquina virtual Java que implementan el método.
* `attributes_count`: el valor del elemento de atributos_cuenta da el número de atributos (§4.7) en la tabla de atributos de esta clase.
* `attributes[]`: cada valor de la tabla de atributos debe ser una estructura de atributo_info.




## Referencias

* [El formato de archivo de la clase](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

