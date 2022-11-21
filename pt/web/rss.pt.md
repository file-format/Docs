{
  "date" : "2021-06-24",
  "keywords" :[ "RSS", "parcial", "extensão", "arquivo", "formato", "web", "Really Simple Syndication", "Userland Software" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RSS - Really Simple Syndication",
  "description":"Saiba mais sobre o formato de arquivo RSS e APIs que podem criar e abrir arquivos RSS.",
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## O que é um arquivo RSS? ##

Um arquivo com a extensão .rss é conhecido como Really Simple Syndication. RSS é um tipo de arquivo de leitura rápida ou fácil pelo computador, o arquivo XML. Esses arquivos XML são atualizados automaticamente com quaisquer alterações nos dados ou atualizações de um site ou página da web. As informações atualizadas juntamente com os metadados (nome do autor, nome do editor, data de publicação, etc.) e outros conteúdos web do site são extraídos pelos arquivos RSS do usuário e apresentados em um formato de fácil leitura. A melhor característica desses arquivos RSS é que ele funciona em tempo real, e as atualizações, notícias, publicações, ou seja, as últimas, são exibidas na parte superior do arquivo. Usando um arquivo RSS, você pode facilmente criar um arquivo contendo as atualizações mais recentes de qualquer tópico de seu interesse, extraindo o conteúdo relacionado da web e lendo-o usando um arquivo RSS.

## Breve história ##

Em sua carne, o arquivo RSS foi criado pela Netscape, eles inventaram a primeira versão do arquivo RSS, mas depois abandonaram a ideia e não continuaram com as versões mais recentes. Foi então o **Userland Software** que trabalhou no formato de arquivo RSS e continuou a inová-lo com uma versão mais recente, foi assim que o RSS v2 entrou no mercado. No entanto, a invenção do RSS pode ser vinculada de volta ao Resource Description Framework, por Ramanathan V em 1997. O funcionamento dos dois arquivos é bastante semelhante e é seguro assumir que o conceito de RSS foi formado com base no funcionamento do RDF, um leitor de arquivos que foi usado para coletar metadados.

## Especificação Técnica ##

O arquivo RSS é um tipo de arquivo XML e todos os arquivos RSS devem seguir os padrões do XML 1.0. Existem diferentes versões de diferentes arquivos RSS, como 0.91, 0.92, 2.0, entre outros. O arquivo de cada versão está em conformidade com as especificações e padrões dessa versão específica.

## Exemplo de RSS ##

O seguinte é um exemplo simplificado do RSS.

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
## Referência ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
