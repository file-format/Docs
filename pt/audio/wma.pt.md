{
  "date" : "2021-02-20",
  "keywords" :[ "WMA", "arquivo", "extensão", "formato", "formato de arquivo de intercâmbio de áudio", "música" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo WMA e APIs que podem criar e abrir arquivos WMA.",
  "title" :"WMA - Arquivo de áudio do Windows Media",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## O que é um arquivo WMA?

Um arquivo com extensão .wma representa um arquivo de áudio salvo no formato Advanced Systems Format (ASF). ASF é o formato proprietário da Microsoft que contém fluxos de bits codificados pelo Windows Media Audio 9. Além do conteúdo de áudio, um arquivo WMA também contém objetos de metadados, como título, álbum, artista e gênero da faixa. Os arquivos WMA são usados principalmente para streaming pela Web, semelhantes aos arquivos [.mp3](/pt/audio/mp3/).

## Formato de arquivo WMA

Um arquivo WMA é um formato de arquivo binário e está contido no formato de arquivo ASF. Especifica a codificação de metadados sobre o arquivo semelhante às tags ID3 usadas pelos arquivos MP3. O codec WMA tem sido usado pela Microsoft em seu Protected Interoperable File Format (PIFF) desde 2008. No entanto, ele não foi declarado como codec de áudio padronizado pelos padrões da indústria relacionados, como DECE UltraViolet e MPEG-DASH.

### Dados específicos do tipo WMA

As informações específicas do tipo para o codec de áudio do Windows Media são armazenadas no formato a seguir como parte dos dados específicos do tipo do objeto de propriedades de fluxo.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Referências

* [Visão geral do ASF - Microsoft](https://learn.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format)

