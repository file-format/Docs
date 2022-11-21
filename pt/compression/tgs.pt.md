{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo tgs", "formato de arquivo tgs", "o que é um arquivo tgs", "arquivo", "exemplo tgs", "extensão de arquivo tgs", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGS - Formato de arquivo de adesivo animado de telegrama",
  "description":"Saiba mais sobre o formato de arquivo TGS e APIs que podem criar e abrir arquivos TGS.",
  "linktitle" : "TGS",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## O que é um arquivo TGS?

Um arquivo com extensão .tgs é um arquivo de adesivo animado que foi introduzido pelo serviço de mensagens multiplataforma [Telegram](https://core.telegram.org/animated_stickers). Adesivos animados são usados por usuários de aplicativos de mensagens para enviar conteúdo mais aprimorado e animado em mensagens, ao contrário dos gráficos estáticos que são imagens estáticas. O Telegram inicialmente usava o formato de arquivo [WEBP](/pt/image/webp/) para adesivos de imagens estáticas. O formato de arquivo TGS pode armazenar dados de animação em resoluções mais altas e tamanho de arquivo menor em comparação com os adesivos WEBP estáticos. Os arquivos TGS podem ser abertos usando aplicativos como Telegram, 7-zip, Apple Archive Utility e Corel WinZip.

## Formato de arquivo TGS

O Telegram introduziu o formato de arquivo TGS em julho de 2019 com base na biblioteca Lottie. Um arquivo TGS consiste em texto [JSON](/pt/web/json/) que é exportado de uma animação no Adobe After Effects. O texto JSON exportado é compactado usando a compactação gzip, que reduz o tamanho do arquivo. As informações JSON sobre o arquivo de texto são armazenadas em arquivo de texto que se torna a base das altas taxas de compactação.

### Especificações dos adesivos TGS

O formato de arquivo TGS impõe certas limitações na criação de adesivos animados TGS. Um arquivo animado TGS:

* O tamanho do adesivo/tela deve ser de 512х512 pixels.
* Objetos adesivos não devem sair da tela.
* A duração da animação não deve exceder 3 segundos.
* Todas as animações devem ser em loop.
* O tamanho do adesivo não deve exceder 64 KB após a renderização no Bodymovin.
* Todas as animações devem ser executadas a 60 quadros por segundo.

### Texto JSON TGS de amostra

Um adesivo animado de amostra, quando descompactado, contém o seguinte conteúdo de texto JSON.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## Referências ##

* [TGS](https://core.telegram.org/animated_stickers)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

