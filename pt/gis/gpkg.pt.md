{
  "date" : "2021-07-29",
  "keywords" :[ "arquivo gpkg", "formato de arquivo gpkg", "o que é um arquivo gpkg", "arquivo", "exemplo gpkg", "extensão de arquivo gpkg","extensão", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPKG - Arquivos de Formato GeoPackage",
  "description":"Saiba mais sobre o formato de arquivo GPKG e APIs que podem criar e abrir arquivos GPKG.",
  "linktitle" : "GPKG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## O que é um arquivo GPKG?
Um arquivo com extensão .gpkg consiste em um sistema de informações geográficas implementado como um contêiner de banco de dados SQLite contendo tabelas de dados e metadados com definições típicas, limitações de formato, declarações de integridade e restrições de conteúdo. Foi publicado em 2014; definido pelo OGC (Open Geospatial Consortium) em nome dos militares dos EUA. Vários governos, organizações comerciais e de código aberto apoiam amplamente o GeoPackage.

## Formato de arquivo GPKG
Um GeoPackage é formado como um arquivo de banco de dados SQLite 3 estendido; um padrão define um conjunto de regras (convenções obrigatórias) para:
- Armazenar conjuntos de imagens de matrizes de blocos
- Recursos vetoriais
- Mapas raster em várias escalas
- Metadados e esquema

Você pode estender um GeoPackage usando as regras de extensão definidas na cláusula 2.3 do padrão. O objetivo de projetar um GeoPackage foi tornar um banco de dados leve o máximo possível e incluí-lo em um único arquivo pronto para uso. Isso o torna ideal para aplicativos móveis no modo off-line e compartilhamento rápido em armazenamento em nuvem ou dispositivos de armazenamento USB, etc.

### Conteúdo GPKG
Os GeoPackages contêm várias tabelas, como outros bancos de dados relacionais. Essas tabelas podem ser definidas pelo usuário ou tabelas de metadados. Os GeoPackages consistem em duas tabelas de metadados obrigatórias:

#### gpkg_contents
Um índice para um GeoPackage. As colunas obrigatórias nesta tabela são:

- **table_name**: o nome real da tabela de dados definida pelo usuário;
- **data_type**: o tipo de dado, por exemplo, títulos, características e atributos;
- **identificador e descrição**: texto legível por humanos;
- **last_change**: a data informativa da última alteração, no formato ISO 8601 ;
- **min_x, min_y, max_x e max_y**: as extensões espaciais do conteúdo. ;
- **srs_id**: sistema de referência espacial.

#### gpkg_spatial_ref_sys
Para conteúdo de referência espacial; incluindo, mas não limitado a blocos e recursos, cada linha no conteúdo deve fazer referência a um sistema de referência de coordenadas; armazenados na tabela **gpkg_spatial_ref_sys**. As colunas obrigatórias nesta tabela são:

- **srs_name, description**: um nome legível e uma descrição para o SRS;
- **srs_id**: um identificador único para o SRS; também a chave primária da tabela;
- **organização**: nome que não diferencia maiúsculas de minúsculas da organização definidora.
- **organization_coordsys_id**: ID numérico do SRS atribuído pela organização;
- **definição**: Definição de texto bem conhecido do SRS.


## Referências

* [GeoPackage - por Wikipedia](https://en.wikipedia.org/wiki/GeoPackage)
* [Introdução ao GeoPackage](http://www.geopackage.org/guidance/getting-started.html)

