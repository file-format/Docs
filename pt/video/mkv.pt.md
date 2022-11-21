{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo MKV",
  "keywords" :[ "mkv", "vídeo matroska", "formato mkv", "como reproduzir arquivos mkv", "vídeo", "arquivo", "formato" ],
  "description":"Saiba mais sobre o formato de arquivo MKV e APIs que podem criar e abrir arquivos MKV.",
  "linktitle" : "MKV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2020-17-11"
}


## O que é um arquivo MKV? ##

MKV (Matroska Video) é um contêiner multimídia semelhante ao formato [MOV](/pt/video/mov/) e [AVI](/pt/video/avi/), mas suporta mais de uma faixa de áudio e legenda no mesmo arquivo. Um arquivo MKV é o formato de contêiner multimídia Matroska usado para vídeo. O MKV é baseado em Extensible Binary Meta Language e suporta vários formatos de compressão de vídeo e áudio. A principal diferença entre o MKV e outros formatos de vídeo é que o MKV é um contêiner e não um codec. Os arquivos MKV são salvos com a extensão de arquivo .mkv. O MKV pode incorporar áudio, vídeo e legendas em um único arquivo, mesmo que esses elementos usem diferentes tipos de codificação. Por exemplo, você pode ter um arquivo MKV que contenha vídeo H.264 e MP3 ou AAC para áudio. O MKV também suporta descrições, classificações, arte da capa e até pontos de capítulo. Existem vários recursos importantes que o MKV é à prova de futuro. Esses recursos incluem:

- Suporte para busca rápida.
- Capacidade de selecionar diferentes fluxos de áudio e vídeo.
- Suporte para legendas (hard-coded e soft-coded).
- Suporte para metadados, capítulos e menus.
- Capacidade de transmissão online.
- Capacidade de recuperar arquivos errôneos que fornecem a capacidade de reproduzir arquivos corrompidos.

## Breve história ##

O arquivo MKV originou-se em 2002 na Rússia. O desenvolvedor líder foi Lasse Kärkkäinen, que trabalhou com o fundador da Matroska, Steve Lhomme, e uma equipe de programadores. O MKV foi desenvolvido como um projeto de padrões abertos, o que significa que é de código aberto e de uso gratuito. Com o passar do tempo, o formato foi aprimorado e tornou-se a base do formato multimídia WebM em 2010.

## Projeto Matroska ##

Matroska adiciona as seguintes restrições à especificação EBML.

- O **docType** do **EBML Header** deve ser 'matroska'.
- O **EBMLMaxIDLength** do **EBML Header** deve ser 4.
- O **EBMLMaxSizeLength** do **EBML Header** deve estar entre 1 e 8 (inclusive).

Todos os elementos de nível superior são codificados em 4 octetos.

