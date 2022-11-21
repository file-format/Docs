{
  "date" : "2019-12-10",
  "keywords" :[ "DIF", "arquivo", "extensão", "formato de arquivo", "Arquivo de intercâmbio de dados", "Planilha" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Seu guia de formato de arquivo para saber o que é uma extensão de arquivo DIF e APIs que podem criar e abrir arquivos DIF.",
  "title" :"DIF - Formato de arquivo de intercâmbio de dados",
  "linktitle" : "DIF",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## O que é um arquivo DIF?

DIF significa Data Interchange Format que é usado para importar/exportar dados de planilhas entre diferentes aplicativos. Estes incluem Microsoft Excel, OpenOffice Calc, StarCalc e muitos outros. Ele armazena os dados contidos em uma única planilha que é a única limitação deste formato de arquivo.

## Breve Histórico do Formato de Arquivo DIF ##

O formato de arquivo DIF foi desenvolvido pela Software Arts, Inc. no início dos anos 80. As especificações de formato de arquivo para DIF foram incluídas no VisiCalc, que foi o primeiro programa de planilha para computadores pessoais. Essas especificações foram protegidas por direitos autorais em 1981 e eram uma marca registrada da Software Arts Products Corp.

## Formato de arquivo DIF ##

O DIF armazena o conteúdo da planilha em arquivo de texto ASCII que permite visualizá-la e editá-la com um editor de texto. O formato possui seu lugar na lista de formatos de serialização de dados por suas características de intercâmbio de dados. Um arquivo DIF consiste em 2 seções; um cabeçalho e dados.

Tudo em DIF é representado por um bloco de 2 ou 3 linhas. Os cabeçalhos recebem um bloco de 3 linhas; dados, 2.

* Os blocos de cabeçalho começam com um identificador de texto que é todo em maiúsculas, apenas caracteres alfabéticos e menos de 32 letras. A linha a seguir deve ser um par de números e a terceira linha deve ser uma string entre aspas.
* Os blocos de dados começam com um par de números e a próxima linha é uma string entre aspas ou uma palavra-chave.

### Valores ###

Um valor ocupa duas linhas, a primeira um par de números e a segunda uma string ou uma palavra-chave. O primeiro número do par indica o tipo:

* −1 – tipo de diretiva, o segundo número é ignorado, a linha a seguir é uma dessas palavras-chave:
** BOT – início da tupla (início da linha)
** EOD - fim dos dados
* 0 – tipo numérico, valor é o segundo número, a linha a seguir é uma dessas palavras-chave:
**V - válido
** NA – não disponível
** ERRO - erro
** TRUE – valor booleano verdadeiro
** FALSE – valor booleano falso
* 1 – tipo de string, o segundo número é ignorado, a linha a seguir é a string entre aspas duplas

### Parte do cabeçalho DIF ###

A parte do cabeçalho de um arquivo DIF é composta por uma linha identificadora seguida pelas duas linhas de um valor. Os valores numéricos nos blocos de cabeçalho usam apenas uma string vazia em vez das palavras-chave de validade. Os detalhes desses pedaços de cabeçalho são os seguintes.

* TABLE - segue um valor numérico da versão, a segunda linha do valor em desuso contém um comentário do gerador
* VETORES - o número de colunas segue como valor numérico
* TUPLES - o número de linhas segue como um valor numérico
* DADOS - após um valor numérico fictício 0, os dados da tabela seguem, cada linha precedida por um valor BOT, a tabela inteira terminada por um valor EOD

### Exemplo de DIF ###

O exemplo a seguir mostra o conteúdo de uma planilha simples e sua representação DIF equivalente.


|Nome|Idade
---|---|
|Bob|34
|Folha|22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## Referências ##

* [ DIF - Por Wikipedia](https://en.wikipedia.org/wiki/Data_Interchange_Format)

