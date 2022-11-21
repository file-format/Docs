{
  "date" : "2019-10-11",
  "keywords": [ "mf file", "mf", "extension", "format", "mf file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MF - Formato de arquivo de manifesto Java",
  "description":"Saiba mais sobre o formato de arquivo MF e APIs que podem criar e abrir arquivos MF.",
  "linktitle" : "MF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## O que é um arquivo MF?

Um arquivo com extensão .mf é um arquivo de Manifesto Java que contém informações sobre as entradas individuais do arquivo [JAR](/pt/programming/jar/). O próprio arquivo MF está contido no arquivo JAR e fornece toda a extensão e definição relacionada ao pacote. Os arquivos JAR podem ser produzidos para serem usados como um arquivo executável. Nesse caso, o arquivo mainfest especifica a classe principal do aplicativo que contém a instrução **`public static void main`**. Os arquivos de manifesto são nomeados como MANIFEST.MF e podem ser abertos com qualquer editor de texto nos sistemas operacionais Windows, MacOS e Linux.

## Especificações de formato de arquivo de manifesto

[Especificações de formato de arquivo de manifesto](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) estão disponíveis pela Oracle em seu guia para formato de arquivo JAR. Um arquivo de manifesto é composto por seções principais que são seguidas por uma lista de seções para entradas de arquivos JAR individuais. Cada seção segue algumas regras e restrições.

### Seções principais

Uma seção principal:

* contém informações sobre segurança e configuração do arquivo JAR
* contém informações sobre o aplicativo ou extensão do qual o arquivo JAR faz parte
* define os principais atributos para cada item de manifesto individual

**Observação**: Nenhum atributo nesta seção pode ser denominado "Nome".

### Seções individuais

Uma seção individual define vários atributos para pacotes ou arquivos de um arquivo JAR. Cada seção deve começar com um atributo chamado "Nome" cujo valor deve ser um caminho relativo para o arquivo ou um URL absoluto que faça referência a dados fora do arquivo.

### Especificações do manifesto

|Atributos|Descrição|
---|---|
|arquivo-manifesto|nova linha da seção principal *seção-individual|
|main-section|version-info newline *main-attribute|
|version-info|Manifest-Version : version-number|
|número-versão|dígito+{.dígito+}*|
|main-attribute|(qualquer atributo principal legítimo) newline|
|individual-seção|Nome : valor nova linha *perentry-attribute|
|perentry-attribute|(qualquer atributo de perentry legítimo) newline|
|nova linha|CR LF | LF | CR (não seguido de LF)|
|dígito|{0-9}|

## Referências

* [Oracle - Formato de arquivo JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
* [Formato de arquivo JAR](https://en.wikipedia.org/wiki/JAR_(file_format)#:~:text=A%20JAR%20(Java%20ARchive)%20is,into%20one%20file%20for% 20distribution.&text=Eles%20são%20construídos%20em%20a extensão jar%20file%20.)

