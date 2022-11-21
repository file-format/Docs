{
  "date" : "2019-12-10",
  "keywords" :[ "XLSX", "arquivo", "extensão", "formato de arquivo", "Excel", "Planilha" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o que é um arquivo XLSX e APIs que podem criar e abrir arquivos XLSX.",
  "title" :"Formato de arquivo XLSX - O que é um arquivo XLSX?",
  "linktitle" : "XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## O que é um arquivo XLSX?

**XLSX** é um formato bem conhecido para documentos do Microsoft Excel que foi introduzido pela Microsoft com o lançamento do Microsoft Office 2007. Com base na estrutura organizada de acordo com as Convenções de Empacotamento Aberto, conforme descrito na [Parte 2](https://www .ecma-international.org/publications/standards/Ecma-376.htm) do padrão OOXML ECMA-376, o novo formato é um pacote zip que contém vários arquivos XML. A estrutura e os arquivos subjacentes podem ser examinados simplesmente descompactando o arquivo .xlsx.

## Breve História do Formato de Arquivo XLSX

O formato de arquivo XLSX foi introduzido em 2007 e usa o padrão Open XML adaptado pela Microsoft em 2000. Antes do XLSX, o formato de arquivo comum usado era [XLS](/pt/spreadsheet/xls/) que era o formato de arquivo binário puro. O novo tipo de arquivo adicionou vantagens de tamanhos de arquivo pequenos, menos alterações de corrupção e representação de imagens bem formatadas. Foi no início de 2000, quando a Microsoft decidiu fazer a mudança para acomodar o padrão para **Office Open XML**. Em 2007, esse novo formato de arquivo passou a fazer parte do Office 2007 e é mantido também nas novas versões do Microsoft Office.

## Especificações de formato de arquivo XLSX

As [especificações de formato de arquivo XLSX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) oficiais estão disponíveis online na Microsoft. Para ver o que está dentro do arquivo XLSX, basta renomeá-lo para arquivo [ZIP](/pt/compression/zip/) alterando sua extensão e depois extraí-lo para visualizar os arquivos constituintes desta pasta de trabalho do Excel. Uma pasta de trabalho em branco, quando extraída para seus arquivos, tem os seguintes arquivos e pastas constituintes.

### [Content_Types].xml ###

Este é o único arquivo encontrado no nível base quando o zip é extraído. Ele lista os tipos de conteúdo para peças dentro do pacote. Todas as referências aos arquivos XML incluídos no pacote são referenciadas neste arquivo XML.

### \_rels (Pasta) ###

Esta é a pasta Relacionamentos que contém um único arquivo XML que armazena os relacionamentos em nível de pacote. Os links para as partes principais dos arquivos Xlsx estão contidos neste arquivo como URIs. Esses URIs identificam o tipo de relacionamento de cada parte chave com o pacote. Isso inclui o relacionamento com o documento principal do escritório localizado como xl/workbook.xml e outras partes em docProps como propriedades principais e estendidas.

### docProps ###

Esta pasta contém as propriedades gerais do documento. Isso inclui um conjunto de propriedades principais, um conjunto de propriedades estendidas ou específicas do aplicativo e uma visualização em miniatura do documento. Uma pasta de trabalho em branco tem dois arquivos nessa pasta, a saber, app.xml e core.xml. O core.xml contém informações como autor, data de criação e salvamento e modificação. App.xml contém informações sobre o conteúdo do arquivo.

### xl (Pasta) ###

Esta é a pasta principal que contém todos os detalhes sobre o conteúdo da pasta de trabalho. Por padrão, ele possui as seguintes pastas:

* \_rels
* tema
* fichas de trabalho

e os seguintes arquivos xml:

* estilos.xml
* pasta de trabalho.xml

## Exemplo de formato XLSX ##


Para cada planilha do Excel contida em uma pasta de trabalho, há um arquivo XML. Você pode encontrar esses arquivos XML na pasta xl/worksheets. Todas as informações contidas em uma planilha são organizadas em diferentes seções no arquivo XML. Vamos examinar uma planilha de exemplo de uma pasta de trabalho que é mostrada na imagem a seguir.

{{< figure src="../XLSX file format.png" alt="Formato de arquivo XLSX" >}}

Como pode ser visto, esta planilha contém conteúdos nas células A1 a B2 e uma imagem. Além disso, a célula G13 é atualmente a célula ativa na planilha. Agora, vamos examinar o arquivo xl/worksheets/sheet1.xml para ver como essas informações são representadas no arquivo XML. O conteúdo deste arquivo XML é mostrado abaixo.

{{< figure src="../XLSX File Format Details.png" alt="Formato de arquivo XPS" >}}

1. A guia tem a cor do tema aplicada. É mencionado no arquivo XML com tag<tabColor> seguindo o id do tema.
1. O valor tabSelected é definido como 1, o que mostra que esta é a planilha selecionada
1. Como pode ser visto na primeira imagem acima, a célula G13 na planilha é uma célula ativa que também é mencionada no arquivo XML.
1. A guia sheetData representa os dados contidos na planilha. No entanto, você pode ver que o conteúdo original da planilha não está nesta seção. Isso ocorre porque o texto é referido indiretamente da planilha XML "sharedStrings". Essa vinculação garante que cada texto seja salvo apenas uma vez e possa ser referenciado novamente para economizar espaço.
1. A imagem como pode ser vista é referenciada pelo ID de referência "rId2"

## Contribuir

Precisa compartilhar algo sobre os formatos de arquivo XLSX ou Planilha? Você pode postar suas descobertas na seção [Newssheet File Format News](https://news.fileformat.com/t/Spreadsheet).

## Referências

* [[MS-XLSX] - Formato de arquivo XLSX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

