{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX - Codec de vídeo de alta eficiência",
  "description":"Saiba mais sobre o formato de arquivo IDX e APIs que podem criar e abrir arquivos IDX.",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## O que é um arquivo IDX?

Um arquivo IDX é um arquivo de índice de legendas que aponta para a lista de informações de metadados para legendas dentro de um arquivo .sub (VobSub Subtitles). Ele é criado e usado pelo aplicativo de software VobSub que permite aos usuários extrair legendas de DVDs e despejá-las em um arquivo SUB. Os arquivos IDX contêm carimbos de data e hora e deslocamentos de bytes usados para apontar para cada legenda. VobSub sempre cria um arquivo IDX junto com o arquivo SUB correspondente.

## Formato de arquivo IDX - Mais informações

Os arquivos IDX são gerados e salvos como arquivos de texto simples que podem ser abertos em qualquer editor de texto. Um arquivo IDX contém informações que são lidas pelos players de mídia para ler parâmetros como a cor do texto da legenda a ser exibida na tela, a posição do texto da legenda na tela.

### Configurações de legendas IDX

Um arquivo IDX típico armazena essas informações de metadados no início do arquivo. As configurações de legenda começam com um **#**. Carimbos de data e hora e referências de imagem são adicionados após todas essas configurações de legendas e começam com **timestamp:**.

## Exemplo de formato de arquivo IDX

```
# VobSub index file, v7 (do not modify this line!)
#
# To repair desyncronization, you can insert gaps this way:
# (it usually happens after vob id changes)
#
#	 delay: [sign]hh:mm:ss:ms
#
# Where:
#	 [sign]: +, - (optional)
#	 hh: hours (0 <= hh)
#	 mm/ss: minutes/seconds (0 <= mm/ss <= 59)
#	 ms: milliseconds (0 <= ms <= 999)
#
#	 Note: You can't position a sub before the previous with a negative value.
#
# You can also modify timestamps or delete a few subs you don't like.
# Just make sure they stay in increasing order.


# Settings

# Original frame size
size: 720x576

# Origin, relative to the upper-left corner, can be overloaded by aligment
org: 0, 0

# Image scaling (hor,ver), origin is at the upper-left corner or at the alignment coord (x, y)
scale: 100%, 100%

# Alpha blending
alpha: 100%

# Smoothing for very blocky images (use OLD for no filtering)
smooth: OFF

# In millisecs
fadein/out: 50, 50

# Force subtitle placement relative to (org.x, org.y)
align: OFF at LEFT TOP

# For correcting non-progressive desync. (in millisecs or hh:mm:ss:ms)
# Note: Not effective in DirectVobSub, use "delay: ... " instead.
time offset: 0

# ON: displays only forced subtitles, OFF: shows everything
forced subs: OFF

# The original palette of the DVD
palette: 000000, 828282, 828282, 828282, 828282, 828282, 828282, ffffff, 828282, bababa, 828282, 828282, 828282, 828282, 828282, 828282

# Custom colors (transp idxs and the four colors)
custom colors: OFF, tridx: 1000, colors: 000000, bababa, 828282, 000000

# Language index in use
langidx: 0

# English
id: en, index: 0
# Decomment next line to activate alternative name in DirectVobSub / Windows Media Player 6.x
# alt: English
# Vob/Cell ID: 1, 1 (PTS: 0)
timestamp: 00:01:25:880, filepos: 000003800
timestamp: 00:01:46:160, filepos: 000008000
timestamp: 00:02:08:880, filepos: 00000c800
# Vob/Cell ID: 1, 2 (PTS: 222840)
timestamp: 00:03:58:800, filepos: 000011000
timestamp: 00:04:00:680, filepos: 000016800
timestamp: 00:04:04:640, filepos: 00001d800
```

## Como usar o arquivo IDX?

Se você tiver os arquivos Sub e IDX para um filme, poderá reproduzir essas legendas junto com o filme para o qual foram criadas. Muitos aplicativos, como VLC, GOM Player, PotPlayer ou PowerDVD, têm a capacidade de carregar esses arquivos SUB e IDX e reproduzi-los ao lado do filme. Os aplicativos de software também podem incorporar arquivos de legenda SUB e IDX em arquivos [.mkv](/pt/video/mkv/).

## Converter IDX para SRT

O [SRT](/pt/video/srt/) (formato de arquivo SubRip) é um arquivo de legenda simples salvo no formato de arquivo SubRip. É mais comumente usado em comparação com o formato de arquivo VobSub. Assim, se você deseja converter arquivos SUB/IDX para o formato de arquivo SRT, existem ferramentas de terceiros disponíveis que podem ser usadas para conseguir isso. O conversor SUB/IDX para SRT, disponível em SubtitleTools.com, é uma dessas ferramentas que recebe arquivos SUB e IDX como entrada e converte essas legendas VobSub em arquivos SRT.

## Referências

* [VobSub](https://www.videohelp.com/software/VobSub)
* [VOBsub - Wiki Multimídia](https://wiki.multimedia.cx/index.php?title=VOBsub)

