{
  "date" : "2019-12-10",
  "keywords" :[ "XLTX", "arquivo", "extensão", "formato de arquivo", "Excel Open XML", "Planilha" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Seu guia de formato de arquivo para saber o que é um arquivo XLTX e APIs que podem criá-los e abri-los.",
  "title" :"O que é um arquivo XLTX?",
  "linktitle" : "XLTX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## O que é um arquivo XLTX?

Arquivos com extensão .xltx representam arquivos de modelo do Microsoft Excel baseados nas especificações de formato de arquivo OpenXML do Office. Ele é usado para criar um arquivo de modelo padrão que pode ser utilizado para gerar arquivos [XLSX](/pt/spreadsheet/xlsx/) que exibem as mesmas configurações especificadas no arquivo XLTX.

## Breve história

Foi no início de 2000, quando a Microsoft decidiu fazer a mudança para acomodar o padrão para **Office Open XML**. Documentos, de diferentes tipos, sob esta nova Norma foram identificados anexando "X" em suas extensões, sendo "X" para XML. Em 2007, esse novo formato de arquivo passou a fazer parte do Office 2007 e é mantido também nas novas versões do Microsoft Office. O novo tipo de arquivo adicionou vantagens de tamanhos de arquivo pequenos, menos alterações de corrupção e representação de imagens bem formatadas.

## Especificações de formato de arquivo XLTX

Os arquivos XLTX são baseados no formato de arquivo OpenXML do Office e usam XML e [ZIP](/pt/compression/zip/) para reduzir o tamanho do arquivo. Ele foi criado com o lançamento do Microsoft Office 2007 para substituir o formato de arquivo binário XLT. Semelhante ao XLTX, o formato de arquivo XLT pode ser usado para criar arquivos [XLS](/pt/spreadsheet/xls/) usando o Microsoft Excel 2003 e 2007. Eles podem ser abertos com o Microsoft Excel clicando duas vezes no arquivo. A organização dos arquivos em um formato de arquivo XLTX pode ser observada renomeando o arquivo para ZIP e depois extraindo seu conteúdo para o disco.

### [Content_Types].xml ###

Este é o único arquivo encontrado no nível base quando o zip é extraído. Ele lista os tipos de conteúdo para peças dentro do pacote. Todas as referências aos arquivos XML incluídos no pacote são referenciadas neste arquivo XML.

### \_rels (Pasta) ###

Esta é a pasta Relacionamentos que contém um único arquivo XML que armazena os relacionamentos em nível de pacote. Os links para as partes principais dos arquivos Xltx estão contidos neste arquivo como URIs. Esses URIs identificam o tipo de relacionamento de cada parte chave com o pacote. Isso inclui o relacionamento com o documento principal do escritório localizado como xl/workbook.xml e outras partes em docProps como propriedades principais e estendidas.

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

## Referências ##

* [[MS-XLSX] - Formato de arquivo .Xlsx](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

