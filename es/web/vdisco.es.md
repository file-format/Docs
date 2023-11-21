{
  "date" : "2023-01-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo VDISCO - Formato de archivo de documento de descubrimiento dinámico DISCO",
  "description":"¿Más información sobre qué es un archivo VDISCO?",
  "linktitle" : "VDISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-01-29"
}

## ¿Qué es un archivo VDISCO?

Un archivo VDISCO es un archivo de descubrimiento utilizado por Microsoft Visual Studio en sus servicios web. Proporciona información sobre los servicios web disponibles, como sus URL, espacios de nombres y métodos. El archivo VDISCO es similar al formato de archivo [DISCO](/es/web/disco/) pero se genera en tiempo de ejecución. Se almacena en la aplicación de servicio web y Visual Studio lo utiliza para descubrir y utilizar dinámicamente servicios web en un proyecto. Los archivos VDISCO se utilizan en combinación con el archivo [.asmx](/es/web/asmx/) que contiene el código del servicio web real.

Puede abrir el archivo VDISCO en cualquier editor de texto, como Microsoft Notepad, Github Atom y Apple TextEdit. También se puede abrir con Microsoft Visual Studio 2012 y versiones posteriores para trabajar con él.

## Formato de archivo VDISCO

Un archivo VDISCO se guarda y aloja en formato de archivo [XML](/es/web/xml/), que es un formato universal para la composición y publicación de datos. Contiene la URL del servicio, espacios de nombres y métodos en etiquetas XML estándar donde cada etiqueta contiene el valor respectivo de su información.

## Referencias

* [DISCO](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Descubrimiento de servicios web](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [Ejemplo de C# de clase DiscoveryClient](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

