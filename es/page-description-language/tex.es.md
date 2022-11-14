{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo TEX",
  "description":"Obtenga información sobre el formato de archivo TEX y las API que pueden crear y abrir archivos TEX",
  "linktitle" : "TEX",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo TEX? ##

**TeX** es un lenguaje que se compone de funciones de programación y marcado, que se utiliza para componer documentos. Donald Knuth de la Universidad de Stanford, es el creador de este ingenioso sistema de composición tipográfica. En todo el mundo, TeX es la mejor elección de autores y editores para producir documentos técnicos de alta calidad. TeX realiza un trabajo sobresaliente al dar formato a expresiones matemáticas complejas. En conjunto con una fotocomponedora de alta calidad, TeX compite con los resultados generados por los mejores sistemas de composición tipográfica tradicionales. Por lo tanto, considerado como los sistemas tipográficos digitales con más clase.

Los archivos de entrada TeX se basan en código ASCII, lo que permite compartir manuscritos entre escritores, directores de publicación y críticos. Una amplia variedad de entornos informáticos, casi todas las plataformas modernas y muchas plataformas más antiguas son compatibles con TeX. Además, TeX es un software gratuito, disponible para una amplia gama de consumidores. Muchas instalaciones de UNIX utilizan UNIX troff y TeX como su sistema de formateo para diferentes propósitos. Otras tareas de composición tipográfica se realizan enormemente en forma de LaTeX, ConTeXt y otros paquetes de macros.

## Breve historia ##

TeX fue diseñado y escrito por Donald Knuth en 1978. Guy Steele del Instituto de Tecnología de Massachusetts revisó la entrada/salida de TeX para que funcione bajo el sistema operativo Incompatible como el Sistema de tiempo compartido (ITS). La primera versión de TeX se desarrolló bajo el sistema operativo WAITS de Stanford en el lenguaje de programación (SAIL) y se probó para ejecutarse en un PDP-10. Knuth introdujo la idea de la programación alfabetizada para versiones avanzadas. La programación alfabetizada es una forma de generar código fuente compilable y composición tipográfica (en TeX) para documentación cruzada utilizando el archivo original. El lenguaje utilizado para desarrollar estas versiones avanzadas de TeX se llama WEB, una mezcla de programas DEC PDP-10 Pascal para garantizar la portabilidad.

Una nueva versión revisada de TeX publicada en 1982 y se llamó TeX82. El cambio principal es el reemplazo del algoritmo original de división de guiones con el algoritmo recién escrito por Frank Liang. Para garantizar la portabilidad entre diferentes plataformas, en lugar de usar punto flotante, TeX82 usa aritmética de punto fijo junto con un lenguaje de programación real y completo. En 1989, se lanzaron nuevas versiones de TeX y Metafont. Entonces, la versión 3.0 de TeX facilita entradas de 8 bits, lo que permite 256 caracteres diferentes en el texto. Después de la versión 3, las actualizaciones se indican agregando un dígito adicional al final del decimal, por ejemplo, la versión actual de TeX se indica como 3.14159265. Esta versión se actualizó por última vez el 1-12-2014.

## Entrada TeX ##

Un archivo de entrada a TEX se puede preparar con un editor de texto usando texto ordinario. A diferencia de un procesador de textos típico, este archivo de entrada no permite ningún carácter de control invisible. Un archivo se puede incrustar en otro archivo, que contiene definiciones de macros y definiciones auxiliares que mejoran las capacidades de TeX. Si una instalación de TeX viene con archivos de macro, la información local sobre TeX demuestra cómo usar archivos de macro. La forma estándar de TeX integra una combinación de macros y otras definiciones conocidas como TEX simple.

Sobre la base del conocimiento preciso de los tamaños de todos los caracteres y símbolos, calcula la organización óptima de letras por línea y líneas por página. En el momento del procesamiento del documento, se genera un archivo .dvi, donde "dvi" significa "independiente del dispositivo". Se requieren programas de controlador de dispositivo para imprimir u obtener una vista previa del documento con una extensión dvi. Hoy en día, la generación de dvi se pasa por alto por un pdf-TeX de uso común. No hay conocimiento previo de fuentes disponible dentro de la instalación de TeX, por lo que los archivos de fuentes externas, que son parte del entorno local de TeX, se utilizan para obtener información para el documento.

## Sistema de composición tipográfica ##

El sistema TeX básico puede comprender unas 300 primitivas (comandos). Los primitivos son comandos de bajo nivel, por lo tanto, un usuario común rara vez los usa directamente y la mayoría de las funciones se realizan mediante archivos de formato. Estos archivos de formato son imágenes de memoria precargadas de TeX a las que sigue la carga de grandes colecciones de macros. El formato predeterminado original del idioma, es decir, Plain TeX agrega alrededor de 600 comandos.

Una barra invertida agrupada con llaves indica el comienzo de los comandos TeX. Dado que TeX es un lenguaje basado en macros y tokens, casi todas las características sintácticas de TeX se pueden cambiar en tiempo de ejecución, incluidas las definidas por el usuario, excepto los tokens no expandibles que luego se ejecutan. La expansión en sí es prácticamente libre de problemas. Algunos comandos deben ir después de un argumento que ayude a explicar la función de un comando. Por ejemplo, el comando \vskip le indica a TEX que salte hacia abajo/arriba de la página seguido de un argumento que determina cuánto espacio saltar.

## Versiones ##

LaTeX es el formato más utilizado y fue desarrollado originalmente por Leslie Lamport. LaTeX integra diferentes estilos de documentos para archivos, cartas, libros y diapositivas y ofrece referenciación y numeración automática para diferentes secciones y expresiones matemáticas. AMS-TeX es otro formato popular, desarrollado por la American Mathematical Society.

AMS-TeX ofrece comandos mucho más fáciles de usar, que las revistas pueden redefinir para que se ajusten a su estilo local. LaTeX puede aprovechar los beneficios de AMS-TeX mediante el uso de los "paquetes" de AMS, que luego se denominan AMS-LaTeX. ConTeXt es otro formato escrito por Hans Hagen que se utiliza principalmente para autoedición.

El software TeX ofrece varias funciones que no estaban disponibles, o eran de menor calidad, en otros sistemas de composición tipográfica en el momento de su creación. Algunas de las características innovadoras de este lenguaje se basan en interesantes algoritmos derivados de las tesis de los alumnos de Knuth. Mientras que otros programas de composición tipográfica ahora están incorporando características útiles de TeX en sus programas.

## Referencias ##

* [Sistema de composición tipográfica TeX] (https://en.wikipedia.org/wiki/TeX)

