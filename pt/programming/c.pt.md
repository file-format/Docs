{
  "date" : "2020-01-10",
  "keywords" :[ "c", ".c", "o que é arquivo ac", "como abrir arquivo c", "extensão", "arquivo", "arquivo c", "formato de arquivo c", "extensão de arquivo c"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo de programação em linguagem C - C",
  "description":"Saiba mais sobre o formato de arquivo C e APIs que podem criar e abrir arquivos C.",
  "linktitle" : "C",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-01-10"
}

## O que é um arquivo C?

Um arquivo salvo com extensão de arquivo c é um arquivo de código-fonte escrito em linguagem de programação C. O **arquivo C** inclui toda a implementação da funcionalidade do aplicativo na forma de código-fonte. A declaração do código fonte é escrita nos arquivos de cabeçalho que são salvos com extensão [.h](/pt/programming/h/). C++ é a forma moderna da linguagem C e é usada para desenvolver a maioria dos softwares hoje em dia.

## Breve história

A linguagem C surgiu como resultado da criação de diferentes utilitários para o sistema operacional UNIX. Denis Ritchie, o homem por trás da criação desta linguagem de programação, o trabalho começou originalmente nos anos 1960 e início dos anos 1970.

## Formato de arquivo C

Os arquivos C são escritos em formato de arquivo de texto simples seguindo a sintaxe da linguagem de programação. Um arquivo C típico terá:

* declaração de importação na parte superior do arquivo para importar qualquer arquivo de cabeçalho
* um ou mais métodos para implementar a funcionalidade desejada

### Importação de cabeçalhos

Os arquivos de cabeçalho, com extensão .h, contêm instruções de inclusão necessárias para incluir outros arquivos de funcionalidade no projeto. Além disso, eles contêm as declarações de métodos definidos no arquivo de implementação. Os arquivos de cabeçalho são incluídos usando a instrução include, conforme mostrado abaixo.

```
#include <filename.h>
```

### Implementação do código-fonte

A implementação real dos requisitos funcionais é codificada como métodos no arquivo C. Cada método em um arquivo C tem um tipo de retorno, nome de método e pode ter alguns parâmetros de entrada. Se o tipo de retorno não for void, o método pode estar retornando algum valor.

### Exemplo de código C
Aqui está um programa de exemplo:

```
long some_function();
/* int */ other_function();

/* int */ calling_function()
{
    long test1;
    register /* int */ test2;

    test1 = some_function();
    if (test1 > 0)
          test2 = 0;
    else
          test2 = other_function();
    return test2;
}
```



## **Referências** ##

* [Implementação de classe - pela Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)

