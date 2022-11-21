{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SP3 - Arquivo NGS SP3",
  "description":"Saiba mais sobre o formato de arquivo SP3 e APIs que podem criar e abrir arquivos SP3.",
  "linktitle" : "SP3",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## O que é um arquivo SP3?

Um arquivo com extensão .sp3 é um formato orbital do National Geodetic Survey (NGS) para armazenar informações orbitais. Esta é uma extensão dos formatos SP1 e SP2 do NGS e inclui as informações de correção do relógio do satélite que são computadas simultaneamente com as órbitas. Baseia-se principalmente na posição e no relógio e não inclui velocidades. O formato foi proposto em Remondi, 1989 e foi adotado em 1991. Além das informações de correção do relógio do satélite, inclui informações como expoentes de precisão da órbita, linhas de comentários, a semana GPS e segundos da semana associados à primeira época. Os arquivos SP3 podem ser abertos com o Wolfram Research Mathematica.

## Formato de arquivo SP3 - Mais informações

Os arquivos SP3 são salvos em disco no formato de arquivo ASCII e seu conteúdo pode ser aberto em qualquer editor de texto para visualização. A estrutura de um arquivo SP3 pode ser vista na imagem a seguir.

{{< figure src="../sp3-file-format.png" title="" >}}

## Referências

* [O formato de órbita do produto padrão estendido 3 (SP3-c)](http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20similar ,uma estrutura%20mais%20flexível%20cabeçalho%20)
* [Extensão dos formatos de órbita GPS padrão do levantamento geodésico nacional](https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)

