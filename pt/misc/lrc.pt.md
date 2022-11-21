{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo LRC - O que é um arquivo LRC?",
  "description":"Saiba mais sobre o arquivo LRC Lyric e as APIs que podem criar e abrir arquivos LRC.",
  "linktitle" : "LRC",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## O que é um arquivo LRC?

Um arquivo LRC é um arquivo de letras baseado em texto que contém as letras de uma música de áudio. Quando a música de áudio é reproduzida com um reprodutor de música ou software de reprodutor de áudio em um computador, o arquivo LRC é lido em paralelo e exibido com o tempo. Os arquivos LRC contêm pontos de sinalização para exibição de letras quando a música está tocando. Em geral, os arquivos LRC têm o mesmo nome do arquivo de áudio correspondente, como audio.mp3 e audio.lrc. Os arquivos LRC são semelhantes aos arquivos de legendas como [SRT](/pt/video/srt/).

## Formato de arquivo LRC - Mais informações

Os arquivos de formato de letra LRC são salvos como arquivos de texto simples e podem ser abertos e editados em um arquivo de texto. O conteúdo de um arquivo LRC contém informações de cores para exibição do texto das letras.

## Formatos LRC

Existem vários formatos de arquivos LRC que foram desenvolvidos ao longo do tempo. Esses

### Formato LRC Simples

As tags de tempo de linha estão no formato [mm:ss.xx] onde mm são minutos, ss são segundos e xx são centésimos de segundo.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### Formato Simples Estendido

Inclui a capacidade de alterar e especificar o gênero das letras usando M: Masculino, F: Feminino, D: Dueto.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Formato LRC aprimorado

O formato LRC aprimorado é uma versão estendida do formato LRC Simples. Adiciona um Word Time Tag no formato<mm:ss.xx> no final da palavra anterior.

```
[ar: Jade Michael]
[al: Sarah Hi]
[au: Jade Michael]
[length: 2:58]
[by: lrc-maker]
[ti: Somebody to Love]

[00:00.00] <00:00.04> When <00:00.16> the <00:00.82> truth <00:01.29> is <00:01.63> found <00:03.09> to <00:03.37> be <00:05.92> lies
[00:06.47] <00:07.67> And <00:07.94> all <00:08.36> the <00:08.63> joy <00:10.28> within <00:10.53> you <00:13.09> dies
[00:13.34] <00:14.32> Don't <00:14.73> you <00:15.14> want <00:15.57> somebody <00:16.09> to <00:16.46> love
```

## Referências

* [LRC Lyrics File Format - Wikipedia](https://en.wikipedia.org/wiki/LRC_(file_format))

