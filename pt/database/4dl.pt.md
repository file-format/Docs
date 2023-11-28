{
  "date" : "2023-06-14",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aprenda sobre o formato de arquivo 4DL e APIs que podem criar e abrir arquivos 4DL.",
  "title" :"4DL - Arquivo de log do banco de dados de 4ª dimensão",
  "linktitle" : "4DL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-06-14"
}

## O que é um arquivo .4DL?

Um arquivo de log 4DL é utilizado para registrar as modificações feitas em um arquivo de banco de dados 4D (.4DD). Este arquivo é armazenado junto com o arquivo de banco de dados e compartilha um nome de arquivo semelhante. Seu objetivo é rastrear e manter com precisão um registro abrangente das atualizações implementadas no banco de dados. Um [arquivo 4DD](/pt/database/4dd/), em comparação com o arquivo 4DL, é associado principalmente com as 4ª Dimensões pela 4D Inc.

## Formato de arquivo 4DL – Mais informações

Normalmente, vários arquivos 4DL são armazenados juntos com um arquivo 4DD. Assim, a primeira versão do arquivo de log pode ser nomeada como 0001.4dl, mas as versões laterais dos arquivos de log serão salvas como 0002.4dl, 0003.4dl e assim por diante. Agora, se o próprio arquivo de log passar por três salvamentos subsequentes, ele será rotulado como "db1[0005-0003].4dl".

## Referências

* [4DD - Wikipedia](https://en.m.wikipedia.org/wiki/4th_Dimension_(software))
