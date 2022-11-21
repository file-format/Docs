---
date: 2019-10-11
keywords: java, .java, formato de arquivo java, como abrir arquivos java, como executar arquivos java, arquivo java, código de amostra java
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de arquivo Java
linktitle: Java
description: "Saiba mais sobre o formato de arquivo Java e as APIs que podem criar e abrir arquivos Java."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## O que é um arquivo Java? ##
Um arquivo contendo código-fonte Java e salvo com extensão de arquivo .java é conhecido como arquivo Java. O Java é uma das tecnologias mais utilizadas para o desenvolvimento de jogos, aplicativos mobile, web e desktop. Como o Java é independente de plataforma, ele funciona perfeitamente no Windows, Mac, Linux, Raspberry Pi, etc. O Java é muito semelhante ao C# e C++, por isso é mais fácil alternar entre essas linguagens.

## Breve história ##

O projeto Java foi iniciado em junho de 1991 por James Gosling, Mike Sheridan e Patrick Naughton. Java foi inicialmente chamado Oak. Mais tarde, foi renomeado para Green e, finalmente, para Java. James Gosling projetou Java com uma sintaxe similar a C/C++. A primeira versão pública do Java foi lançada em 1996 pela Sun Microsystems. Ele pode ser executado em todos os sistemas populares que fizeram com que o Java se tornasse popular rapidamente. Com o lançamento do Java 2 em dezembro de 1998, várias configurações para diferentes tipos de plataformas foram construídas. As versões foram as seguintes

- J2EE (Java EE): Para soluções empresariais
- J2ME (Java ME): Para aplicativos móveis
- J2SE (Java SE): Para aplicativos de desktop

Em 19 de novembro de 2006, a Java Virtual Machine (JVM) foi lançada pela Sun como software livre e de código aberto. Depois que a Oracle Corporation adquiriu a Sun Microsystems em 2009–2010, James Gosling renunciou à Oracle em 2 de abril de 2010.

## Como executar/executar código Java ##

Para executar o código Java, ele precisa ser compilado primeiro. Para isso, o Java SDK é necessário. O Java SDK compila o código Java em um arquivo de classe de bytecode. Existem IDEs como Eclipse e IntelliJ Idea que facilitam o trabalho com arquivos Java fornecendo preenchimento de código e interface fácil de usar para compilar e executar o código Java.

## Formato de arquivo Java ##

A sintaxe de Java foi altamente influenciada por C e C++, mas diferentemente de C++, Java foi construída quase exclusivamente como uma linguagem orientada a objetos. Em Java, todo o código é escrito dentro de classes e cada item de dados é um objeto. Em contraste com C++, Java não suporta sobrecarga de operadores ou herança múltipla.

### Código de exemplo Java ###

Veja a seguir um exemplo de sintaxe Java.

```java
/*
The example code prints
Hello World from Java to the console.
*/
    public class ExampleApp {
        public static void main(String[] args) {
            System.out.println("Hello World from Java"); // Prints the string to the console.
        }
    }
```
No código acima, a palavra-chave **public** denota o modificador de acesso. Ele afirma que esta classe pode ser acessada pelas classes fora da hierarquia de classes. O modificador de acesso também pode ser **protegido** (pode ser acessado no mesmo pacote) ou **privado** (os métodos só podem ser acessados pela mesma classe). O **static** na frente do método indica que o método pode ser invocado sem uma instância específica da classe. O **void** indica que o método não retornaria nada. Para imprimir a string no console. O comando System.out.println é usado. Neste comando, a classe *System* tem um campo estático *out* que é uma instância da classe *PrintStream* que contém o método *println*.

O nome do arquivo dos arquivos Java deve ser o mesmo que o nome da classe. Assim, o arquivo Java para o código de exemplo seria denominado *ExampleApp.java*.

## Referências ##

- [Java (linguagem de programação) - Wikipedia](https://en.wikipedia.org/wiki/Java_(programming_language))

