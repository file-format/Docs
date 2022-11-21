{
  "date" : "2022-05-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo GDB - Arquivo ESRI Arquivo Geodatabase",
  "description":"Saiba mais sobre o formato de arquivo GDB e APIs que podem criar e abrir arquivos GDB.",
  "linktitle" : "GDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-08"
}

## O que é um arquivo GDB?

O arquivo ESRI Geodatabase (FileGDB) é uma coleção de arquivos em uma pasta em disco que contém dados geoespaciais relacionados, como conjuntos de dados de recursos, classes de recursos e tabelas associadas. Ele requer que alguns outros arquivos sejam mantidos junto com o arquivo .gdb no mesmo diretório para que funcione. As consultas podem ser executadas no arquivo .gdb para gerenciar dados espaciais e não espaciais.

## Formato de arquivo GDB - Mais informações

Os geodatabases de arquivos são compostos por sete tabelas de sistema mais dados do usuário. Os dados do usuário podem ser armazenados nos seguintes tipos de conjuntos de dados:

* Classe de recurso
* Conjunto de dados de recursos
* Conjunto de dados do mosaico
* Catálogo Raster
* Conjunto de dados raster
* Conjunto de dados esquemático
* Tabela (não espacial)
* Caixas de ferramentas

Os conjuntos de dados de recursos podem conter classes de recursos, bem como os seguintes tipos de conjuntos de dados:

* Anexos
* Anotação vinculada ao recurso
* Redes geométricas
* Conjuntos de dados de rede
* Tecidos para encomendas
* Aulas de relacionamento
* Terrenos
* Topologias

O tamanho máximo padrão de conjuntos de dados em geodatabases de arquivo é 1 TB. O tamanho máximo pode ser aumentado para 256 TB para grandes conjuntos de dados (geralmente raster). Isso é controlado por uma palavra-chave de configuração. Consulte Palavras-chave de configuração para geodatabases de arquivo para obter mais informações.

Os geodatabases de arquivos também podem conter subtipos e domínios e participar de replicação de check-in/check-in e réplicas unidirecionais.

Um arquivo geodatabase pode ser acessado simultaneamente por vários usuários. Se os usuários estiverem editando, eles deverão editar conjuntos de dados diferentes.

## Especificações de formato de arquivo GDB ##

O arquivo GDB é um formato proprietário da ESRI e suas especificações não estão disponíveis publicamente. Devido a esse motivo, os detalhes do formato de arquivo para FIle GDB não puderam ser documentados em nenhum outro lugar além de algumas fontes que o fizeram [parcialmente] (https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec) por engenharia reversa .

## Referências ##

* [Especificações do FGDB](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec)

