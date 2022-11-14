{
  "date" : "2022-02-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo WSDL - Archivo de lenguaje de descripción de servicios web",
  "description":"Obtenga más información sobre qué es un archivo WSDL y las API que pueden crear y abrir archivos WSDL",
  "linktitle" : "WSDL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-02-03"
}

## ¿Qué es un archivo WSDL?

Un archivo WSDL es un archivo de lenguaje de descripción de servicios web escrito en lenguaje XML para describir servicios web. Contiene información sobre los puntos finales o interfaces para la conectividad con el mundo exterior en un formato universalmente aceptado. [Especificaciones de formato de archivo WSDL](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (mantenido por W3C.org) define los términos para publicar fuentes de datos para el intercambio de datos a fin de tener acceso a aplicaciones remotas a través de puertos y puntos finales.

## Formato de archivo WSDL - Más información

Los archivos WSDL se guardan como archivos XML que son legibles por humanos y se pueden abrir en cualquier editor de texto para ver el contenido.

## Descripción del servicio WSDL

Las especificaciones de formato de archivo WSDL 2.0 describen el servicio WSDL como compuesto por dos etapas:

- Etapa abstracta
- Escenario de hormigón

La reutilización de los diseños de descripción y preocupación independiente se rige por un servicio Web. Esto se logra utilizando varios tipos diferentes de elementos, incluidos tipos (definiciones de tipos de datos), mensajes (los datos comunicados), operaciones (acciones) y protocolos utilizados por el servicio. Todos estos se gestionan a nivel abstracto. El enlace de los detalles del formato de transporte y conexión se especifica mediante el enlace, que agrupa los puntos finales para implementar una interfaz común.

### ¿Qué tecnologías se pueden utilizar para interactuar con los servicios WSDL?

Se pueden usar varias tecnologías diferentes para interactuar con los servicios WSDL, incluidas las aplicaciones ASP.NET, C/C++ y Java.

## Ejemplo de WSDL

```
<message name="getTermRequest">
  <part name="term" type="xs:string"/>
</message>

<message name="getTermResponse">
  <part name="value" type="xs:string"/>
</message>

<portType name="glossaryTerms">
  <operation name="getTerm">
    <input message="getTermRequest"/>
    <output message="getTermResponse"/>
  </operation>
</portType>
```

En este ejemplo, portType "glossaryTerms" define una operación unidireccional llamada "setTerm".

## Referencias

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)
* [Especificaciones del formato de archivo WSDL](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)

