{
  "date" : "2021-06-29",
  "keywords" :[ "arquivo com", "o que é um arquivo com", "arquivo", "exemplo com", "extensão de arquivo com", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo COM e APIs que podem criar e abrir arquivos COM.",
  "title" :"COM - Formato de arquivo de comando DOS",
  "linktitle" : "COM",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-29"
}

## O que é um arquivo COM?
Os arquivos COM são usados simplesmente para executar um conjunto de comandos ou instruções. Um arquivo COM consiste em um programa executável que pode ser executado no Windows ou no MS-DOS. Da mesma forma que um arquivo EXE, o arquivo COM também é salvo em formato binário, mas é diferente do arquivo EXE porque não possui cabeçalho ou metadados e também possui o tamanho máximo de aproximadamente 64 KB. Quando o arquivo COM é executado pela primeira vez em um sistema de 32 bits, ele solicita a instalação do componente NT Virtual DOS Machine (NTVDM). O arquivo COM pode ser executado na versão de 64 bits do Microsoft Windows com uma máquina virtual que ofereça suporte ao ambiente MS-DOS.

## Formato de arquivo COM
O formato de arquivo COM é um formato executável binário usado no Microsoft Windows ou MS-DOS. Sua estrutura consiste em apenas um conjunto de instruções; não tem cabeçalho e não contém metadados padrão. Ele armazena todos os seus dados e código em apenas um segmento e seu binário tem tamanho máximo de 64 KB. Este formato de arquivo não se realoca ao tentar executar novamente. Assim, o sistema operacional o carrega em um endereço predefinido. Além disso, é possível fazer um arquivo COM para executar em ambos os sistemas operacionais na forma de um **fat binary**. Não há nenhuma compatibilidade real no nível de instrução. As instruções no ponto de entrada são selecionadas para serem iguais em funcionalidade, mas diferentes em ambos os sistemas operacionais, e fazem o programa em execução, pular para a seção do sistema operacional em uso. São basicamente dois programas diferentes com o mesmo procedimento em um único arquivo, precedidos de código selecionando aquele a ser utilizado.
### Exemplo de arquivo COM
Ao executar um arquivo COM, as instruções são lidas a partir do primeiro byte e são seguidas consecutivamente até que as últimas instruções sejam encontradas. Aqui está um exemplo de código ASM:

```
[BITS 16]		;Set code generation to 16 bit mode
[ORG 0x0100]		;Set code start address to 0100h


[SEGMENT .text]		;Main code segment
    mov ah, 9 ; DOS print string function
    mov dx, hello
    int 21h
    ;Exit to DOS
    mov ah, 4ch
    int 21h
[SEGMENT .data]		;Initialised data segment
hello:   db   'Hello, .COM programmer!',13,10,'$'
```

## Referências

* [arquivo COM - por Wikipewdia](https://en.wikipedia.org/wiki/COM_file)

