{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo ott", "formato de arquivo ott", "o que é um arquivo ott", "arquivo", "exemplo ott", "extensão de arquivo ott", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTT - Arquivo de modelo OpenDocument",
  "description":"Saiba mais sobre o formato de arquivo OTT e APIs que podem criar e abrir arquivos OTT.",
  "linktitle" : "OTT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo OTT?

Arquivos com extensão OTT representam documentos de modelo gerados por aplicativos em conformidade com o formato padrão OpenDocument do OASIS. Eles são criados com aplicativos de processador de texto, como o OpenOffice Writer gratuito, e podem conter configurações que podem ser usadas para gerar novos documentos a partir desses arquivos de modelo. Essas configurações incluem margens de página, bordas, cabeçalhos, rodapés e outras configurações de página. Esses modelos são usados em documentos oficiais, como papéis timbrados da empresa e formulários padronizados.

## Breve história ##

As especificações de formato de arquivo ODP são baseadas no padrão desenvolvido como especificações ODF. Essas especificações evoluíram no passado na forma de três versões desenvolvidas e publicadas pelo OASIS como segue:

**2005:** a versão 1.0 foi publicada em maio de 2005

**2007:** a versão 1.1 foi publicada em fevereiro de 2007

**2011:** a versão 1.2 foi publicada em setembro de 2011

Houve pequenas mudanças na transição das versões ODF 1.0 para 1.1. A [versão ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) é a versão mais recente para especificações de ODF e deve ser consultada por desenvolvedores para desenvolvimento de aplicativos relacionados à leitura/gravação de ODS.

## Especificações de formato de arquivo

O formato OpenDocument suporta a representação de documentos como um único documento XML, bem como uma coleção de vários subdocumentos dentro de um pacote como arquivo [ZIP](/pt/compression/zip/). Cada um dos arquivos do arquivo ZIP armazena parte do documento completo. Cada subdocumento armazena um aspecto particular do documento. Por exemplo, um subdocumento contém as informações de estilo e outro subdocumento contém o conteúdo do documento. Um documento ODF típico tem os seguintes componentes:

* content.xml – Conteúdo do documento e estilos automáticos usados no conteúdo.
* styles.xml – Estilos usados no conteúdo do documento e estilos automáticos usados nos próprios estilos.
* meta.xml – Documentar informações meta, como o autor ou a hora da última ação de salvamento.
* settings.xml – Configurações específicas do aplicativo, como tamanho da janela ou informações da impressora.

Além destes, no pacote pode haver muitos outros subdocumentos como miniaturas de documentos, imagens, etc. Arquivos de documentos são o subconjunto de arquivos ODF onde o conteúdo (folhas) é armazenado no subdocumento //content.xml//.

## Referências ##

* [OpenDocument - Por Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

