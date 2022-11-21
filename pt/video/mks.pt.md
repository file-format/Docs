{
  "date" : "2021-24-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo MKS",
  "keywords" :[ "mks", "vídeo matroska", "formato mkv", "arquivo", "formato", "vídeo"],
  "description":"Aprenda sobre o formato de arquivo MKS para legendas criadas apenas pela Matroska e APIs que podem criar e abrir arquivos MKS.",
  "linktitle" : "MKS",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-25-02"
}

## O que é um arquivo MKS?

Os arquivos MKS são geralmente conhecidos como arquivos Matroska contendo apenas legendas. Embora o Matroska seja um container de arquivo geral, ele evita manter as informações de formatos específicos. Como as legendas estão sendo usadas em alguns dos contêineres de áudio ou vídeo, a Matroska está prestando atenção em armazenar alguns formatos comuns de legendas. Ajuda a Matroska a ser consistente com a taxa de crescimento. Você precisa seguir os pontos indicados abaixo para armazenar as legendas no Matroska:

- Os “.mks”. a extensão será usada pelo arquivo Matroska (contendo apenas legendas).
- **CodecPrivate** está sendo usado para armazenar todas as informações relacionadas a codecs que são globais para um fluxo inteiro.
- Remova os carimbos de data/hora de início e fim que são usados em um formato de armazenamento nativo de carimbo de data/hora. Em vez disso, use o carimbo de data/hora e a duração dos blocos.
- Você pode usar qualquer coisa com uma camada transparente, incluindo um vídeo.

## Formatos de legendas comuns

Aqui estão algumas notas breves sobre os formatos de legenda mais comuns armazenados no Matroska:

### Legendas das imagens
O formato de legenda VobSub é o primeiro formato de legenda de imagem a ser importado para o Matroska. Este formato é gerado exportando as legendas de um DVD. As faixas devem ser separadas durante o armazenamento no Matroska se o VobSub consistir em um conjunto de vários fluxos.

### Legendas SRT
O SRT é o mais simples e básico de todos os formatos de legendas. É composto por quatro partes, conforme abaixo:
 



1. Um número que indica a sequência da legenda.
2. O tempo de aparecimento e desaparecimento das legendas na tela.
3. A legenda em si.
4. Uma linha em branco para indicar o início da próxima legenda.
 



### Legendas SSA/ASS
Sub Station Alpha (SSA) é um formato de arquivo usado pelo popular editor de legendas SubStation Alpha. As legendas SSA são amplamente utilizadas pelos fansubbers. Ele tem a capacidade de exibir recursos modernos, por exemplo, karaokê, posicionamento, estilo, etc.
 



### Legendas WebVTT
O World Wide Web Consortium (W3C) desenvolveu o WebVTT que é abreviado como “Web Video Text Tracks Format”. Esse formato está sendo usado para marcar recursos de trilha de texto externos em conexão com o elemento HTML.

### Legendas gráficas de apresentação HDMV
O formato de legenda de gráficos de apresentação HDMV (HDMV PGS) é uma série de bitmaps e não podemos dizer que é texto. Em outras palavras, você pode dizer que é apenas uma sequência cronometrada de imagens gráficas. Para extrair as informações, a conversão de PGS para SRT é um processo necessário.

### legendas de texto HDMV
O texto HDMV é conhecido como o formato de legenda textual usado em Blu-rays. Matroska só permite o conjunto de caracteres UTF-8 Quando armazena as legendas TextST.

### Legendas de transmissão de vídeo digital (DVB)
O formato de legenda DVB foi introduzido para regular a transmissão e exibição de legendas em vários idiomas em sinais de TV. Um formato de legendagem típico também permitiria a qualquer espectador assistir a transmissões legendadas em DVB, independentemente do fabricante dos sistemas de transmissão.


## Referências ##

- [Legendas de Matroska](https://www.matroska.org/technical/subtitles.html)

