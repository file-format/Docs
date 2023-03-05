{
  "date" : "2020-03-16",
  "keywords" :[ "Archivo IFC", "Formato", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo IFC y las API que pueden crear y abrir archivos IFC",
  "title" :"Formato de archivo IFC",
  "linktitle" : "IFC",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo IFC?

Los archivos con extensión IFC se refieren al formato de archivo Industry Foundation Classes (IFC) que establece estándares internacionales para importar y exportar objetos de construcción y sus propiedades. Este formato de archivo proporciona interoperabilidad entre diferentes aplicaciones de software. Las especificaciones para este formato de archivo son desarrolladas y mantenidas por buildingSMART International como su estándar de datos. El objetivo final del formato de archivo IFC es mejorar la comunicación, la productividad, el tiempo de entrega y la calidad a lo largo del ciclo de vida de un edificio.

Debido a los estándares establecidos para objetos comunes en la industria de la construcción, reduce la pérdida de información durante la transmisión de una aplicación a otra. IFC puede contener datos de geometría, cálculo, cantidades, administración de instalaciones, precios, etc. para muchas profesiones diferentes (arquitecto, eléctrico, HVAC, estructural, terreno, etc.).

## Breve historia ##

Autodesk tomó la iniciativa de IFC en 1994 para respaldar el desarrollo de aplicaciones integradas e incluyó empresas como Honeywell, Butler Manufacturing y AT&T. En 1995, la membresía se abrió para cualquiera y el nombre se cambió a International Alliance for Interoperability. La intención de la organización sin fines de lucro era publicar Industry Foundation Class (IFC) como un modelo de producto AEC. En 2005, el nombre se cambió nuevamente y ahora buildSMART lo mantiene.

## Formato de archivo IFC ##

El formato de archivo IFC ha sufrido varios cambios en el pasado para alcanzar las especificaciones de formato de archivo v4. Ocurrieron varios cambios menores de vez en cuando y se han hecho parte de las especificaciones como Anexos. A continuación se incluye una lista de diferentes versiones de especificaciones de archivos que se han hecho públicas en el pasado.

* IFC4 Agregar 2 (2016) IFC4 Agregar 1 (2015)
* IFC4 (marzo de 2013) ifcXML2x3 (junio de 2007)
* IFC2x3 (febrero de 2006) ifcXML2 para IFC2x2 add1 (RC2)
* Apéndice 1 de IFC2x2 (julio de 2004) ifcXML2 para IFC2x2 (RC1)
* IFC 2x2IFC 2x Apéndice 1ifcXML1 para IFC2x y
* Anexo IFC2x 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5

Las últimas versiones de las especificaciones de formato de archivo IFC siempre están disponibles en el sitio web de buildingSMART y el desarrollador debe consultarlas para cualquier tipo de aplicación que planee desarrollar. Al momento de escribir este artículo, las especificaciones de la versión 4 son las más recientes disponibles en línea.

### Formatos de archivos de datos IFC ###

El formato de archivo IFF admite el intercambio de datos entre aplicaciones que utilizan diferentes formatos, como se indica a continuación:

**IFC:** Este es el formato de intercambio IFC predeterminado y utiliza la estructura de archivos físicos STEP según ISO 10303-21. Este formato de archivo tiene la extensión de archivo .ifc y es el formato IFC más utilizado.

**IFC-XML:** Es una versión de formato de archivo XML de IFC que puede ser generado directamente por la aplicación de envío según la estructura ISO 10303-28, también llamado STEP-XML. El formato de archivo IFC-XML se considera adecuado para la interoperabilidad entre herramientas XML. En comparación con el formato de archivo IFC, el IFC-XML es un 300-400 % más grande en tamaño.

**IFC-ZIP:** Es una versión comprimida [ZIP](/es/compression/zip/) de IFC o IFC-XML donde uno de estos archivos se encuentra en el directorio principal del archivo zip. Este formato comprime un .ifc en un 60-80 % y un archivo .ifc XML en un 90-95 %.

### Arquitectura IFC ###

La especificación IFC incluye términos, conceptos y elementos de especificación de datos que se originan a partir del uso en disciplinas, oficios y profesiones del sector de la industria de la construcción y la gestión de instalaciones. Términos y conceptos utiliza palabras en inglés simple, los elementos de datos dentro de la especificación de datos siguen una convención de nomenclatura.

los nombres de elementos de datos para tipos, entidades, reglas y funciones comienzan con el prefijo "Ifc" y continúan con las palabras en inglés en la convención de nomenclatura CamelCase (sin guión bajo, la primera letra de la palabra en mayúsculas); los nombres de atributo dentro de una entidad siguen la convención de nomenclatura CamelCase sin prefijo; las definiciones de conjuntos de propiedades que forman parte de este estándar comienzan con el prefijo "Pset_" y continúan con las palabras en inglés en la convención de nomenclatura CamelCase; las definiciones de conjuntos de cantidad que forman parte de este estándar comienzan con el prefijo "Qto_" y continúan con las palabras en inglés en la convención de nomenclatura CamelCase.

La arquitectura de esquema de datos de IFC define cuatro capas conceptuales, cada esquema individual se asigna exactamente a una capa conceptual.

**Capa de recursos**: la capa más baja incluye todos los esquemas individuales que contienen definiciones de recursos, esas definiciones no incluyen un identificador único global y no se utilizarán independientemente de una definición declarada en una capa superior;

**Capa central**: la siguiente capa incluye el esquema del núcleo y los esquemas de extensión del núcleo, que contienen las definiciones de entidad más generales, todas las entidades definidas en la capa central o superior llevan una identificación única global y, opcionalmente, información de propietario e historial;

**Capa de interoperabilidad**: la siguiente capa incluye esquemas que contienen definiciones de entidades que son específicas de un producto general, proceso o especialización de recursos utilizados en varias disciplinas, esas definiciones se utilizan normalmente para el intercambio entre dominios y el intercambio de información de construcción;

**Capa de dominio**: la capa más alta incluye esquemas que contienen definiciones de entidades que son especializaciones de productos, procesos o recursos específicos de una determinada disciplina; esas definiciones se utilizan normalmente para el intercambio dentro del dominio y el intercambio de información.

## Referencias ##

* [Clases fundamentales de la industria: por Wikipedia](https://en.wikipedia.org/wiki/Industry_Foundation_Classes)

