{
  "date" : "2019-10-11",
  "keywords" :[ "c++", "arquivo", "extensão", "formato de arquivo", "C++", "Linguagem de programação" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPP - Arquivo de código-fonte C++",
  "description":"Saiba mais sobre o formato de arquivo CPP e as APIs que podem criar e abrir arquivos CPP.",
  "linktitle" : "CPP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo C++?

Arquivos com extensão de arquivo CPP são arquivos de código-fonte para aplicativos escritos em linguagem de programação C++. Um único projeto C++ pode conter mais de um arquivo CPP como código-fonte do aplicativo. Tal projeto consiste em diferentes tipos de arquivos, dos quais os arquivos CPP são conhecidos como arquivos de implementação, pois contêm todas as definições dos métodos declarados no arquivo de cabeçalho (.h). O projeto C++ como um todo resulta em um aplicativo executável quando compilado como um todo.

## Estrutura do arquivo CPP

Uma estrutura de arquivo CPP é simples em comparação com os arquivos de cabeçalho. O objetivo principal de tal arquivo de implementação é dividir a interface da implementação. Isso resulta em declarações de todas as funções de membro em um arquivo de cabeçalho e seus detalhes dentro do arquivo CPP. Um arquivo de implementação CPP pode ser usado como um arquivo simples para escrever um aplicativo ou como uma implementação de classe.

### Implementação Independente

Um arquivo CPP quando usado como uma aplicação independente pode conter todas as implementações dentro dele sem a exigência de declaração de métodos no arquivo de cabeçalho. Tal implementação consiste em todos os métodos definidos no arquivo de implementação onde a entrada do aplicativo é governada por um método principal que recebe entradas opcionais do usuário como argumentos. Ele também pode incluir qualquer biblioteca da Biblioteca Padrão C++ para ser usada por qualquer método declarado no arquivo.

```
/*
* File: main.cpp
* Author: SomeOne
* Created on November 16, 2018, 4:09 PM
*/

#include <iostream>
using namespace std;

int main()
{
   cout<<"About the CPP file format";
   cout<<std::endl<<"and its very easy";
}
```

### Implementação de classe

Na Programação Orientada a Objetos (OOP), um arquivo CPP é usado como uma definição de classe. Nesse caso, todos os membros de dados de classe e funções de membro são declarados dentro do arquivo de cabeçalho. Cada arquivo de cabeçalho pode, por sua vez, ter referência a métodos de biblioteca padrão. O arquivo CPP de definição de classe refere-se ao arquivo de cabeçalho em uma instrução de inclusão no início do arquivo. Principalmente, os desenvolvedores de software incluem comentários no início de tal arquivo de implementação de classe que fornecem informações sobre o conteúdo real do arquivo, detalhes do autor e a data de implementação. Nesses casos, os arquivos de implementação de cabeçalho devem ter os mesmos nomes. Um exemplo de tal arquivo de cabeçalho e implementação é o seguinte.

### Arquivo de cabeçalho

```
#include <string>
#include <iostream>

using namespace std;

class MyClass {
public:
   MyClass();     // Constructor
   void add(int i, int j);

private:
   std::string name;
};
```

### Arquivo de Implementação CPP

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## Referências

* [Implementação de classe - pela Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)

