---
date: 2022-05-09
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Formato de arquivo PYM - Arquivo de pré-processador de macro PYM
linktitle: PYM
description: "Saiba mais sobre o formato de arquivo PYM e APIs que podem criar e abrir arquivos PYM."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## O que é um arquivo PYM?

Um arquivo PYM é um arquivo de pré-processador de macro baseado na linguagem de programação Python. Foi desenvolvido pela VRVis Research e armazena atalhos de macro. Quando o arquivo PYM é interpretado pelo estágio de pré-processamento do interpretador Python, esses atalhos são expandidos como substitutos do texto completo. Além disso, uma terceira operação opcional que pode ser executada por um pré-processador de macro é a inclusão de arquivos. Os arquivos PYM podem ser abertos em editores de texto como Notepad, Notepad++, Apple TextEdit e VI no Linux.

## Formato de arquivo PYM

Os arquivos PYM são salvos como arquivos de texto simples no disco. Um arquivo PYM também pode incluir outros arquivos usando a diretiva `#include`.

### Sintaxe PYM

As instruções PYM são incluídas entre os marcadores ""#begin python e "#end python", conforme mostrado abaixo.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### Expansão da Macro PYM

A expansão da macro PYM é representada por duas sequências, ou seja, <[ e ]>. Estas são tags html especiais e podem aparecer em qualquer lugar em uma linha. Um pequeno exemplo de PYM é o seguinte.

```
#begin python
TITLE = "My Web page"
def EXP(e): return str(e)
#end python
<head>
<title><[TITLE]></title>
</head>
<body>
<h4><[TITLE]></h4>
<p>The value of 2 raised to the 4th power is <[EXP(2**4)]>.</p>
</body>
```

A saída de executar isso através do PYM é a seguinte:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Referências ##

* [PYM - Um pré-processador de macro baseado em Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [Intérpretes PYM](https://github.com/interpreters/pym)

