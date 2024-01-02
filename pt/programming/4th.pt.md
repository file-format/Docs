
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"4º arquivo - formato de arquivo do quarto idioma",
  "description":"Aprenda sobre o que é o formato de arquivo .4 com exemplos e APIs que podem criar e abrir arquivos 4.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## O que é um quarto arquivo?

Um arquivo com extensão .4th é um arquivo de programação criado para a **Forth Programming Language**. Ele contém código-fonte para programas escritos na linguagem de programação Forth e gera a saída quando o programa é executado. É apenas outro arquivo de linguagem de programação semelhante ao arquivo fonte [C](/pt/programming/c/) e [C++](/pt/programming/cpp/).

## 4º Formato de Arquivo – Mais Informações


### 4º exemplo de código de linguagem de programação

Aqui está um exemplo de um programa simples escrito em Forth que calcula o fatorial de um determinado número:

```
: factorial ( n -- n! )
   dup 0=
   if
      drop 1
      exit
   then
   1
   swap
   begin
      dup 1-
      dup 0=
      if
         drop
         exit
      then
      swap
      *
   repeat
;

```

Neste exemplo, a palavra fatorial recebe um único argumento n e retorna seu fatorial. A palavra dup duplica o valor no topo da pilha, drop descarta o valor no topo da pilha e * multiplica os dois valores no topo da pilha. As construções if e start/until controlam o fluxo do programa.

Para usar este programa, você deve inserir a definição no interpretador Forth e, em seguida, chamar a palavra fatorial com o número cujo fatorial deseja encontrar:

```
10 factorial .
```
Isso resultaria na saída 3628800, que é o fatorial de 10.

## Referências

* [Quarta Linguagem de Programação](https://en.wikipedia.org/wiki/Forth_(programming_language))

