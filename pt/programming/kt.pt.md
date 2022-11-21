---
date: 2019-10-11
keywords: kt, .kt, formato de arquivo kotlin, como abrir arquivos kotlin, como executar arquivos kotlin, formato de arquivo .kt, arquivo kt , extensão de arquivo kotlin, extensão .kt, kotlin vs java
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de arquivo KT
linktitle: KT
description: "Saiba mais sobre o formato de arquivo KT e APIs que podem criar e abrir arquivos KT."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## O que é um arquivo KT? ##

Um código-fonte escrito em Kotlin é salvo com a extensão .kt que é comumente conhecida como **extensão de arquivo Kotlin**. O Kotlin é uma linguagem de programação multiplataforma de propósito geral desenvolvida pela JetBrains para ser totalmente interoperável com [Java](/pt/programming/java/). A marca Kotlin é protegida pela Kotlin Foundation.

Kotlin foi anunciado como a linguagem de programação preferida para o desenvolvimento de aplicativos Android pelo Google em 7 de maio de 2019. O Android Studio 3.0 começou a oferecer suporte ao Kotlin como uma alternativa para o desenvolvimento de aplicativos Android em outubro de 2017.

## Breve história do formato de arquivo Kotlin KT##

Kotlin foi revelado pela JetBrains em julho de 2011 como uma nova linguagem de programação para JVM. O líder da JetBrains, Dmitry Jemerov, disse que a maioria das linguagens estava faltando recursos que eles estavam procurando, exceto Scala, mas a lenta compilação do Scala era uma desvantagem. Um dos principais objetivos do Kotlin era compilar tão rapidamente quanto o Java. O projeto Kotlin foi open-source sob a licença Apache 2 em fevereiro de 2012.

A versão 1.0 do Kotlin foi lançada em 15 de fevereiro de 2015. O Android anunciou suporte de primeira classe para Kotlin no Android no Google I/O 2017. Kotlin 1.2 foi lançado em 28 de novembro de 2017 com a capacidade de compartilhar código entre plataformas JVM e JavaScript. Kotlin 1.3 foi lançado em 29 de outubro de 2018 com suporte para programação assíncrona. O Google anunciou o Kotlin como a linguagem de programação preferida para o desenvolvimento de aplicativos Android em 7 de maio de 2019. O Kotlin 1.4 foi lançado em agosto de 2020 com algumas pequenas alterações para oferecer suporte à interoperabilidade com Swift/Objective-C.

## Sintaxe Kotlin ##

O Kotlin foi projetado para ser melhor que o Java, mas ainda ser interoperável com o código Java para permitir a migração gradual do Java para o Kotlin.

* Os pontos e vírgulas são opcionais em Kotlin. Uma nova linha é suficiente para indicar o fim da instrução.
* Kotlin suporta dois tipos de variáveis, somente leitura, definidas pela palavra-chave *val*, e mutáveis, definidas pela palavra-chave *var*.
* As aulas são privadas e finais por padrão. Para derivar de uma classe, a classe base deve ser declarada com a palavra-chave *open*.
* Kotlin também suporta programação procedural.
* O ponto de entrada para o programa Kotlin é a função "principal" semelhante a Java, C#, etc.

### Exemplo de sintaxe ###

Veja a seguir um exemplo de sintaxe Kotlin.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

No código acima, a palavra-chave **fun** define a função chamada main. Dentro da função, uma variável somente leitura 'audience' é declarada com a palavra-chave **val**. Usando o método **println**, "Hello World from Kotlin" é impresso no console. O valor da variável audiência é injetado na string com o sinal **$**.

## Kotlin vs Java
O Kotlin é uma linguagem oficial para escrever aplicativos Android com muitos recursos avançados, mas muitos desenvolvedores especialistas em Java ainda não demonstraram interesse em mudar para o Kotlin. Eles pensam que podem fazer tudo apenas com Java. Então a seguir está a comparação entre duas tecnologias que podem convencer os desenvolvedores java a mudar:

| Parâmetro | Java | Kotlin |
|--------------------|-----------|---------------- -|
| Objetos Singletons | √ | √ |
| Tipos curinga | √ | Χ |
| Compilação | Bytecodes | Máquina Virtual |
| Expressão Lambda | Χ | √ |
| Matriz invariável | Χ | √ |
| Campos não privados | √ | Χ |
| Elencos Inteligentes | Χ | √ |
| Nulo Segurança | Χ | √ |
| Membros estáticos | √ | Χ |

## Referências ##

- [Kotlin (linguagem de programação) - Wikipedia](https://en.wikipedia.org/wiki/Kotlin_(programming_language))

