{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo odt", "formato de arquivo odt", "o que é um arquivo odt", "arquivo", "exemplo odt", "extensão de arquivo odt", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODT - Arquivo de texto OpenDocument",
  "description":"Saiba mais sobre o formato de arquivo ODT e APIs que podem criar e abrir arquivos ODT.",
  "linktitle" : "ODT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo ODT?

Os arquivos ODT são tipos de documentos criados com aplicativos de processamento de texto baseados no formato OpenDocument Text File. Estes são criados com aplicativos de processamento de texto como o OpenOffice Writer gratuito e podem conter conteúdo como texto, imagens, objetos e estilos. O arquivo ODT é para o processador de texto Writer o que o [DOCX](/pt/word-processing/docx/) é para o Microsoft Word. Vários aplicativos, incluindo o Google Docs e o processador de texto baseado na Web do Google incluído no Google Drive, podem abrir os arquivos ODT para edição. O Microsoft Word também pode abrir arquivos ODT e salvá-los em outros formatos, como [DOC](/pt/word-processing/doc/) e DOCX.

## Breve história ##

As especificações de formato de arquivo ODP são baseadas no padrão desenvolvido como especificações ODF. Essas especificações evoluíram no passado na forma de três versões desenvolvidas e publicadas pelo OASIS como segue:

**2005** A versão 1.0 foi publicada em maio de 2005

**2007:** a versão 1.1 foi publicada em fevereiro de 2007

**2011:** a versão 1.2 foi publicada em setembro de 2011

Houve pequenas mudanças na transição das versões ODF 1.0 para 1.1. A [versão ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) é a versão mais recente para especificações de ODF e deve ser consultada por desenvolvedores para desenvolvimento de aplicativos relacionados à leitura/gravação de ODS.

## Especificações de formato de arquivo ##

O formato OpenDocument suporta a representação de documentos como um único documento XML, bem como uma coleção de vários subdocumentos dentro de um pacote como arquivo [ZIP](/pt/compression/zip/). Cada um dos arquivos do arquivo ZIP armazena parte do documento completo. Cada subdocumento armazena um aspecto particular do documento. Por exemplo, um subdocumento contém as informações de estilo e outro subdocumento contém o conteúdo do documento. Um documento ODF típico tem os seguintes componentes:

* content.xml – Conteúdo do documento e estilos automáticos usados no conteúdo.
* styles.xml – Estilos usados no conteúdo do documento e estilos automáticos usados nos próprios estilos.
* meta.xml – Documentar informações meta, como o autor ou a hora da última ação de salvamento.
* settings.xml – Configurações específicas do aplicativo, como tamanho da janela ou informações da impressora.

Além destes, no pacote pode haver muitos outros subdocumentos como miniaturas de documentos, imagens, etc. Arquivos de documentos são o subconjunto de arquivos ODF onde o conteúdo (folhas) é armazenado no subdocumento //content.xml//.

## Referências ##

* [OpenDocument - Por Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

