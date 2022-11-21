{
  "date" : "2019-10-11",
  "keywords" :[ "htm", "arquivo htm", "formato de arquivo htm", "tipo de arquivo htm", "arquivo", "tipo", "o que é um arquivo htm" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo HTM",
  "description" :"Seu guia de formato de arquivo para saber o que é um arquivo HTM e APIs que podem criá-los e abri-los.",
  "linktitle" : "HTM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo HTM?

Arquivos com extensão **.htm** representam Hypertext Markup Language para criar páginas da web para exibição em navegadores da web, como Google Chrome, Internet Explorer, Firefox e vários outros. Ele define as marcações para a criação de páginas estáticas a serem publicadas na World Wide Web (WWW) para acesso de outras pessoas. Essas marcações informam aos navegadores como exibir o conteúdo de uma página da web. Essas páginas podem conter texto simples, imagens, hiperlinks para outras páginas, vídeos e outras informações de mídia. Quando uma página da Web é publicada, você pode dar uma olhada no código de marcação por trás dela visualizando a fonte da página. Os navegadores modernos permitem inspecionar cada seção de uma página da Web onde cada subdivisão ou elemento de marcação na fonte HTM é elaborado.

## Breve História do HTM

Desde a sua criação e primeira distribuição, as especificações HTML foram mantidas pelo World Wide Web Consortium (W3C) desde 1996. Em 2000, também se tornou um padrão internacional (ISO/IEC 15445:2000). Em 1999, o HTML 4.01 foi publicado. Em 2004, o Web Hypertext Application Technology Working Group (WHATWG) começou a trabalhar na versão HTML5, que se tornou uma entrega conjunta com o W3C em 2008. Foi concluída e padronizada em 28 de outubro de 2014.

## Formato de arquivo HTML

Um documento HTML 4 é composto de três partes:

1. uma linha contendo informações sobre a versão HTML
1. uma seção de cabeçalho declarativa
1. um corpo, que contém o conteúdo real do documento. O corpo pode ser implementado pelo elemento BODY ou pelo elemento FRAMESET para conter o corpo em quadros

Cada seção pode ser liderada ou seguida por espaços em branco, novas linhas, guias e comentários. Um exemplo de um documento HTML simples é mostrado abaixo:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### Versão informação

A primeira linha de código,<!DOCTYPE html> , é chamado de declaração de doctype e informa ao navegador em qual versão do HTML a página está escrita. Dependendo da versão do HTML, há várias declarações de doctype diferentes que nomeiam a definição de tipo de documento (DTD) em uso para o documento. Cada DTD difere dos outros nos elementos que suporta e difere da seguinte forma:

* HTML 4.01 Strict - inclui todos os elementos e atributos que não foram [descontinuados](https://www.w3.org/TR/html401/conform.html#deprecated) ou não aparecem em documentos de conjunto de quadros
* HTML 4.01 Transitional - inclui tudo no DTD estrito, além de elementos e atributos obsoletos (a maioria dos quais diz respeito à apresentação visual
* HTML 4.01 Frameset - inclui tudo no DTD de transição mais os frames também

Para **HTML5**, as informações da versão são as mencionadas abaixo.

```
<!DOCTYPE html>
```

### Informações do cabeçalho

O cabeçalho de um documento HTML pode incluir vários elementos HTML que não são renderizados pelo navegador. Esses elementos são metadados que descrevem informações sobre a página ou incluem seções usadas para buscar informações de recursos externos, como folhas de estilo CSS ou arquivos JavaScript. O cabeçalho de uma página é representado por \<head> marca e termina com \</head> marcação.

<html>Para definir o título da página, o \<title> elemento é o único que é necessário dentro das tags \<head>. O mesmo é usado pelos motores de busca para identificar o título de uma página. </html>

### Informações do corpo

Esta é a seção principal do arquivo que contém todo o conteúdo do arquivo que é renderizado pelos navegadores. O corpo HTML pode conter marcações que podem se referir a vários blocos de construção na forma de tags. Ele pode conter vários tipos diferentes de informações como texto, imagens, cores, gráficos, etc. Além disso, elementos de áudio e vídeo também podem ser incorporados no corpo html para renderização pelos navegadores. Na presença de aplicativos modernos de folhas de estilo para representação visual, os atributos de apresentação de BODY, como cor de fundo, cor do link, cor do texto, etc., foram preteridos. Assim, os mesmos efeitos podem ser alcançados usando folhas de estilo conforme mostrado abaixo:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

As folhas de estilo inline são fáceis de incorporar e, para aplicações rápidas aos efeitos visuais, as folhas de estilo externas tornam mais conveniente implantar uma vez e acessar em vários lugares.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### Elementos HTML

Como mencionado anteriormente, o conteúdo dentro do HTML Body é representado por tags, também conhecidas como Html Elements. Cada tag pode ter informações adicionais na forma de atributos que são escritos como
```
<tag attribute1#"value1" attribute2#"value2">
```
embora não seja necessário ter atributos com cada tag. Se os atributos não forem mencionados, os valores padrão serão usados em cada caso. A seguir estão alguns dos exemplos de elementos:

#### Cabeçalho

```
<head>
  <title>The Title</title>
</head>
```

#### Títulos

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Parágrafos

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```

## Referências

* [A estrutura global do documento HTML](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

