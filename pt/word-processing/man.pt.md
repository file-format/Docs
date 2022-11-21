{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - Manual Unix",
  "description":"Saiba mais sobre o formato de arquivo FODT e APIs que podem criar e abrir arquivos MAN.",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## O que é um arquivo MAN?

Um arquivo com extensão .man significa man page que é um manual do usuário de programação Unix em forma de documentação de software. Ele é usado pelo utilitário `Man`, incluído no Unix, que é usado para visualizar a documentação. A documentação do software contém informações em seções e páginas que podem ser recuperadas usando o utilitário Man do terminal de comando emitindo comandos. Estando disponível no computador como cópia eletrônica da documentação, não requer qualquer cópia impressa ou conexão com a internet para acessá-la.

## Formato de arquivo manual do Unix - Mais informações

As páginas de manual são armazenadas em formato de texto simples e podem ser criadas e abertas em qualquer editor de texto para visualização ou edição. No UNIX, as informações das páginas Man são recuperadas emitindo comandos do terminal que incluem referência aos números de seção e página do manual.

### Seções e páginas

Unix man é o manual do sistema onde cada argumento de página para o comando se refere ao nome de um programa, utilitário ou função. o comando, se fornecido com informações de seção, procurará a página nessa seção específica. No entanto, o comportamento padrão é pesquisar a página em todas as seções e exibir a primeira página, independentemente de existir em várias seções.

### Números de seção

A seguir estão as informações sobre os números das seções do manual seguidos pelos tipos de páginas que eles contêm.

|Número da seção|Tipo de páginas|
---|---|
|1|Programas executáveis ou comandos shell|
|2|Chamadas do sistema (funções fornecidas pelo kernel)|
|3|Chamadas de biblioteca (funções dentro de bibliotecas de programa)|
|4|Arquivos especiais (geralmente encontrados em /dev)|
|5|Formatos de arquivo e convenções, por exemplo, /etc/passwd|
|6|Jogos|
|7|Diversos (incluindo pacotes de macro e convenções), por exemplo, man(7), groff(7)|
|8|Comandos de administração do sistema (geralmente apenas para root)|
|9|Rotinas do kernel [Não padrão]|

## Exemplo - Como Ler Páginas MAN?

Aqui está um exemplo de como recuperar informações sobre o comando MkDir usando o comando Man.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## Referências

* [Especificações técnicas do OpenDocument - Por Wikipedia](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) — página de manual do Linux](https://man7.org/linux/man-pages/man1/man.1.html)

