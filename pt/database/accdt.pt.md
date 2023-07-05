{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDT", "extensão", "arquivo", "formato de arquivo", "Tipo de arquivo de banco de dados", "Formato de arquivo de banco de dados", "Arquivos de banco de dados" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo ACCDT e APIs que podem criar e abrir arquivos ACCDT.",
  "title" :"ACCDT - Formato de arquivo de banco de dados de modelo do Microsoft Access 2007",
  "linktitle" : "ACCDT",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## O que é um arquivo ACCDT?

Um arquivo com extensão .accdt é um arquivo de modelo de banco de dados do Microsoft Access que contém elementos de banco de dados predefinidos. Esses elementos são uma coleção de estruturas que definem um aplicativo de banco de dados, como esquemas de banco de dados para armazenamento de dados, descrição de layout para visualizações dos dados e metadados que descrevem o banco de dados. Sendo arquivos de modelo, os arquivos ACCDT podem ser usados para criar bancos de dados com base nas configurações de modelo disponíveis neles. Os arquivos de banco de dados resultantes são salvos como arquivos [ACCDB](/pt/database/accdb/) e preenchidos com dados em tabelas. O Microsoft Access 2007 e posteriores podem abrir arquivos ACCDT.

## Formato de arquivo ACCDT

Os arquivos de modelo ACCDT são baseados nas especificações do Office Open XML e todos os dados estão contidos em um pacote ZIP. As informações de estrutura e conteúdo do banco de dados estão contidas nos arquivos [XML](/pt/web/xml/) e arquivos de texto e vinculadas entre si por meio de relacionamentos. Você pode renomear um arquivo ACCDT para a extensão [.zip](/pt/compression/zip/) e usar qualquer software de compactação para extrair o conteúdo do arquivo ZIP.

### Estrutura do arquivo

Os arquivos ACCDT são pacotes que contêm uma coleção de partes relacionadas. Cada **parte** armazena informações sobre o conteúdo de um aplicativo de banco de dados usando formatos XML, texto e binários, incluindo:

* Objetos de banco de dados
* Metadados associados
* Estrutura do pacote

#### Pacote

Um pacote é um arquivo [ZIP](/pt/compression/zip/) que contém várias partes e está em conformidade com as convenções de embalagem aberta especificadas em [ISO/IEC-29500-2](https://www.iso.org/standard/51459.html). Os arquivos ACCDT devem conter pelo menos uma parte do Metadaa do modelo que deve ser o destino de um relacionamento. Esses Metadados de Modelo são a parte inicial de um arquivo ACCDT.

#### Papel

Uma parte é um fluxo de bytes que possui um tipo associado para especificar a natureza e o tipo de conteúdo armazenado nele. A enumeração de partes especifica partes válidas, tipos de conteúdo válidos e relacionamentos necessários entre todas as partes em um pacote.

#### Relação

`Package Relationship` - onde o destino é uma parte e a origem é o pacote como um todo.

`Relação Parte a Parte` - onde o destino é uma parte e a origem é uma parte do pacote.

`Relacionamento explícito` - onde um recurso é referenciado a partir do conteúdo de uma parte de origem, referenciando um elemento de relacionamento pelo valor de seu atributo ID.

`Relação Implícita` - uma relação que não é explícita.

`Relacionamento interno` - onde o alvo faz parte do pacote.

`Relação externa` - onde o destino é um recurso externo que não está no pacote.

## Referências ##

* [Formato de arquivo de modelo de acesso](https://docs.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