- Códigos de idioma: Matroska (versão 1 a 3) usou códigos de idioma que podem ser o formato bibliográfico ISO-639-2 de 3 letras (como "fre" para francês), ou código de país adicional pode ser usado como "fre-ca " para o francês canadense. A partir da versão 4 do Matroska, o ISO 639-2 ou o BCP 47 PODEM ser usados para códigos de idioma, embora o BCP 47 seja recomendado.
- Tipos Físicos: Estes têm significados diferentes para arquivos de áudio e vídeo. Por exemplo, ChapterPhysicalEquiv = 60 significa (CD / 12" / 10" / 7" / TAPE / MINIDISC / DAT) para áudio e (DVD / VHS / LASERDISC) para vídeo.
- Estrutura do Bloco - Cabeçalho do Bloco: O cabeçalho do bloco contém informações sobre o número da faixa, carimbos de data/hora, tipo de laço, etc.
- Lacing: É um mecanismo para economizar espaço ao armazenar dados que normalmente é usado para pequenos blocos de dados (frames). Existem 3 tipos de laço:
  - Xiph: Frame with a size multiple of 255 coded with a 0 at the end of the size. For example, The code for 765 is 255;255;255;0.
  - EBML: The frame size is coded as a difference between the previous size and this size. The first size in the lace is unsigned but others use a range shift to get a sign on each value.
  - fixed-size: The size remains the same.
- Estrutura SimpleBlock: É inspirada na **estrutura de bloco** com a principal diferença sendo a adição de sinalizadores **Keyframe** e **Discardable**. Fora isso, tudo igual.

## Estrutura Matroska ##

Um documento Matroska deve ser composto por pelo menos um **Documento EBML** usando o **Tipo de Documento Matroska**. Cada **Documento EBML** deve começar com um **Cabeçalho EBML** seguido pelo **Elemento Raiz EBML** definido como um Segmento. Matroska define vários Elementos de Nível Superior que podem ocorrer dentro do **Segmento**.

EBML usa um sistema de Elementos para compor um Documento EBML, A seguir está a lista de elementos de nível superior no arquivo Matroska:

- **Documento EBML**: Wrapper para todo o arquivo.
- **EBML Header**: Contém as informações do cabeçalho do arquivo como DocType.
- **Segmento**: o elemento superior que contém todos os outros elementos de nível superior.
- **SeekHead**: Contém a posição dos Segmentos de outros Elementos de Nível Superior.
- **Info**: Contém informações gerais sobre o Segmento.
- **Faixas**: um elemento de informação de nível superior com muitas faixas descritas.
- **Capítulos**: É usado para definir menus básicos e dados de partição.
- **Cluster**: O Elemento de Nível Superior que contém a estrutura do Bloco.
- **Cues**: Um Elemento de Nível Superior que contém todas as entradas locais para o Segmento que aceleram a busca de acesso.
- **Anexos**: Contém arquivos anexados.
- **Tags**: este elemento contém metadados que descrevem Faixas, Edições, Capítulos, Anexos ou o Segmento como um todo.

A tabela a seguir mostra a estrutura do documento Matroska com a maioria dos elementos exibidos em uma hierarquia:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| Cabeçalho EBML | | | |
| Segmento | SeekHead| Procurar | ProcurarID |
| | | | ProcurarPosição |
| | Informações | SegmentUID | |
| | | SegmentFilename | |
| | | AnteriorUID | |
| | | PrevFilename | |
| | | PróximoUID | |
| | | PróximoFilename | |
| | | SegmentoFamília | |
| | | CapítuloTraduzir | |
| | | TimestampScale | |
| | | Duração | |
| | | DataUTC | |
| | | Título | |
| | | MuxingApp | |
| | | WritingApp | |
| | Faixas | TrackEntry | TrackNumber |
| | | | TrackUID |
| | | | Tipo de faixa |
| | | | Nome |
| | | | Idioma |
| | | | CodecID |
| | | | CodecPrivado |
| | | | CodecName |
| | | | Vídeo | BandeiraEntrelaçado |
| | | | | FieldOrder |
| | | | | StereoMode |
| | | | | AlphaMode |
| | | | | PixelWidth |
| | | | | PixelAltura |
| | | | | Largura de exibição |
| | | | | Altura de exibição |
| | | | | AspectRatioType |
| | | | | Cor |
| | | | Áudio | Frequência de Amostragem |
| | | | | Canais |
| | | | | BitDepth |
| | Capítulos | EdiçãoEntrada | EdiçãoUID |
| | | | EdiçãoFlagHidden |
| | | | EdiçãoFlagPadrão |
| | | | EdiçãoFlagOrdenado |
| | | | CapítuloAtom | CapítuloUID |
| | | | | CapítuloStringUID |
| | | | | CapítuloHoraInício |
| | | | | CapítuloHoraFim |
| | | | | CapítuloFlagHidden |
| | | | | Capítulo Exibição | ChapString |
| | | | | | ChapLinguagem |
| | Agrupamento | Carimbo de data e hora |
| | | SilentTracks |
| | | Posição |
| | | Tamanho anterior |
| | | SimpleBlock |
| | | BlockGrupo |
| | | Bloco Criptografado |
| | Dicas | CuePoint | CueTime |
| | | | CueTrackPosições |
| | Anexos | Arquivo Anexado | Descrição do arquivo |
| | | | Nome do arquivo |
| | | | FileMimeType |
| | | | ArquivoUID |
| | | | Referência de arquivo |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | Etiquetas | Etiqueta | Alvos | TargetTypeValue |
| | | | | Tipo de destino |
| | | | | TagTrackUID |
| | | | | TagEdiçãoUID |
| | | | | TagChapterUID |
| | | | | TagAttachmentUID |
| | | | SimpleTag | TagName |
| | | | | TagLinguagem |
| | | | | TagPadrão |
| | | | | TagString |
| | | | | TagBinário |
| | | | | SimpleTag |


### Usando Codecs ###

Se você não quiser um novo reprodutor de mídia e preferir usar o reprodutor existente, precisará instalar alguns codecs (abreviação de compactação/descompactação). Embora o download de codecs seja uma opção válida, você deve ter cuidado com a fonte, pois eles podem conter malware.

## Referências ##

- [Matroska pela Wikipedia](https://en.wikipedia.org/wiki/Matroska)

