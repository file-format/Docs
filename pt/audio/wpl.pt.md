{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "arquivo wpl", "extensão", "formato", "o que é um arquivo wpl", "música", "formato de arquivo wpl"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo WPL e APIs que podem criar, converter e abrir arquivos WPL.",
  "title" :"WPL - Arquivo de lista de reprodução do Windows Media Player",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## O que é um arquivo WPL?

Um arquivo com extensão .wpl contém a lista de reprodução de músicas a serem executadas no Microsoft Windows Media Player. Esses arquivos geralmente são criados pelos usuários para suas coleções de vídeo e áudio. O conteúdo escrito em um arquivo WPL é apenas caminhos ou locais de diretório para os arquivos multimídia selecionados pelo criador do arquivo .wpl, de modo que o aplicativo media player possa localizar e reproduzir imediatamente o conteúdo multimídia de seus locais de diretório.

## Formato de arquivo WPL

WPL (Windows Media Player Playlist) é um formato de arquivo proprietário usado no Microsoft Windows Media Player versões 9 ou superiores. É um formato de arquivo de computador que armazena listas de reprodução multimídia. Por padrão, a lista de reprodução é salva com uma extensão .wpl(Windows Media Player Playlist). Você pode usar a extensão [.m3u](/pt/audio/m3u/) se quiser reproduzir seus discos de dados em um dispositivo que não suporta essa extensão. Os elementos de um arquivo WPL são representados no formato XML.

O elemento de nível superior "smil" especifica que os elementos do arquivo seguem a estrutura SMIL (Synchronized Multimedia Integration Language). O arquivo é criado e salvo com a extensão .wpl e seu tipo MIME é application/vnd.ms-wpl.

### Exemplo WPL

Aqui está um exemplo de um arquivo wpl:
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## Referências ##

* [MPEG-1 Audio Layer II - Por Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

