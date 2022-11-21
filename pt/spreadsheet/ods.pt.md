{
  "date" : "2019-12-10",
  "keywords" :[ "ODS", "arquivo", "extensão", "formato de arquivo", "Planilha OpenDocument" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Seu guia de formato de arquivo para saber o que é um arquivo ODS e APIs que podem criá-los e abri-los.",
  "title" :"O que é um arquivo ODS?",
  "linktitle" : "ODS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## O que é um arquivo ODS?

Arquivos com extensão .ods representam o formato OpenDocument Spreadsheet Document que pode ser editado pelo usuário. Os dados são armazenados dentro do arquivo ODF em linhas e colunas. É um formato baseado em XML e é um dos vários subtipos da família Open Document Formats (ODF). O formato é especificado como parte das especificações ODF 1.2 publicadas e mantidas pelo OASIS. Vários aplicativos no Windows, bem como em outros sistemas operacionais, podem abrir arquivos ODS para edição e manipulação, incluindo Microsoft Excel, NeoOffice e LibreOffice. Os arquivos ODS também podem ser convertidos em outros formatos de planilha, como [XLS](/pt/spreadsheet/xls/), [XLSX](/pt/spreadsheet/xlsx/) e outros por diferentes aplicativos.

## Breve história ##

As especificações de formato de arquivo ODS são baseadas no padrão desenvolvido como especificações ODF. Essas especificações evoluíram no passado na forma de três versões desenvolvidas e publicadas pelo OASIS como segue:

`2005` - A versão 1.0 foi publicada em maio de 2005

`2007` - A versão 1.1 foi publicada em fevereiro de 2007

`2011` - A versão 1.2 foi publicada em setembro de 2011

Houve pequenas mudanças na transição das versões ODF 1.0 para 1.1. A [versão ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) é a versão mais recente para especificações de ODF e deve ser consultada por desenvolvedores para desenvolvimento de aplicativos relacionados à leitura/gravação de ODS.

## Formato de arquivo ODS ##

O formato OpenDocument suporta a representação de documentos como um único documento XML, bem como uma coleção de vários subdocumentos dentro de um pacote como arquivo [ZIP](/pt/compression/zip/). Cada um dos arquivos do arquivo ZIP armazena parte do documento completo. Cada subdocumento armazena um aspecto particular do documento. Por exemplo, um subdocumento contém as informações de estilo e outro subdocumento contém o conteúdo do documento. Um documento ODF típico tem os seguintes componentes:

* `content.xml` – Conteúdo do documento e estilos automáticos usados no conteúdo.
* `styles.xml` – Estilos usados no conteúdo do documento e estilos automáticos usados nos próprios estilos.
* `meta.xml` – Documento meta-informações, como o autor ou a hora da última ação de salvamento.
* `settings.xml` – Configurações específicas do aplicativo, como tamanho da janela ou informações da impressora.

Além destes, no pacote pode haver muitos outros subdocumentos como miniaturas de documentos, imagens, etc.

Arquivos de documento de planilha são o subconjunto de arquivos ODF onde o conteúdo (folhas) é armazenado no subdocumento content.xml.

## Referências ##

* [OpenDocument - Por Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

