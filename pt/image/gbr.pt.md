{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo gbr", "formato de arquivo gbr", "o que é um arquivo gbr", "arquivo", "exemplo gbr", "extensão de arquivo gbr", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo GBR - Formato de arquivo Gerber para PCB",
  "description":"Saiba mais sobre o formato de arquivo GBR e APIs que podem criar e abrir arquivos GBR.",
  "linktitle" : "GBR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo GBR?

Um arquivo com extensão .gbr é um formato de arquivo de imagem Gerber para transferência de dados de projeto de placa de circuito impresso (PCB). Foi desenvolvido pela Ucamco. Os dados de projeto do PCB são o principal componente exigido pela indústria de fabricação para manuseio. Um arquivo GRB contém dados de PCB, como camadas de cobre, máscara de solda, legenda e dados de perfuração e rota. Ele pode ser usado para transferir dados como características de fabricação de PCB, incluindo espessura ou acabamento em um formato padronizado. Todos os sistemas de projeto de PCB geram arquivos Gerber que podem ser manipulados por sistemas de fabricação de PCB. Os arquivos GBR agora se tornaram o padrão de fato para transferência de dados de projeto de placas de circuito impresso (PCB). A Ucamco forneceu um [visualizador online gratuito](https://gerber-viewer.ucamco.com/) para abrir e visualizar formatos de arquivo GBR.

## Formato de arquivo GBR

GBR é um formato legível UTF-8 que consiste em apenas 27 comandos. Devido a esta pequena lista de comandos e sua compacidade, o GBR é fácil de depurar. Gerber em sua essência é um formato vetorial aberto para imagens binárias 2D. A meta-informação é transferida com as imagens por meio de Atributos. Um único arquivo GRB especifica uma única imagem e não requer que nenhum arquivo acompanhante ou parâmetros externos sejam interpretados. Uma imagem precisa de apenas um arquivo. Ele usa caracteres ASCII de 7 bits para todos os comandos e nomes definidos na especificação que podem ser impressos. Isso cobre totalmente a geração de imagem completa.

### Exemplo de arquivo GBR

A seguir está um exemplo de arquivo Gerber que cria um círculo de 1,5 mm de diâmetro centrado na origem. Há um comando por linha.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## Referências

* [Formato Gerber](https://www.ucamco.com/en/gerber)

