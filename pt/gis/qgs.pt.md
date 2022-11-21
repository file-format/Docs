{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo qgs", "formato de arquivo qgs", "o que é um arquivo qgs", "arquivo", "exemplo qgs", "extensão de arquivo qgs","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGS - Formato de arquivo de projeto QGIS",
  "description":"Saiba mais sobre o formato de arquivo QGS e APIs que podem criar e abrir arquivos QGS.",
  "linktitle" : "QGS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo QGS?

Um arquivo com extensão .qgs é um arquivo de projeto criado com [QGIS](https://www.qgis.org/en/site/), que é um aplicativo GIS de plataforma cruzada de código aberto. Todas as configurações do projeto, como propriedades da camada e dados auxiliares para o projeto. Ele é criado quando um projeto de mapa é salvo em disco. Na verdade, é um arquivo de configuração que retém informações como ponteiros para os dados GIS, informações de estilo sobre as camadas e título do projeto. Os arquivos QGS podem ser abertos com o software QGIS que está disponível gratuitamente para download.

## Formato de arquivo QGS

Os arquivos QGS estão no formato [XML](/pt/web/xml/) e armazenam dados de projetos como tags XML. Um arquivo QGS contém informações como:

* título do projeto
*projeto CRS
* a árvore de camadas
* configurações de encaixe
* relações
* a extensão da tela do mapa
* modelos de projetos
* lenda
* docas de visualização de mapas (2D e 3D)
* as camadas com links para os conjuntos de dados subjacentes (fontes de dados) e outras propriedades de camada, incluindo extensão, SRS, junções, estilos, renderizador, modo de mesclagem, opacidade e muito mais.
* propriedades do projeto

### Tags XML de nível superior QGS

{{< figure src="../qgstoplevel.png" title="" >}}

### Tags de camada de projeto de nível superior estendidas

{{< figure src="../qgstoplevel.png" title="" >}}

## Referências

* [QGIS](https://www.qgis.org/en/site/)

