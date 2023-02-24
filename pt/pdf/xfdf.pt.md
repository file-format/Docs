{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo XFDF - O que é um arquivo XFDF?",
  "description":"Saiba mais sobre o arquivo XFDF e APIs que podem criar e abrir arquivos XFDF.",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo XFDF?

Um arquivo com extensão .xfdf é um formato de dados de formulários XML gerado com o software Adobe Acrobat. Assim como o [FDF](/pt/pdf/fdf/), o XFDF contém a descrição dos elementos do formulário e seus valores no formato XML. Isso pode incluir os nomes e valores dos campos de texto no formulário PDF. XFDF são salvos em formato legível por humanos e podem ser lidos programaticamente usando linguagens de programação como C#.

## Formato de arquivo XFDF - Mais informações

Os arquivos XFDF são salvos no formato de arquivo XML, que é um formato universal usado para importação e exportação de dados. Uma estrutura de arquivo XFDF consiste em um cabeçalho, seguido por valores de campo e dados de elementos, conforme mostrado abaixo.

|Elemento|Atributo|Conteúdo|
---|---|---|
|\<XFDF> ||Elemento superior|
|\<fields> ||Todos os valores de campo para este modelo|
|<field (T)> |nome |Nome do campo|
|<value (V)> |valor |Valor do campo|

## Referências

* [Suporte ao formato FDF do Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for-acroforms.html)
* [Recursos para desenvolvedores da Adobe](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

