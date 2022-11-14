{
  "date" : "2021-08-31", 

  "keywords" :[ "AS", "archivo", "extensión", "formato de archivo", "", "Guía de programación", "Ejemplo de AS", "Adobe Flash", "ActionScript", "Mасrоmedia Flash"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AS - Formato de archivo ActionScript",
  "description":"Obtenga información sobre el formato de archivo AS y las API que pueden crear y abrir archivos AS",
  "linktitle" : "AS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-31"
}

## ¿Qué es un archivo AS? ##

El AS, también conocido como ActionScript, se diseñó inicialmente para controlar animaciones vectoriales simples en 2D realizadas en Adobe Flash (anteriormente Macromedia Flash). Inicialmente centradas en la animación, las primeras versiones de contenido Flash ofrecían pocas funciones de interactividad y, por lo tanto, tenían una capacidad de escritura muy limitada. Las versiones posteriores agregaron funcionalidad que permite la creación de juegos basados en la web y aplicaciones web enriquecidas con medios de transmisión (como video y audio).

## Formato de archivo AS ##

ActionScrirt es adecuado para el desarrollo de equipos de escritorio y dispositivos móviles a través de Adobe Air, para su uso en algunas aplicaciones de bases de datos y, básicamente, para robótica, como con el kit de control Make. Flash MX 2004 introdujo ActionScrirt 2.0, un lenguaje de escritura más adecuado para el desarrollo de aplicaciones Flash. A menudo es posible ahorrar tiempo escribiendo algo en lugar de animarlo, lo que generalmente también permite un mayor nivel de flexibilidad al editar.

Desde la llegada de Flash Player 9 alrh (en 2006), se ha lanzado una versión más nueva de АсtionSсriрt, АсtionSсrirt 3.0. Esta versión del lenguaje está pensada para ser compilada y ejecutada en una versión de la máquina virtual ActionScript que ha sido completamente reescrita desde cero. Debido a esto, el código escrito en АсtionSсrirt 3.0 generalmente está destinado a Flash Player 9 y superior y no funcionará en versiones anteriores. Al mismo tiempo, АсtionSсrirt 3.0 se ejecuta hasta 10 veces más rápido que el anterior.

El código AS es el mejor debido a las mejoras del compilador Just-In-Time. Las bibliotecas flash se pueden usar con las capacidades XML del navegador para generar contenido enriquecido en el navegador. Adobe ofrece su línea de productos Flex para satisfacer la demanda de aplicaciones web enriquecidas basadas en el tiempo de ejecución de Flash, con comportamientos y programación realizados en ActionScript. АсtionSсriрt 3.0 forma la base de Flex 2 АРI.

 

## Breve historia ##

ActionScrirt comenzó como un lenguaje de programación orientado a objetos para la herramienta de autoría Flash de Macromedia, más tarde desarrollado por Adobe Systems como Adobe Flash. Las tres primeras versiones de la herramienta de creación de Flash proporcionaban funciones de interactividad limitadas. Los primeros desarrolladores de Flash podían adjuntar un comando simple, llamado "acción", a un botón o un marco. El conjunto de acciones eran controles básicos de navegación, con comandos como "reproducir", "almacenar", "getURL" y "ir y retransmitir".


Con el lanzamiento de Flash 4 en 1999, este simple conjunto de acciones se convirtió en un pequeño lenguaje de escritura. Las nuevas capacidades introducidas para Flash 4 incluyeron variables, expresiones, operadores, declaraciones if y loor. Aunque se conoce internamente como "ScriptScrirt", el manual de usuario de Flash 4 y los documentos de marketing continuaron usando el término "acciones" para describir este conjunto de comandos.


## Especificación técnica ##

La información de verificación de tipos en tiempo de compilación y en tiempo de ejecución existe tanto en tiempo de compilación como en tiempo de ejecución. El rendimiento mejorado de un sistema de herencia basado en clases lo separa del sistema de herencia basado en prototipos. Proporciona soporte para paquetes, nombres y expresiones regulares, y se compila en un tipo de código de bytes completamente nuevo, incompatible con ActionScript 1.0 y código de 2.0 bytes.


La versión revisada de Flash Player AI está organizada en paquetes y su sistema unificado de gestión de eventos se basa en el estándar de gestión de eventos DOM. Hay una integración de EMMA Sсrirt para XML (E4X) para fines de procesamiento de XML. Brinda un acceso directo a la lista de visualización del tiempo de ejecución de Flash para un control completo de lo que se muestra en el tiempo de ejecución y una implementación completamente conforme del borrador de la especificación de la cuarta edición del ECM.


ActionScript tiene soporte limitado para objetos 3D dinámicos. (rotación X, Y, Z y mapeo de texturas). Los tipos de datos de nivel superior de ActionScript 2 incluyen Sin cadena + Una lista de caracteres como "Hello World" y también Número + Cualquier valor numérico. АсtionSсriрt 2 tipos de datos completos Movie Сliр + una creación de АсtionSсriрt que permite un fácil uso de los objetos visibles y también Text Field + А simрle dynаmiс o campo de texto de entrada. Hereda el tipo de imagen en movimiento.


АсtionSсriрt 3 tipos de datos primitivos (primo) incluye el tipo de datos booleanos tiene solo dos valores posibles: verdadero y falso o 1 y 0. Todos los demás valores son válidos. ActionScrirt 3 con algunos tipos de datos complejos incluye un objeto de fecha que contiene la representación digital de fecha/hora. Y también Error, un error genérico sin objeto que permite el informe de errores de tiempo de ejecución cuando se lanza como una excepción.


## Ejemplo de formato de archivo AS ##

```
package com.example
{
    import flash.text.TextField;
    import flash.display.Sprite;

    public class Greeter extends Sprite
    {
        public function Greeter()
        {
            var txtHello: TextField = new TextField();
            txtHello.text = "Hello World";
            addParent3(txtHello);
    }
}
}
```

## Referencia ##

* [AS - por Wikipedia]( https://en.wikipedia.org/wiki/ActionScript)



