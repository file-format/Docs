{
  "date" : "2020-08-20",
  "keywords" :[ "arquivo cff", "formato de arquivo cff", "o que é um arquivo cff", "arquivo", "exemplo de cff", "extensão de arquivo cff", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF - Formato de arquivo de fonte compacta",
  "description":"Saiba mais sobre o formato de arquivo CFF e APIs para criar e abrir arquivos CFF.",
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## O que é um arquivo CFF?

Um arquivo com extensão .cff é um formato de fonte compacta e também é conhecido como PostScript Type 1 ou CIDFont. O CFF atua como um contêiner para armazenar várias fontes juntas em uma única unidade conhecida como FontSet. O design das fontes CFF permite incorporar código de linguagem PostScript que permite flexibilidade e extensibilidade adicionais do formato para uso com ambientes de impressora. Os arquivos de fonte CFF podem ser abertos e convertidos usando APIs como [Aspose.Font](https://products.aspose.com/font).

## Formato de arquivo CFF

Os arquivos CFF são arquivos binários que contêm um layout de dados estruturado, tipos de dados definidos, um cabeçalho, organização de glifos e dicionários de tabelas. Mais detalhes sobre eles podem ser encontrados nas [especificações de formato de fonte compacta](https://docs.microsoft.com/en-us/typography/opentype/spec/cff).

### Layout de dados
O layout de dados do formato de arquivo CFF é mostrado abaixo.

|Entrada|Comentários|
---|---|
|Cabeçalho|–|
|NomeINDEX|–|
|ÍNDICE DICT superior|–|
|String ÍNDICE|–|
|Subr Global ÍNDICE|–|
|Codificações–Charsets|–|
|FDSelect|CIDFonts apenas|
|CharStrings INDEX|por-fonte|
|Fonte DICT INDEX|por fonte, apenas CIDFonts|
|DICT privado|por-fonte|
|Local Subr INDEX|por fonte ou por-Private DICT para CIDFonts|
|Avisos de Direitos Autorais e Marcas Registradas|–|

### Tipos de dados

Os tipos de dados CFF são mostrados na tabela a seguir.

|Nome|Intervalo|Descrição|
---|---|---|
|Card8|0 –255|número sem sinal de 1 byte|
|Card16|0 – 65535|número sem sinal de 2 bytes|
|Offset|varies|1, 2, 3 ou 4 bytes offset (especificado pelo campo OffSize)|
|OffSize|1–4|número sem sinal de 1 byte especifica o tamanho de um campo ou campos de deslocamento|
|SID|0 – 64999|identificador de string de 2 bytes|

### Cabeçalho

Os dados binários começam com um cabeçalho com o formato mostrado na tabela a seguir.

|Tipo|Nome|Descrição|
---|---|---|
|Card8|major|Formatar versão principal (começando em 1)|
|Card8|minor|Formatar versão secundária (começando em 0)|
|Card8|hdrSize| Tamanho do cabeçalho (bytes)|
|OffSize|offSize|Deslocamento absoluto (0) tamanho|

## Referências

* [Tabela de formato de fonte compacta](https://docs.microsoft.com/en-us/typography/opentype/spec/cff)
* [Formato de arquivo CFF](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
* [Conjunto de gráficos CFF2](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

