{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Make File - Xcode Makefile Script File",
  "description":"Saiba mais sobre o formato XCode MakeFile e APIs que podem criar e abrir arquivos MakeFile.",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## O que é um arquivo MAKE?

Um arquivo MAKE é um arquivo de script XCode que organiza a compilação de código. Ele é usado para compilar e vincular programas de vários arquivos de código-fonte. Essa ajuda a decidir quais partes de um aplicativo grande precisam ser recompiladas quando o aplicativo precisar ser atualizado. Faça com que os arquivos usem uma série de instruções para serem executados, dependendo de quais arquivos foram alterados.

## Exemplo de formato de arquivo MAKE

O conteúdo a seguir é executado usando o utilitário Make e as saídas são as seguintes.

```
hello:
	echo "hello world"
```
**Fazer saída**

```
$ make
echo "hello world"
hello world
```

## Referências
* [XCode and Make - Apple Forums](https://developer.apple.com/forums/thread/657458)
* [Guia Object-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

