---
date: 2019-10-11
keywords: dart, .dart, formato de arquivo dart, arquivo dart, como executar arquivos dart, extensão .dart
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de arquivo de dardo
linktitle: Dart
description: "Saiba mais sobre o formato de arquivo Dart e as APIs que podem criar e abrir arquivos Dart."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## O que é um arquivo Dart? ##

Um arquivo Dart contém o código-fonte da linguagem de programação Dart, que é uma linguagem de programação otimizada para cliente desenvolvida pelo Google que é usada para criar aplicativos para dispositivos móveis, desktop, web, Iot (Internet das coisas) etc. Dart é uma linguagem orientada a objetos com uma sintaxe semelhante a C. O Dart pode ser compilado para JavaScript ou código nativo. Você pode executar os arquivos Dart no famoso navegador da web, assim como você pode executar um arquivo javascript. Uma ferramenta de linha de comando conhecida como máquina virtual Dart que vem com o Dart SDK também é usada para compilar e executar os arquivos Dart.

## Breve história ##

O projeto Dart foi fundado por Lars Bak e Kasper Lund e a primeira versão foi lançada em 14 de novembro de 2013. No início o Dart foi criticado pela fragmentação da web devido aos planos de incluir uma VM Dart no Google Chrome. Esses planos foram abandonados e o Dart se concentrou em compilar para JavaScript com o lançamento da versão 1.9 em 2015.

O Dart 2.0 foi lançado em agosto de 2018, no qual foi introduzida a extensão dart2native que compilava o código Dart para plataformas nativas Linux, Windows e macOS. Essa extensão permitia executáveis autônomos devido aos quais o SDK do Dart não era necessário para executar aplicativos Dart nessas plataformas. Essa extensão também se integrou ao Flutter, possibilitando a criação de aplicativos multiplataforma.

A ECMA padronizou o Dart com a primeira edição em julho de 2014 e a segunda edição em dezembro de 2014.


## Como executar/executar código Dart ##

O código Dart pode ser executado das seguintes maneiras:

- **Compilado como JavaScript**:</br> O código Dart é compilado para JavaScript usando o compilador dart2js. O código JavaScript compilado é compatível com todos os principais navegadores da web.
- **Estar sozinho**:</br> O Dart Software Development Kit (SDK) é fornecido com uma VM Dart autônoma que permite que o código Dart seja executado na interface de linha de comando. O Dart é fornecido com uma biblioteca padrão completa que permite aos usuários escrever aplicativos totalmente funcionais.
- **Compilação antecipada (AOT)**:</br> O código Dart pode ser compilado AOT em código de máquina que permite que aplicativos móveis sejam criados com o Flutter.
- **Nativo**:</br> Com o compilador dart2native, o código Dart pode ser compilado em executáveis independentes que podem ser executados no Windows, Linux e macOS.

## Formato de arquivo Dart ##

Dart é uma linguagem orientada a objetos no estilo C que suporta interfaces, mixins, classes abstratas, genéricos reificados e interface de tipo.

### Sintaxe ###

A seguir estão alguns exemplos de sintaxe do Dart.

#### Imprimir para o console ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### Loops e Arrays ####

```dart
// loops and arrays
var names = {
  'John',
  'James',
  'Rose',
};
main() {
  for (var name in names) {
    print(name);
  }
}
```

#### Funções ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### Aulas ####

```dart
// classes
abstract class Person {
  detail();
}

class Student implements Person {
  String firstName = "Jack";
  String lastName = "Wick";
  detail() => print("Student: $firstName $lastName");
}

main() {
  // The 'new' keyword is optional.
  Student student = Student();
  student.detail();
}
```

#### Misturas ####

Mixins são classes normais das quais podemos emprestar métodos/variáveis sem herdá-los. Isso é feito usando a palavra-chave *"with"*.

```dart
class B {  
  method(){
     ....
  }
}

class A with B {
  ....
     ......
}
void main() {
  A a = A();
  a.method();  //We are able to access the method of B class without inheriting from it.
}
```

## Referências ##

- [Dart (linguagem de programação) - Wikipedia](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [Dart](https://dart.dev/)

