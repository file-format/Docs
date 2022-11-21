{
  "date" : "2021-04-26",
  "keywords" :[ "aiff", "arquivo", "extensão", "formato", "formato de arquivo de intercâmbio de áudio", "música", "formato de arquivo aiff", "aiff para mp3", "aiff vs wav", "converter aiff para mp3" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo AIFF e APIs que podem criar, converter e abrir arquivos AIFF.",
  "title" :"AIFF - Formato de arquivo de intercâmbio de áudio",
  "linktitle" : "AIFF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## O que é um arquivo AIFF?
O AIFF (Audio Interchange File Format) é um formato de arquivo de áudio não compactado desenvolvido pela Apple em 1998, mas é baseado no **EA IFF 85** (Padrão para Arquivos de Formato de Intercâmbio desenvolvido pela Electronic Arts), um formato wrapper usado em sistemas Amiga . Este formato de arquivo vem com um padrão para armazenar sons amostrados. O formato é bom o suficiente em flexibilidade e permite o armazenamento de sons amostrados mono ou multicanal em várias taxas de amostragem e larguras de amostra. Como os arquivos AIFF são descompactados, isso os torna maiores em tamanho do que outros formatos com perdas, como [MP3](https://docs.fileformat.com/audio/mp3/).

Os arquivos AIFF consistem em 2 canais de áudio estéreo não compactado com tamanho de amostra de 16 bits, gravados em 44,1 khz. Devido à alta qualidade do áudio, um áudio de 5 minutos pode ocupar até 50 MB de espaço em disco, semelhante ao formato de arquivo [WAV](https://docs.fileformat.com/audio/wav/).

## AIFF vs WAV

O AIFF e o WAV são quase os mesmos em termos de qualidade. Ambos usam a mesma codificação PCM (modulação de código de pulso), o que os torna maiores em tamanho em comparação com outros formatos com perdas, como [MP3](https://docs.fileformat.com/audio/mp3/), [M4A](). Algumas das diferenças gerais estão escritas na tabela abaixo:

|AIFF|WAV|
---|---|
|Sendo usado principalmente para MAC|Principalmente usado para PCs|
|Permite para metadeta| Não permite metadeta|

## Estrutura do arquivo AIFF

O **EA IFF 85** estabelece uma estrutura geral para armazenar dados em arquivos. Um arquivo **EA IFF 85** consiste em vários blocos de dados. Um bloco de construção de um arquivo AIFF consiste em algumas informações de cabeçalho seguidas de dados:
{{< figure src="../chunk.png" alt="Pedaço AIFF" >}}

Um arquivo AIFF é uma coleção de vários tipos diferentes de pedaços. Existem dois tipos gerais de blocos que são importantes para formar um bloco de arquivo AIFF:
- **Common Chunk**: Contém parâmetros importantes que descrevem o som amostrado, como comprimento e taxa de amostragem.
- **Sound Data Chunk**: Contém as amostras de áudio reais.
Existem muitos outros blocos opcionais que listam os parâmetros do instrumento, definem marcadores, armazenam informações específicas do aplicativo, etc.

### Tipos de pedaços locais

Os tipos de pedaços para formar AIFF são fornecidos na tabela abaixo:

|Tipo de Bloco| Descrição|
---|---|
|Common Chunk|O Common Chunk descreve os parâmetros fundamentais do som amostrado|
|Sound Data Chunk|O Sound Data Chunk contém os quadros de amostra reais|
|Marker Chunk|O Marker Chunk contém marcadores que apontam para posições nos dados de som|
|Instrument Chunk|O Instrument Chunk define os parâmetros básicos que um instrumento, como um sampler, pode usar para reproduzir os dados de som|
|MIDI Data Chunk|O MIDI Data Chunk pode ser usado para armazenar dados MIDI|
|Audio Recording Chunk|O Audio Recording Chunk contém informações pertinentes aos dispositivos de gravação de áudio|
|Application Specific Chunk|O Application Specific Chunk pode ser usado para qualquer finalidade pelos fabricantes de aplicativos|
|Comments Chunk|O Comments Chunk é usado para armazenar comentários no FORM AIFF|
|Pedaços de Texto - Nome, Autor, Direitos Autorais, Anotação| Todos são pedaços de texto|

## Referências ##

* [Formato de arquivo de intercâmbio de áudio - pela Wikipedia](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)

