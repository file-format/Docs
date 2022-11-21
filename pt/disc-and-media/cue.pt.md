{
  "date" : "2021-06-09",
  "keywords" :[ "cue", "arquivo", "extensão", "formato", "o que é um arquivo cue", "música", "formato do arquivo cue", "especificação do formato do arquivo cue", "folha cue", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo CUE e APIs que podem criar, converter e abrir arquivos CUE.",
  "title" :"CUE - Arquivo de folha de sugestões",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## O que é um arquivo CUE?

Um arquivo com extensão .cue, também conhecido como arquivo cue sheet, é um arquivo de metadados que contém informações sobre o layout das faixas em um CD ou DVD. Eles são suportados por reprodutores de mídia e aplicativos de criação de discos ópticos. Os principais dados de áudio armazenados no CD são referenciados pelo arquivo cue, juntamente com as especificações de duração das faixas, títulos de disco e artistas. Assim, se um único arquivo de áudio contém várias faixas, o arquivo cue pode ser usado para dividir o áudio em vários arquivos ou fazer referência a várias faixas.

## Formato de arquivo CUE

Os arquivos CUE ou cue sheet são armazenados em formato de texto simples que pode ser lido por humanos. As informações em um arquivo cue são comandos com um ou mais parâmetros. Esses comandos se aplicam ao arquivo inteiro ou a uma faixa individual, dependendo do comando específico e do contexto. O guia do usuário CDRWIN descreve as especificações para a sintaxe e semântica da folha de sinalização.

## Comandos Essenciais da Folha de CUE

|Comando|Descrição|
---|---|
|ARQUIVO| Refere-se ao arquivo que contém os dados e seu formato, como [MP3](/pt/audio/mp3/), [WAV](/pt/audio/wav/), ou imagem de disco binário simples)|
|TRILHA| Define as informações de contexto da faixa, como seu número e tipo ou modo.|
|ÍNDICE| Representa a posição como um índice dentro do FILE. O formato é mm:ss:ff (quadro minuto-segundo).|
|PREGAP e POSTGAP|Indica o pré-gap ou pós-gap de uma trilha, que não está armazenada em nenhum arquivo de dados. O comprimento é especificado no mesmo formato de quadro minuto-segundo para INDEX.|

### Exemplo de planilha CUE

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## Referências

* [arquivo .cda - Por Wikipedia](https://en.wikipedia.org/wiki/.cda_file)

