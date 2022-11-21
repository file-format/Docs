{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M - Arquivo de código-fonte Matlab",
  "description":"Saiba mais sobre o arquivo de código-fonte Matlab .m e APIs que podem criar e abrir arquivos MF.",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

# M - Arquivos de código-fonte do Matlab

## O que é um arquivo M (Matlab)?

Um arquivo com extensão .m é um arquivo de código-fonte usado pelo Matlab, uma plataforma de programação e computação numérica usada para análise, desenvolvimento de algoritmos e modelagem de simulação. Como outros formatos de arquivo de programação, um arquivo M contém código-fonte que executa comandos do Matlab para plotar gráficos, executar simulações e outras operações matemáticas. Uma única simulação Matlab pode abranger vários arquivos .m que podem classificar o aplicativo em scripts, classes, funções ou declarações. Os arquivos Matlab M podem ser abertos com qualquer editor de texto.

## Formato de arquivo Matlab M - Mais informações

Os arquivos Matlab .m são arquivos de texto que contêm código de programação na linguagem de programação Matlab. Estes podem ser abertos e editados em qualquer editor de texto e salvos novamente para serem executados no software Matlab. O próprio Matlab contém um Live Editor que é usado para criar scripts que são uma combinação de código, saída e texto formatado.

### Arquivos de função do Matlab

Como outras linguagens de programação, você pode criar um arquivo .m que contém apenas a definição de uma função que executa apenas uma tarefa específica. Esses arquivos também são salvos com extensão .m e implementam a funcionalidade relacionada apenas a essa função.

### Exemplo de arquivo .M

A seguir está um exemplo de arquivo de função do Matlab que calcula o tempo gasto para um objeto cair da altura h.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

Para chamar esta função do editor Matlab ou de outro arquivo .m, o código a seguir pode ser usado.
```C++
TimeToGround(100)
```

## Referências

* [Matlab - Formatos de arquivo compatíveis](https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [Usando Matlab](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - Arquivo de Implementação Objective-C

## O que é um arquivo M (Objective-C)?

Um arquivo M também é chamado de arquivo de implementação que contém o código-fonte de uma classe escrita em linguagem Objective-C, uma linguagem de programação usada para escrever aplicativos de software para OS X e iOS. Objective-C é a principal linguagem de programação usada pelas principais APIs da Apple, Cocoa e Cocoa Touch, para essas plataformas. Um único aplicativo de software desenvolvido nesta linguagem pode conter vários arquivos .m, contendo a implementação das classes do programa. Eles podem ser abertos usando o Apple XCode, jEdit e outros editores de texto comuns.

## Formato de arquivo Objective-C M - Mais informações

Os arquivos M são escritos em formato de texto simples usando a sintaxe de programação do Objective-C. Cada método de uma classe deve ser definido com todo o seu código necessário nesses arquivos de implementação. Esses arquivos M de implementação podem importar um ou mais arquivos de cabeçalho .h conforme os requisitos. A instrução de importação informa ao compilador onde encontrar o arquivo de cabeçalho que pertence a esse arquivo de implementação. A instrução de importação é escrita da seguinte forma.

```C++
#import "network.h"
```

Cada implementação de arquivo M começa com a diretiva `@implementation`, seguida pelo nome do arquivo da classe de implementação. Isso é seguido por todas as implementações de métodos que são declaradas no arquivo de cabeçalho.

### Exemplo de formato de arquivo M

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## Referências
* [Sobre o Objective C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [Guia Object-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

