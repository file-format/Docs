{
  "date" : "2021-03-18",
  "keywords" :[ "arquivo qgz", "formato de arquivo qgz", "o que é um arquivo qgz", "arquivo", "exemplo qgz", "extensão de arquivo qgz", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGZ - Projeto Comprimido GIS Quantum",
  "description":"Aprenda sobre o formato de arquivo QGZ, que é apenas um QGS compactado e APIs que podem criar e abrir arquivos QGZ.",
  "linktitle" : "QGZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## O que é um arquivo QGZ?

O formato de arquivo **QGZ** é um arquivo compactado que contém um arquivo [QGS](https://docs.fileformat.com/gis/qgs/) e um arquivo QGD. Considerando que, o arquivo QGD é o banco de dados sqlite do projeto qgis que consiste em dados auxiliares para o projeto. Se não houver dados auxiliares, o arquivo QGD permanecerá vazio.

## Detalhes sobre o formato de arquivo QGZ

O QGZ foi introduzido como uma nova variante do **formato de arquivo de projeto QGIS 3**. Este formato é um contêiner compactado para o arquivo xml QGS. Se os usuários escolherem QGD que é um formato opcional, neste caso o container é benéfico para armazenar o banco de dados de armazenamento auxiliar.

No modo clássico, o banco de dados auxiliar é salvo como um arquivo com extensão .qgd junto com o arquivo xml. Ao escolher o container compactado, o arquivo .qgd inclui no .qgz, apenas facilita os usuários sem nenhum problema, os usuários não podem excluí-lo ou esquecer de copiá-lo ao compartilhar arquivos de projeto!


## Referências

* [QGZ – Um novo formato de arquivo de projeto padrão para QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [Formatos de arquivo QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

