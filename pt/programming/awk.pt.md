{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo AWK - arquivo de script AWK",
  "description":"Saiba mais sobre o formato de arquivo AWK e APIs que podem criar e abrir arquivos AWK.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## O que é um arquivo AWK?

Um arquivo AWK é um arquivo de script criado para o aplicativo de processamento de texto **AWK** que vem junto com os sistemas operacionais Unix e Linux. Ele contém instruções lógicas para executar ações no texto ou no conteúdo de um arquivo, como correspondência, substituição e impressão de texto. Isso ajuda a gerar relatórios e texto formatado do arquivo de entrada. O utilitário awk geralmente está localizado em /usr/bin/awk na maioria das distribuições linux/unix.

## Como criar um script AWK?

Um arquivo AWK pode ser criado ou aberto em qualquer editor de texto no sistema operacional Linux/Unix. Um novo arquivo de script AWK pode ser criado da seguinte maneira.

```
$ vi script.awk
```

Isso abrirá o arquivo AWK no editor de texto. Insira algumas instruções no editor de texto como segue.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
A primeira linha deste conteúdo de texto é explicada a seguir.

*\#! – referido como `Shebang`, que especifica um interpretador para as instruções em um script
* /usr/bin/awk – é o interpretador
* -f – opção do interpretador, usada para ler um arquivo de programa

## Como executar o script AWK?

Salve o arquivo e torne o script executável emitindo o comando abaixo:
```
$ chmod +x script.awk
```

O script pode então ser executado da seguinte forma.

```
$ ./script.awk
```

que resulta na seguinte saída.

```
Writing my first Awk executable script!
```

## Referência ##

* [Escrever scripts usando a linguagem de programação Awk](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)

