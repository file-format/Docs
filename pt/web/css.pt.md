---
date: 2019-10-11
keywords: css, .css, formato de arquivo css, como abrir arquivos css, folhas de estilo em cascata
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de arquivo CSS
linktitle: CSS
description: "Saiba mais sobre o formato de arquivo CSS e as APIs que podem criar e abrir arquivos CSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## O que é um arquivo CSS? ##

CSS (Cascading Style Sheets) são arquivos que descrevem como os elementos HTML são exibidos na tela, papel, etc. Com HTML, você pode ter estilos incorporados ou estilos podem ser definidos em uma folha de estilo externa. Para incorporar os estilos, o \ <style>\</style> etiquetas são usadas. As folhas de estilo externas são armazenadas em arquivos com a extensão .css. Com o CSS externo, você pode incluí-lo em várias páginas HTML para atualizar o estilo dessas páginas. Até mesmo um único arquivo CSS pode ser usado para estilizar um site completo.

## Breve história ##

CSS1 foi lançado em 1996 com Bert Bos como co-autor. O Grupo de Trabalho CSS começou a trabalhar nas questões que não foram abordadas no CSS1. Isso resultou na criação do CSS2 em novembro de 1997, que foi publicado como uma recomendação do W3C em 12 de maio de 1998. Essa versão adicionou suporte para dispositivos específicos de mídia, como impressoras, fontes para download, tabelas e posicionamento de elementos. Em junho de 1999, CSS3 tornou-se a recomendação do W3C. Isso dividiu a documentação em módulos onde cada módulo tinha recursos de extensão definidos em CSS2.

## Como usar arquivos CSS ##

Para usar um arquivo CSS, inclua-o na seção de cabeçalho do documento HTML. Você usa a tag de link para incluir o arquivo conforme mostrado abaixo.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

o atributo *href* da tag de link contém o caminho para o arquivo CSS. Ao fazer isso, os estilos aplicáveis contidos no arquivo CSS incluído são aplicados ao documento HTML.

## Sintaxe CSS ##

Uma regra CSS é composta por dois componentes, um seletor e uma declaração. Um seletor aponta para um elemento no documento HTML. Pode ser uma tag de elemento, nome de classe, nome de id, várias tags mostrando a hierarquia, etc. Uma declaração contém a definição de estilo que inclui propriedade e valor. A propriedade identifica a propriedade do elemento que você deseja alterar e o valor define seu novo valor. Cada regra CSS pode ter várias declarações. O seguinte é um exemplo de uma regra CSS.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

No exemplo acima, temos o **h1** como seletor que seleciona todas as tags h1 no documento HTML. A regra tem duas declarações, uma para peso da fonte e outra para cor. *font-weight* e *color* são propriedades e *700* e *forestgreen* são seus valores, respectivamente.

## Exemplo de uso de CSS ##

Veja a seguir o documento HTML de exemplo e a folha de estilo usada para estilizá-lo. A imagem de comparação também é adicionada para comparar os documentos HTML estilizados e simples

### Documento HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### Folha de estilo CSS ###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### Comparação de saída ###

O lado esquerdo da imagem exibe o documento HTML sem os estilos aplicados e o lado direito exibe o documento HTML com os estilos aplicados.

{{< figure src="../CssExample.jpg" alt="Exemplo de imagem" >}}

## Referências ##

- [CSS - Wikipedia](https://en.wikipedia.org/wiki/CSS)

