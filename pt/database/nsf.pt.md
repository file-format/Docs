{
  "date" : "2020-11-11",
  "keywords" :[ "NSF", "extensão", "arquivo", "formato de arquivo", "Tipo de arquivo de banco de dados", "Formato de arquivo de banco de dados", "Arquivos de banco de dados" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo NSF e APIs que podem criar e abrir arquivos NSF.",
  "title" :"Formato de arquivo NSF - Formato de banco de dados do Lotus Notes",
  "linktitle" : "NSF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## O que é um arquivo NSF?

Um arquivo com extensão .nsf (Notes Storage Facility) é um formato de arquivo de banco de dados usado pelo [software IBM Notes](https://en.wikipedia.org/wiki/HCL_Domino), anteriormente conhecido como Lotus Notes. Ele define o esquema para armazenar diferentes tipos de objetos, como e-mails, compromissos, documentos, formulários e visualizações. Todas essas informações estão contidas em um único arquivo NSF para colaboração empresarial semelhante a um arquivo PST/OST. Alguns dos aplicativos que podem abrir arquivos NSF incluem IBM Lotus Notes e IBM Domino.

## Especificações de formato de arquivo NSF

Os arquivos NSF são de natureza binária e suas especificações estão disponíveis por Joachim Metz no [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc). De acordo com esses detalhes, um arquivo NSF é composto por:

* Cabeçalho do arquivo
* Cabeçalho do banco de dados

Além disso, é composto por:

* Superbloco
* Bloco descritor de balde
* Bitmap
* Registrar bucket de vetor de realocação
* buckets de resumo
* buckets não-resumo


### Cabeçalho do arquivo NSF

O cabeçalho do arquivo NSF tem 6 bytes de tamanho. Isso consiste de:

|Deslocamento|Tamanho|Valor|Descrição|
---|---|---|---|
0|2|0x1a 0x00|Assinatura|
2|4| |O tamanho do cabeçalho do banco de dados|

### Cabeçalho do banco de dados

O cabeçalho do banco de dados NSD contém os seguintes valores confirmados.

* Informações do banco de dados
* Identificador de banco de dados (DBID)
*Informações de replicação
* Sinalizadores de buffer de informações do banco de dados
* Título
* Categorias
* Classe
* Classe de design (nome do modelo)
* Identificadores de notas especiais
* Preenchimento
* Informações do banco de dados 2
* Informações do banco de dados 3
* Informações do banco de dados 4
* Informações do banco de dados 5
* Preenchimento
* Identificador de instância de banco de dados (DBIID)
* Histórico de replicação

## Referências
* [Formato NSF - Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)
