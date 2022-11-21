---
date: 2019-10-11
keywords: sass, .sass, formato de arquivo sass, como abrir arquivos sass, folha de estilo sintaticamente incrível, pré-processador css, sass
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de arquivo Sass
linktitle: Sass
description: "Saiba mais sobre o formato de arquivo Sass e APIs que podem criar e abrir arquivos Sass."
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## O que é um arquivo SASS? ##

Sass (folhas de estilo sintaticamente impressionantes) é uma linguagem de script de pré-processador. Ele é compilado em [CSS](/pt/web/css/) e é armazenado com a extensão .sass. Sass consiste em duas sintaxes, a original baseada em recuos que usa a extensão .sass e a SCSS mais recente com formatação de bloco como CSS que usa a extensão .scss.

## Por que usar Sass ##

O Sass é realmente útil na manutenção de estilos, pois fornece muitos recursos, como introdução de variáveis, aninhamento, mixins, importações e herança de seletores que tornam o trabalho com estilos divertido.

## Como usar arquivos SASS ##

Os arquivos SASS não são incluídos diretamente no documento [HTML](/pt/web/html/), mas são convertidos em arquivos CSS incluídos nos arquivos HTML. Você pode instalar o Sass em seu sistema seguindo as instruções fornecidas no [Site Oficial do Sass](https://sass-lang.com/install).

O Sass pode ser convertido em CSS convertendo um arquivo SASS já salvo ou observando as alterações e convertendo à medida que o arquivo é salvo. Os comandos para ambos são fornecidos abaixo.

### Converter uma vez ###

O primeiro parâmetro do comando é o arquivo SASS de origem e o segundo parâmetro é o arquivo CSS de saída.

```cmd
sass main.sass main.css
```

### Fique atento às alterações ###

O comando acima pode ser executado com um sinalizador adicional *watch* que mantém o comando em execução e assim que o arquivo Sass é salvo, o CSS de saída é gerado.

```cmd
sass --watch main.sass main.css
```

## Sintaxe Sass ##

O Sass suporta variáveis, aninhamento, mixins, importações, herança de seletores, etc. Abaixo estão alguns exemplos desses recursos.

### Variáveis ###

As variáveis podem ser usadas para definir informações reutilizáveis, como cor primária ou preenchimento para um botão. Isso pode ser útil se, no futuro, você precisar alterar essas informações, basta alterá-las em um local e elas são atualizadas em todos os lugares.

**Sass**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**CSS gerado**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Aninhamento ###

Os seletores CSS podem ser aninhados de maneira semelhante à hierarquia do HTML. No exemplo a seguir, o intervalo está aninhado dentro do bloco h1.

**Sass**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**CSS gerado**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Misturas ###

Mixins são usados para agrupar propriedades semelhantes que são usadas em vários lugares. Mixins também suportam parâmetros.

**Sass**

**Declarando uma mixagem**

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

**Usando uma mixagem**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
```

**CSS gerado**

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

### Ampliar ###

Estender/Herança pode ser útil nos casos em que as propriedades de um seletor precisam ser compartilhadas com outro seletor. No exemplo abaixo, o seletor *.error-notice* pega todas as propriedades do seletor *.error-text* e adiciona propriedades de borda e preenchimento.

**Sass**

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
```

**CSS gerado**

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

### Importar ###

A importação pode ser útil se você estruturar seus estilos em arquivos diferentes com base na funcionalidade ou em qualquer outra estrutura que você seguir. Você pode importar todos esses arquivos em um arquivo SASS primário que é posteriormente convertido em CSS. Durante a importação, você não precisa especificar a extensão do arquivo na instrução de importação. Sass compila todos os arquivos SASS diretamente. Para evitar que arquivos de importação sejam compilados diretamente, você pode torná-los parciais adicionando underscore(_) no início de seu nome. Parciais são importados de forma semelhante aos arquivos Sass normais.

**Sass**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

O CSS de saída terá os estilos de todos os arquivos importados.

## Referências ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

