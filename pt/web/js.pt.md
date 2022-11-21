---
date: 2019-10-11
keywords: js, .js, formato de arquivo js, como abrir arquivos js, arquivos javascript
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de arquivo JS
linktitle: JS
description: "Saiba mais sobre o formato de arquivo JS e as APIs que podem criar e abrir arquivos JS."
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## O que é um arquivo JS? ##

JS (JavaScript) são arquivos que contêm código JavaScript para execução em páginas da web. Os arquivos JavaScript são armazenados com a extensão .js. Dentro do documento [HTML](/pt/web/html/), você pode incorporar o código JavaScript usando o \ <script>\</script> tags ou inclua um arquivo JS. Semelhante aos arquivos [CSS](/pt/web/css/), os arquivos JS podem ser incluídos em vários documentos HTML para reutilização de código. JavaScript pode ser usado para manipular o HTML DOM.

## Breve história ##

O JavaScript foi lançado pela primeira vez como parte do Navigator Browser em setembro de 1995 com o nome LiveScript da Netscape. Foi renomeado JavaScript três meses depois. Em 1996, a Microsoft fez a engenharia reversa do interpretador do Navigator para criar o JScript. JScript foi lançado com o Internet Explorer e era muito diferente do JavaScript.

A Netscape submeteu JavaScript à ECMA International que levou ao lançamento oficial da primeira especificação ECMAScript em 1997. ECMAScript 2 foi lançado em 1998, ECMAScript 3 em 1999, e o trabalho em ECMAScript 4 começou em 2000, mas nunca chegou a ser concretizado.

Jesse James Garrett em 2005 lançou um white paper onde cunhou o termo *Ajax*. Isso usava JavaScript como backbone para criar aplicativos da Web que carregavam dados em segundo plano e evitavam recarregamentos de página inteira. Isso resultou na criação de bibliotecas como JQuery, Prototype, Dojo, etc.

O Google lançou o navegador Chrome com o mecanismo JavaScript V8 em 2008. No início de 2009, foi feito um acordo para combinar todo o trabalho relevante e impulsionar o JavaScript. Isso resultou no lançamento do ECMAScript 5 Standard em dezembro de 2009.

## Como usar arquivos JS ##

Para usar um arquivo JS, inclua-o no documento HTML. Você usa a tag de link para incluir o arquivo conforme mostrado abaixo.

```html
<script src="site.js"></script>
```

O atributo *src* da tag *script* contém o caminho para o arquivo JS. Ao fazer isso, a funcionalidade JS é adicionada ao documento HTML.

## Sintaxe JS ##

Arquivos JavaScript podem conter variáveis, operadores, funções, condições, loops, arrays, objetos, etc. Abaixo está uma breve visão geral da sintaxe do JavaScript.

- Cada comando termina com um ponto e vírgula(;).
- Use a palavra-chave *var* para declarar variáveis.
- Suporta operadores aritméticos ( + - * / ) para calcular valores.
- Comentários de linha única são adicionados com // e comentários de várias linhas são cercados por /* e */.
- Todos os identificadores diferenciam maiúsculas de minúsculas, ou seja, *modelNo* e *modelno* são duas variáveis diferentes.
- As funções são definidas usando a palavra-chave *function*.
- Arrays podem ser definidos usando colchetes [].
- JS suporta operadores de comparação como ==, != , >=, !==, etc.
- As classes podem ser definidas usando a palavra-chave *class*.

## Exemplo de uso de JS ##

Veja a seguir um arquivo JavaScript de exemplo de uso simples.

### Documento HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Test</title>
    <script src="main.js"></script>
</head>

<body>
    <div class="content-wrapper">
        <h1 id="heading">Test document for JS testing</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

            <button type="button" onclick="showAlert()">Show Alert</button>
            <button type="button" onclick="updateHeading()">Update Heading</button>
    </div>
</body>

</html>
```

### Código JS ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Referências ##

- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

