{
  "date" : "2019-12-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Seu guia de formato de arquivo para saber o que é um arquivo _XLSX e APIs que podem criar e abrir arquivos _XLSX.",
  "title" :"O que é um arquivo _XLSX?",
  "linktitle" : "_XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-11-22"
}

## O que é um arquivo _XLSX?

Um arquivo com extensão .\_xlsx é na verdade um arquivo [XLSX](/pt/spreadsheet/xlsx/) que é renomeado por algum outro aplicativo. Isso pode acontecer em certos casos quando o nome do arquivo contém uma extensão . no final do nome do arquivo. Os arquivos \_XLSX podem ser abertos no Microsoft Excel de forma semelhante aos arquivos XLSX, renomeando-os novamente para a extensão .xlsx.

## Formato de arquivo _XLSX - Mais informações

Os arquivos _XLSX não são diferentes dos arquivos XLSX e usam o padrão Open XML adotado pela Microsoft em 2000. Antes do XLSX, [XLS](/pt/spreadsheet/xls/) era o principal formato de arquivo usado para trabalhar com planilhas do Excel para salvar documentos em formato binário. Esse novo formato de arquivo baseado em XML veio com vantagens como tamanhos de arquivo pequenos, resistência à corrupção de arquivos e representação de imagens bem formatadas. Este novo formato de arquivo baseado em XML tornou-se parte do Office 2007 e é realizado também nas novas versões do Microsoft.

## \_ Especificações de formato de arquivo XLSX

Como um arquivo \_XLSX é um arquivo XLSX renomeado, ele possui as mesmas especificações do arquivo original. É apenas um arquivo de arquivo baseado no formato de arquivo de arquivo [ZIP](/pt/compression/zip/). Se você quiser ver o conteúdo deste arquivo, basta renomear o arquivo para extensão .zip e extraí-lo para visualizar os arquivos constituintes desta pasta de trabalho do Excel. Uma pasta de trabalho em branco, quando extraída para seus arquivos, tem os seguintes arquivos e pastas constituintes.

### [Content_Types].xml

Este é o único arquivo encontrado no nível base quando o zip é extraído. Ele lista os tipos de conteúdo para peças dentro do pacote. Todas as referências aos arquivos XML incluídos no pacote são referenciadas neste arquivo XML.

### \_rels (Pasta)

Esta é a pasta Relacionamentos que contém um único arquivo XML que armazena os relacionamentos em nível de pacote. Os links para as partes principais dos arquivos Xlsx estão contidos neste arquivo como URIs. Esses URIs identificam o tipo de relacionamento de cada parte chave com o pacote. Isso inclui o relacionamento com o documento principal do escritório localizado como xl/workbook.xml e outras partes em docProps como propriedades principais e estendidas.

### docProps

Esta pasta contém as propriedades gerais do documento. Isso inclui um conjunto de propriedades principais, um conjunto de propriedades estendidas ou específicas do aplicativo e uma visualização em miniatura do documento. Uma pasta de trabalho em branco tem dois arquivos nessa pasta, a saber, app.xml e core.xml. O core.xml contém informações como autor, data de criação e salvamento e modificação. App.xml contém informações sobre o conteúdo do arquivo.

### xl (pasta)

Esta é a pasta principal que contém todos os detalhes sobre o conteúdo da pasta de trabalho. Por padrão, ele possui as seguintes pastas:

* \_rels
* tema
* fichas de trabalho

e os seguintes arquivos xml:

* estilos.xml
* pasta de trabalho.xml

## Referências

* [MS-XLSX - Formato de arquivo .xlsx](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

