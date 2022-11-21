{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - Formato de definição de canal",
  "description" :"Saiba mais sobre o que é um arquivo CDF e APIs que podem criar e abrir arquivos CDF.",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## O que é um arquivo CDF?

Um arquivo com extensão .cdf é um formato de arquivo de distribuição de informações baseado em XLM que foi usado para publicar atualizações frequentes como "canais". A informação é publicada a partir de qualquer servidor web e é entregue automaticamente a computadores com programas de recepção compatíveis, como navegadores web. Os usuários se inscrevem em canais ativos e têm atualizações agendadas entregues em sua área de trabalho.
Os arquivos CDF foram usados anteriormente em conjunto com as tecnologias Active Channel, Active Desktop e Smart Offline Favorites da Microsoft.

## Formato de arquivo CDF

Os arquivos CDF são salvos como arquivos XML, que é um formato genérico de arquivo da Web para troca de informações. O formato de arquivo CDF é um formato antigo agora e nunca foi amplamente adotado. Em comparação a isso, o RSS da Netscape era mais famoso e amplamente utilizado.

### Exemplo de formato de arquivo CDF

O seguinte é um exemplo genérico do formato de arquivo CDF.

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://domínio/pasta/"
ÚLTIMO MOD="1998-11-05T22:12"
PRECACHE="SIM"
NÍVEL="0">
<TITLE>Título do canal</TITLE>
<ABSTRACT>Sinopse do conteúdo do canal.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    ÚLTIMO MOD="1998-11-05T22:12"
    PRECACHE="SIM"
NÍVEL="1">
<TITLE>Título da página dois</TITLE>
<ABSTRACT>Sinopse do conteúdo da Página Dois.</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## Referências

* [Channel Definition Format - By Wikipedia](https://en.wikipedia.org/wiki/Channel_Definition_Format)

