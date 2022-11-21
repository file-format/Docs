---
date: 2019-10-11
keywords: scss, .scss, formato de arquivo scss, como abrir arquivos scss, folha de estilo sintaticamente incrível, pré-processador css, sass
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de arquivo SCSS - Folha de estilos em cascata Sass
linktitle: SCSS
description: "Saiba mais sobre o formato de arquivo SCSS e APIs que podem criar e abrir arquivos SCSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## O que é um arquivo SCSS? ##

SCSS é a segunda sintaxe do Sass (Syntactically Awesome Stylesheet) que usa colchetes em vez de recuos. O SCSS foi projetado de forma que um arquivo CSS3 válido também seja um arquivo SCSS válido. Os arquivos SCSS são armazenados com a extensão .scss.

## Por que usar SCSS ##

Como os designs dos sites estão se tornando complexos, resultando em grandes arquivos [CSS](/pt/web/css/). Esses arquivos são mais difíceis de manter. É aí que entra o SCSS. O SCSS introduz variáveis, aninhamento, mixins, importações e herança de seletor no desenvolvimento de CSS. Essas adições tornam o trabalho com design muito mais divertido.

## Como usar arquivos SCSS ##

Os arquivos SCSS não são incluídos diretamente no documento [HTML](/pt/web/html/) como CSS. Em vez disso, os arquivos SCSS são convertidos em arquivos CSS incluídos em arquivos HTML. Para instalar o SCSS em seu sistema, siga as instruções fornecidas no [Official Sass Site](https://sass-lang.com/install).
Para converter SCSS para CSS, você pode converter um arquivo SCSS já salvo ou observar as alterações e converter à medida que o arquivo é salvo. Os comandos para ambos são fornecidos abaixo.

### Converter uma vez ###

O primeiro parâmetro é o arquivo SCSS de origem e o segundo parâmetro é o arquivo CSS de saída.

```cmd
sass main.scss main.css
```

### Fique atento às alterações ###

O comando tem um sinalizador adicional *watch** que mantém o comando em execução e assim que o arquivo SCSS é salvo, o CSS de saída é gerado.

```cmd
sass --watch main.scss main.css
```

## Sintaxe SCSS ##

O SCSS suporta variáveis, aninhamento, mixins, importações, herança de seletor, etc. Abaixo estão alguns exemplos desses recursos.

### Variáveis ###

Com o uso de variáveis, você pode definir informações reutilizáveis, como cor primária ou cor de fundo para o botão salvar. Isso é útil se você precisar alterar essas informações, basta alterá-las em um local e elas são atualizadas onde quer que sejam usadas.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

Você pode aninhar os seletores CSS de forma semelhante à hierarquia do HTML. No exemplo dado abaixo, o span está aninhado dentro do bloco h1.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

Mixins podem ser usados para agrupar propriedades semelhantes que são usadas juntas em vários lugares. Você também pode passar parâmetros para mixins.

**SCSS**

**Declarando uma mixagem**

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

**Usando uma mixagem**

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
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

Estender/Herança é útil nos casos em que as propriedades de um seletor precisam ser compartilhadas com outro seletor. No exemplo abaixo, o seletor *.error-notice* pega todas as propriedades do seletor *.error-text* e adiciona propriedades de borda e preenchimento.

**SCSS**

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
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

A importação pode ser útil na separação de interesses. Você pode dividir os estilos de forma que os estilos de cabeçalho fiquem em um arquivo separado, os estilos de rodapé estejam em um arquivo separado, todas as variáveis de cores usadas nos estilos possam estar em um arquivo separado, etc. estilos permanecem organizados. Você apenas importa os arquivos em seu arquivo SCSS principal, conforme mostrado no exemplo abaixo. Você não precisa especificar a extensão do arquivo na instrução de importação. Sass compila todos os arquivos SCSS diretamente. Para evitar que os arquivos de importação sejam compilados diretamente, você pode torná-los parciais adicionando underscore(_) antes de seu nome. Você pode importar parciais semelhantes aos arquivos SCSS normais sem o sublinhado.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

O CSS de saída terá os estilos de todos os arquivos importados.

## Referências ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

