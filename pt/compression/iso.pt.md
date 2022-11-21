{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ISO - Formato de arquivo de imagem de disco",
  "description":"O que é um arquivo ISO e APIs que podem criar e abrir arquivos ISO.",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## O que é um arquivo ISO?

Um arquivo com extensão .iso é um arquivo de imagem de disco de arquivo não compactado que representa o conteúdo de dados inteiros em um disco óptico, como CD ou DVD. Com base no padrão [ISO-9660](https://www.iso.org/standard/17505.html), o formato de arquivo de imagem ISO contém os dados do disco junto com as informações do sistema de arquivos armazenadas nele. A capacidade dos arquivos ISO de conter uma réplica exata do conteúdo o torna o tipo de arquivo perfeito para criar cópias de CDs/DVDs e são usados principalmente para armazenar dados inicializáveis para instalação. Na maioria das vezes, os arquivos ISO são gravados em USB/CD/DVD como conteúdo inicializável para inicializar a máquina para instalação. Os arquivos ISO têm application/x-iso9660-image do tipo MIME.

## Formato de arquivo ISO

O formato de arquivo ISO não é como outros formatos de arquivo de contêiner, embora arquive o conteúdo de dados especificado. O arquivo é criado como um arquivo binário com a estrutura exata do conteúdo e das informações do sistema de arquivos. O formato do arquivo ISO é descrito pelo [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) como segue.

### Estrutura de nível superior do arquivo ISO

A estrutura geral do arquivo consiste em:

* `System Area` - 32.768 bytes e não é utilizado por ISO_9660
* `Área de Dados` - consiste no conjunto de descritores de volume e tabelas de caminho, diretórios e arquivos

### Conjunto de descritores de volume

A área de dados começa com o conjunto de descritores de volume, um conjunto de um ou mais descritores de volume terminados com um terminador de conjunto de descritores de volume. Eles atuam coletivamente como um cabeçalho para a área de dados, descrevendo seu conteúdo (semelhante ao bloco de parâmetros do BIOS usado pelos discos formatados em FAT, HPFS e NTFS).

Um conjunto de descritores de volume é mostrado abaixo.

|Conjunto de descritores de volume|
---|
|Descritor de volume #1|
|...|
|Descritor de volume #N|
|Terminador do conjunto de descritores de volume|

#### Descritor de Volume

Cada descritor de volume tem 2048 bytes de tamanho e tem a seguinte estrutura:

|Peça |Tipo |Identificador |Versão |Dados|
---|---|---|---|---|
|Tamanho |1 byte |5 bytes (sempre 'CD001') |1 byte (sempre 0x01) |2.041 bytes|

## Referências

* [Imagem de disco óptico - Wikipedia](https://en.wikipedia.org/wiki/Optical_disc_image)
* [Assinaturas de arquivo](https://www.garykessler.net/library/file_sigs.html)
* [ISO 9660 - Wikipedia](https://en.wikipedia.org/wiki/ISO_9660)

