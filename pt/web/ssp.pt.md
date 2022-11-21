---
date: 2021-07-05
keywords: ssp, .ssp, formato de arquivo ssp, como abrir arquivos ssp, Scala Server Page
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP - Formato de arquivo Scala Server Pages
linktitle: SSP
description: "Saiba mais sobre o que é um formato de arquivo SSP e APIs que podem criar e abrir arquivos SSP."
menu:
  docs:
    identifier: "web-ssp"
    parent: "web"
lastmod: 2021-09-30
---

## O que é um arquivo SSP?

Um arquivo com extensão .ssp é uma página da Web criada com código Scala para expressões em vez de apenas HTML simples. Ele atua como um script do lado do servidor usando a combinação de HTML e Scala. Esses arquivos residem no servidor e são usados para criar páginas da Web estáticas para serem veiculadas aos usuários. O próprio Scala é uma linguagem de programação de uso geral cuja sintaxe é familiar para usuários que trabalharam com Velocity, JSP ou Erb. Os arquivos SSP podem ser analisados e avaliados usando [Scalate](https://scalate.github.io/scalate/), que é um mecanismo de modelo baseado em Scala para gerar texto e marcação.

## Formato de arquivo SSP - Mais informações

Os arquivos SSP são salvos em arquivo de texto simples e podem ser avaliados usando Scalate. Um modelo Ssp consiste em texto simples que é mais frequentemente o documento HTML. Ele possui tags Ssp incorporadas que fazem com que os mecanismos de renderização renderizem diferentes partes do documento dinamicamente. As tags começam e terminam com a sequência <% ... %> e ${ ... } e qualquer coisa fora delas é considerada como texto literal.

### Exemplo SSP

O exemplo a seguir mostra o código SSP e sua saída quando ele é renderizado pelo mecanismo de renderização.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
A saída é a seguinte.
```
<p>
  hi there reader!
  yo 7
</p>
```

## Referências

- [Referência SSP](https://scalate.github.io/scalate/documentation/ssp-reference.html)

