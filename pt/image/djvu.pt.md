{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo djvu", "formato de arquivo djvu", "o que é um arquivo djvu", "arquivo", "exemplo djvu", "extensão de arquivo djvu", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo DJVU",
  "description":"Saiba mais sobre o formato de arquivo DJVU e APIs que podem criar e abrir arquivos DJVU.",
  "linktitle" : "DJVU",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo DJVU?

DjVu, pronunciado como “déjà vu”, é um formato de arquivo gráfico destinado a documentos e livros digitalizados, especialmente aqueles que contêm a combinação de texto, desenhos, imagens e fotografias. Foi desenvolvido pela AT&T Labs. Ele usa várias técnicas, como separação de camadas de imagem de texto e imagens de fundo, carregamento progressivo, codificação aritmética e compactação com perdas para imagens bitonais. Como o arquivo DJVU pode conter imagens coloridas, fotografias, textos e desenhos compactados e de alta qualidade e pode ser salvo em menos espaço, ele é usado na web como eBooks, manuais, jornais, documentos antigos etc.

O DjVu pode ser classificado como uma alternativa superior ao [PDF](/pt/pdf/). As extensões de arquivo associadas ao DjVu são .DJVU ou .DJV. O DjVu pode atingir taxas de compactação cerca de 5 a 10 melhores do que os métodos existentes, como [JPEG](/pt/image/jpeg/) e [GIF](/pt/image/gif/) para documentos coloridos e 3 a 8 vezes melhor do que [TIFF]( /image/tiff/) em documentos em preto e branco. Documentos digitalizados em 300 DPI com cores de até 25 MB podem ser compactados em até 30 a 100 KB. Da mesma forma, documentos em preto e branco podem ser compactados de até 5 a 30 KB. A página HTML média pode ter até 50 KB, portanto, esses documentos podem ser carregados na rede sem nenhum problema.

## Breve história ##

A tecnologia DjVu foi desenvolvida nos laboratórios da AT&T por [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3% A9on_Bottou), Patrick Haffner e Paul G de 1996 a 2001. O formato de arquivo DjVu passou por várias revisões, sendo a mais recente de 2005.


|Versão|Data de lançamento|Notas
---|---|---|
|1–19|1996–1999|Estas são as versões de desenvolvimento.
|20|Abril de 1999|A página única foi alterada para o formato de várias páginas.
|23|julho de 2002|pedaço CID
|24|Fevereiro 2003|LTAnno pedaço
|21|Setembro 1999|Formato de armazenamento indireto substituído. Camada de pesquisa de texto foi adicionada.
|22|Abril 2001|Orientação da página, cor JB2
|25|Maio 2003|Número NAVM. Suporte para marcadores DjVu foi adicionado.
|26|Abril de 2005|Anotações de texto/linha

## Formato de arquivo DjVu ##

Os documentos DjVu são arquivos IFF85. A estrutura fornece uma hierarquia de contêineres que contém informações em um arquivo DjVu. Esses contêineres também são chamados de "Pedaços". O tipo de pedaço e o ID do pedaço descrevem como o pedaço é usado. Há um cabeçalho de 4 bytes seguido pela estrutura IFF. Os primeiros quatro bytes de um arquivo DjVu são 0x41 0x54 0x26 0x54. Esta seção discute os vários tipos de documentos DjVu e os blocos correspondentes dos quais eles consistem.


|ID do bloco|Uso
---|---|
|FORM|O fragmento composto com os primeiros quatro bytes de dados do fragmento FORM que são identificadores secundários.
|FORM:DJVM|Um documento DjVu de várias páginas. Parte composta que contém a parte DIRM.
|FORM:DJVU|Documento DjVu de página única. Parte composta que contém as partes que compõem uma página em um documento djvu.
|FORM:DJVI|Um arquivo DjVu “compartilhado” que é incluído através do bloco INCL. Anotações compartilhadas e dicionário de formas.
|FORM:THUM|Parte composta que contém as partes TH44 que são as miniaturas incorporadas.
|DIRM|Informações de nome de página para documentos de várias páginas.
|NAVM|Informações de favoritos
|ANTa, ANTz|Anotações incluindo configurações de visualização inicial e hiperlinks sobrepostos, caixas de texto, etc.
|TXTa, TXTz|Unicode Texto e informações de layout.
|Djbz|Tabela de formas compartilhadas.
|Sjbz|BZZ dados bitonais JB2 compactados usados para armazenar máscara.
|FG44|IW44 dados usados para armazenar o primeiro plano
|BG44|dados IW44 usados para armazenar o plano de fundo
|TH44|IW44 dados usados para armazenar imagens em miniatura incorporadas
|WMRM|Dados JB2 necessários para remover uma marca d'água
|FGbz|Dados JB2 em cores. Fornece uma cor para cada (blit ou shape?) no bloco Sjbz correspondente.
|INFO|Informações sobre a página de um DjVu
|INCL|O ID de um bloco FORM:DJVI incluído.
|BGjp|fundo codificado em JPEG
|FGjp|Primeiro plano codificado em JPEG
Máscara codificada |Smmr|G4

### Compressão DJVU

Uma única imagem é dividida em muitas imagens diferentes e, em seguida, cada imagem é compactada separadamente. Para a criação de um arquivo DjVu a imagem é primeiro separada em três imagens, uma imagem de fundo, primeiro plano e uma imagem de máscara. Normalmente, as imagens de plano de fundo e primeiro plano são imagens coloridas de resolução mais baixa; mas a imagem da máscara é uma imagem de resolução mais alta e normalmente o texto é armazenado lá. Após a separação, as imagens de primeiro plano e de fundo são comprimidas através de um algoritmo de compressão baseado em wavelet IW44, enquanto a imagem de máscara é comprimida usando outro método chamado JB2.

O método de codificação JB2 elimina grande parte da redundância na imagem de texto ao identificar formas idênticas na página, como várias ocorrências de um caractere em uma fonte específica. O JB2 primeiro codifica o bitmap de cada forma exclusiva, aproveitando a redundância entre formas semelhantes. Em seguida, ele codifica os locais em que cada forma aparece na página. Tanto o JB2 quanto o IW44 contam com um novo tipo de codificador aritmético binário adaptativo chamado ZP-coder, que elimina qualquer redundância restante dentro de alguns por cento do limite de Shannon. O codificador ZP é adaptável e mais rápido do que outros codificadores aritméticos binários aproximados.

## Referências ##

* [DjVu - Wikipedia](https://en.wikipedia.org/wiki/DjVu)
* [Formato de arquivo DjVu](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)

