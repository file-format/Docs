{
  "date" : "2019-12-12",
  "keywords" :[ "EPS", "arquivo", "extensão", "formato de arquivo", "Layout de página", "PostScript encapsulado" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo EPS e APIs que podem criar e abrir arquivos EPS.",
  "title" :"Formato de arquivo EPS - arquivo PostScript encapsulado",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo EPS?

Um arquivo .eps é um arquivo de imagem que é salvo em disco no formato de arquivo Encapsulated Postscript. Pode conter qualquer combinação de texto, gráficos e imagens. Os arquivos EPS também podem incluir uma imagem de visualização de bitmap encapsulada para exibição por aplicativos que podem abrir esses arquivos.

## Breve História do Formato de Arquivo EPS

Uma rápida olhada no formato de arquivo EPS da perspectiva do histórico revela as seguintes informações:

* A primeira versão do EPS foi lançada pela Adobe em algum momento entre 1985 e 1988
* A versão 2.0 da especificação EPS foi publicada em janeiro de 1989
* A especificação para a versão 3.0 do EPS foi publicada como um documento separado em 1992; esta é a última versão publicada.

EPS, em combinação com o mecanismo de extensão Open Structuring Conventions descrito na cláusula 9 da Adobe PostScript Language Document Structuring Conventions Specification, formou a base das primeiras versões do formato de arquivo de arte do Adobe Illustrator.

## Formato de arquivo EPS

EPS é um formato proprietário, mas documentado publicamente, e as especificações de formato de arquivo EPS estão disponíveis publicamente para referência do desenvolvedor. EPS é um formato de arquivo em conformidade com o [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Document Structuring Convention) e adere a todas as regras estabelecidas pelo DSC. O DSC é um formato de arquivo especial para documentos PostScript da Adobe. Qualquer aplicativo que afirma ser capaz de ler arquivos EPS deve ser compatível com DSC.

Um arquivo EPS consiste em duas seções principais, conforme explicado abaixo.

### Visualizar imagem ###

Um arquivo EPS típico contém uma imagem de visualização em um formato destinado ao uso conveniente em um fluxo de trabalho que envolve vários sistemas ou aplicativos. A intenção de uma visualização é ter uma imagem em um formato que a maioria dos aplicativos gráficos possa renderizar; uma visualização geralmente é de resolução mais baixa, em dimensões de pixel e/ou em profundidade de bits. O arquivo de visualização pode estar em um de vários formatos. A especificação para EPS_3 lista três formatos de visualização "específicos do dispositivo":

* para o Apple Macintosh, uma imagem PICT usada pelo aplicativo QuickDraw
* para computadores DOS, um bitmap TIFF
* Metarquivo do Windows.

PICT e Windows Metafile podem incorporar dados de bitmap e gráficos vetoriais. Além disso, a especificação define uma representação independente de dispositivo muito simples para uma imagem de visualização de bitmap incorporada. Esta representação é conhecida como Encapsulated PostScript Interchange Format (EPSI).

Uma visualização EPSI é um bitmap representado como hexadecimal ASCII, agrupado entre alguns comentários PostScript para identificação e destinado a ser simples e facilmente transportável. Para distinguir arquivos EPS com os diferentes formatos de visualização, diferentes extensões de arquivo DOS e tipos de arquivo Macintosh foram recomendados na especificação EPS.

### Código PostScript

No mínimo, o formato de arquivo EPS deve incluir o seguinte:

* um comentário de cabeçalho, %!PS-Adobe-3.0 EPSF-3.0
* e um comentário de caixa delimitadora, %%BoundingBox: llx lly urx ury, que descreve os limites da ilustração. Esses quatro argumentos correspondem aos cantos inferior esquerdo (llx, lly) e superior direito (urx, ury) da caixa delimitadora.

Um arquivo EPS não pode usar nenhum dos seguintes operadores:

* dispositivo de banda,
* cleardictstack
* Copiar página
* apagar
* sair do servidor
* dispositivo de quadro
*grestoreall
* initclip
* initgraphics
* matriz de inicialização
* Sair
* bandas de renderização
* setglobal
* setpagedispositivo
* conjunto compartilhado
* iniciar trabalho.

## Conversão de EPS para outros formatos de arquivo

Os arquivos EPS podem ser convertidos em formatos de imagem padrão, como [JPG](/pt/image/jpeg/), [PNG](/pt/image/png/), [TIFF](/pt/image/tiff/) e [PDF](/pt/pdf /) usando diferentes aplicativos, por exemplo, Adobe Illustrator, Photoshop e PaintShop Pro.

Devido a uma [vulnerabilidade de segurança](https://support.office.com/en-us/article/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e- a1b5-cbb0c334a840) em arquivos EPS, Office 2016, Office 2013, Office 2010 e Office 365 desativaram a capacidade de inserir arquivos EPS em documentos do Office.

## Referências

* [PostScript Encapsulado - Por Wikipedia](https://en.wikipedia.org/wiki/Encapsulated_PostScript)

