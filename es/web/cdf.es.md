{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - Formato de definición de canal",
  "description" :"Obtenga más información sobre qué es un archivo CDF y las API que pueden crear y abrir archivos CDF",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## ¿Qué es un archivo CDF?

Un archivo con extensión .cdf es un formato de archivo de distribución de información basado en XLM que se utilizó para publicar actualizaciones frecuentes como "canales". La información se publica desde cualquier servidor web y se entrega automáticamente a computadoras con programas de recepción compatibles, como navegadores web. Los usuarios se suscriben a canales activos y reciben actualizaciones programadas en su escritorio.
Los archivos CDF se usaban anteriormente junto con las tecnologías Active Channel, Active Desktop y Smart Offline Favorites de Microsoft.

## Formato de archivo CDF

Los archivos CDF se guardan como archivos XML, que es un formato de archivo web genérico para el intercambio de información. El formato de archivo CDF es un formato antiguo ahora y nunca fue adoptado ampliamente. En comparación con esto, el RSS de Netscape fue más famoso y ampliamente utilizado.

### Ejemplo de formato de archivo CDF

El siguiente es un ejemplo genérico del formato de archivo CDF.

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://dominio/carpeta/"
LASTMOD="1998-11-05T22:12"
PRECACHE="SI"
NIVEL="0">
<TITLE>Título del canal</TITLE>
<ABSTRACT>Sinopsis de los contenidos del canal.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    LASTMOD="1998-11-05T22:12"
    PRECACHE="SI"
NIVEL="1">
<TITLE>Título de la página dos</TITLE>
<ABSTRACT>Sinopsis del contenido de la página dos.</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## Referencias

* [Formato de definición de canal: por Wikipedia](https://en.wikipedia.org/wiki/Channel_Definition_Format)

