{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo CPIO - Formato de arquivo Unix CPIO",
  "description":"Aprenda a saber o que é um arquivo CPIO e APIs que podem criar e abrir arquivos CPIO.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## O que é um arquivo .CPIO?

Um arquivo CPIO é um arquivo criado no formato Copy In Copy Out (CPIO) do Unix. É semelhante ao formato de arquivo TAR, exceto pelo fato de ser descompactado. Os arquivos CPIO podem armazenar arquivos de dispositivos, links simbólicos e atributos de arquivo estendidos.

## Formato de arquivo CPIO

Um arquivo CPIO é criado como um arquivo binário que não é legível por humanos. Ele armazena a coleção de arquivos e diretórios. O conteúdo de um arquivo CPIO é identificado com informações de metadados, como nomes de arquivos, permissões, propriedade e carimbos de data/hora. Essas informações de metadados também são armazenadas no arquivo para acesso lateral pelo sistema.

## Formato do arquivo CPIO

Um arquivo CPIO é composto por um ou mais arquivos membros concatenados. Cada arquivo no arquivo consiste em um cabeçalho opcionalmente seguido pelo conteúdo do arquivo conforme mencionado no cabeçalho. O arquivo contém outro cabeçalho no final que é descrito por um arquivo vazio chamado TRAILER!!.

### Tipos de arquivos CPIO

Existem dois tipos de arquivos CPIO. Estes diferem apenas no estilo do cabeçalho.

* Arquivos ASCII - Esses arquivos CPIO possuem um cabeçalho imprimível que se torna parte do arquivo CPIO se o próprio arquivo consistir em arquivos ASCII
* Arquivos Binários - Esses arquivos CPIO possuem cabeçalhos binários.

## Trabalhando com arquivo CPIO

### Como criar arquivos CPIO?

Você pode criar um CPIO em sistemas do tipo Unix usando o comando **cpio**. O comando a seguir encontrará todos os arquivos e diretórios no diretório atual e seus subdiretórios. Essa saída é então canalizada para o comando cpio que irá gerar um novo arquivo CPIO denominado archive.cpio.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### Como extrair arquivos de arquivos CPIO?

O comando a seguir extrai os arquivos de um arquivo existente.

```
cpio -id < archive_cpio.cpio
```
Ele lerá o arquivo archive.cpio da entrada padrão e extrairá os arquivos para o diretório atual.


## Referências

* [CPIO - Pela Wikipédia](https://en.wikipedia.org/wiki/Cpio)
* [Formato de arquivo CPIO](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

