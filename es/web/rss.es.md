{
  "date" : "2021-06-24",
  "keywords" :[ "RSS", "parcial", "extensión", "archivo", "formato", "web", "Really Simple Syndication","Userland Software" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RSS - Sindicación realmente simple",
  "description":"Obtenga información sobre el formato de archivo RSS y las API que pueden crear y abrir archivos RSS",
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## ¿Qué es un archivo RSS? ##

Un archivo con la extensión .rss se conoce como Really Simple Syndication. RSS es un tipo de archivo fácil de leer por la computadora, el archivo XML. Estos archivos XML se actualizan automáticamente con cualquier cambio en los datos o actualizaciones de un sitio web o página web. La información actualizada junto con los metadatos (nombre del autor, nombre del editor, fecha de publicación, etc.) y otros contenidos web del sitio web son extraídos por los archivos RSS del usuario y presentados en un formato fácil de leer. La mejor característica de estos archivos RSS es que funcionan en tiempo real y las actualizaciones, noticias, publicaciones, es decir, las últimas, se muestran en la parte superior del archivo. Usando un archivo RSS, puede crear fácilmente un archivo que contenga las últimas actualizaciones de cualquier tema que le interese, extrayendo el contenido relacionado de la web y leyéndolo usando un archivo RSS.

## Breve historia ##

En realidad, el archivo RSS fue creado por primera vez por Netscape, inventaron la primera versión del archivo RSS, pero luego abandonaron la idea y no continuaron con las versiones más nuevas. Fue entonces el **Userland Software** el que trabajó en el formato de archivo RSS y continuó innovándolo con una versión más nueva, así es como RSS v2 entró al mercado. Sin embargo, la invención de RSS se puede vincular a Resource Description Framework, por Ramanathan V en 1997. El funcionamiento de los dos archivos es bastante similar y es seguro asumir que el concepto de RSS se formó en base al funcionamiento de RDF, un lector de archivos que se utilizó para recopilar metadatos.

## Especificación técnica ##

El archivo RSS es un tipo de archivo XML y todos los archivos RSS deben seguir los estándares de XML 1.0. Existen diferentes versiones de diferentes archivos RSS, como 0.91, 0.92, 2.0, entre otros. El archivo de cada versión se ajusta a las especificaciones y estándares de esa versión específica.

## RSS Ejemplo ##

El siguiente es un ejemplo simplificado del RSS.

```
<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0">
	<channel>
		<title>RSS Title</title>
		<description>This is a simplified example of the RSS feed</description>
		<link>https://blog.fileformat.com/</link>
		<copyright>2021 fileformat.com All rights reserved</copyright>
		<lastBuildDate>Wed, 22 Jun 2021 00:01:00 +0000</lastBuildDate>
		<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		<ttl>1800</ttl>
		<item>
			<title>Example entry</title>
			<description>Here is some text containing an interesting description.</description>
			<link>https://blog.fileformat.com/blog/post/1</link>
			<guid isPermaLink="false">9bd605d5-1921-8i67-dgft-65g635d3587u</guid>
			<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		</item>
	</channel>
</rss>

```
## Referencia ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
