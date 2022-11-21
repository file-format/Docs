{
  "date" : "2019-12-09",
  "keywords" :[ "arquivo zip", "formato de arquivo zip", "o que é um arquivo zip", "arquivo", "exemplo zip", "extensão de arquivo zip", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FECHO ECLAIR",
  "description":"O que é um arquivo ZIP e APIs que podem criar e abrir arquivos ZIP.",
  "linktitle" : "ZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## O que é um arquivo ZIP? ##

Um arquivo com extensão .zip é um arquivo que pode conter um ou mais arquivos ou diretórios. O arquivo pode ter compressão aplicada aos arquivos incluídos para reduzir o tamanho do arquivo ZIP. O formato de arquivo ZIP foi tornado público em fevereiro de 1989 por Phil Katz para obter arquivamento de arquivos e pastas. O formato fez parte do utilitário [PKZIP](https://www.pkware.com/pkzip), criado pela PKWARE, Inc. Logo após a disponibilização de [especificações disponíveis](https://pkware.cachefly.net/ webdocs/casestudies/APPNOTE.TXT), muitas empresas tornaram o formato de arquivo ZIP parte de seus utilitários de software, incluindo Microsoft (desde o Windows 7), Apple (Mac OS X) e muitos outros.

## Breve História do Formato de Arquivo ZIP

O histórico do formato de arquivo ZIP remonta ao evento de ação judicial movida pela System Enhancement Associates (SEA) contra o PKWARE por usar seu utilitário ARC sem permissões para sua marca registrada e os direitos autorais da aparência do produto e da interface do usuário. Antes disso, Phil Katz reescreveu o código-fonte da SEA e lançou o PKXARC, um extrator ARC, e o PKARC, um compressor de arquivos, como freeware para sistemas baseados em MS-DOS. Perdendo para o processo, a PKWARE não pôde mais usar nada relacionado ao ARC. Foi aqui que surgiu a criação de uma nova compactação de arquivos, denominada ZIP, que fez parte do utilitário PKZIP na PKWARE, Inc.

Katz lançou as especificações do formato de arquivo ZIP para o domínio público, mantendo os direitos de propriedade sobre seu utilitário de compactação e extração, ou seja, PKZIP. O sistema de compactação ZIP foi (e é) capaz de arquivar arquivos em uma pasta por meio de um algoritmo de verificação de redundância cíclica de 32 bits ([CRC](http://en.wikipedia.org/wiki/Cyclic_redundancy_check)) para compactar arquivos tamanhos. Ao contrário do ARC, as pastas .ZIP incluíam um arquivo de diretório que desempenhava o papel de livro de códigos de um criptógrafo, contendo as informações necessárias para renderizar os arquivos compactados.

## Métodos de compactação compatíveis em ZIP

De acordo com as especificações do formato de arquivo .ZIP, os seguintes métodos de compactação são suportados.

* Armazenar - não implica compressão
* Encolher
* Redução (Isto implica em fatores de compressão que vão do nível 1 ao nível 4)
* Implodir
* Esvaziar
* Esvaziar 64
* BZIP2
* LZMA (EFS)
* WavPack
* PPMd versão I, Rev 1

DEFLATE é o método de compactação comumente usado, que é um algoritmo de compactação de data sem perdas que usa uma combinação da codificação LZ77 e Huffman e é detalhado em [RFC 1951](https://tools.ietf.org/html/rfc1951).

## Especificações de formato de arquivo ZIP

Os arquivos ZIP têm a capacidade de armazenar vários arquivos usando diferentes técnicas de compactação e, ao mesmo tempo, suportam o armazenamento de um arquivo sem nenhuma compactação. Cada arquivo é armazenado/compactado individualmente, o que ajuda a extraí-los ou adicionar novos, sem aplicar compactação ou descompactação em todo o arquivo.

### Formato geral do arquivo ZIP

Cada arquivo Zip é estruturado da seguinte maneira:


|Formato de arquivo ZIP
---|
|Cabeçalho de Arquivo Local 1
|Dados do arquivo 1
|Descritor de dados 1
|Cabeçalho de Arquivo Local 2
|Dados do arquivo 2
|Descritor de dados 2
| ....
| ....
|Cabeçalho do Arquivo Local N
|Arquivo de dados N
|Descritor de dados N
|Cabeçalho de descriptografia do arquivo
|Arquivar registro de dados extras
|Diretório Central

O formato de arquivo ZIP usa o algoritmo CRC de 32 bits para fins de arquivamento. Para renderizar os arquivos compactados, um arquivo ZIP contém um diretório em sua extremidade que guarda a entrada dos arquivos contidos e sua localização no arquivo compactado. Ele, assim, desempenha o papel de codificação para encapsular as informações necessárias para renderizar os arquivos compactados. Os leitores ZIP usam o diretório para carregar a lista de arquivos sem ler todo o arquivo ZIP. O formato mantém cópias duplas da estrutura de diretórios para fornecer maior proteção contra perda de dados.

Cada arquivo em um arquivo ZIP é representado como uma entrada individual onde cada entrada consiste em um cabeçalho de arquivo local seguido pelos dados do arquivo compactado. O diretório no final do arquivo contém as referências a todas essas entradas de arquivo. Os leitores de arquivos ZIP devem evitar a leitura dos cabeçalhos dos arquivos locais e todos os tipos de listagem de arquivos devem ser lidos do Diretório. Este diretório é a única fonte de entradas de arquivo válidas no arquivo, pois os arquivos também podem ser anexados no final do arquivo. É por isso que, se um leitor ler os cabeçalhos locais de um arquivo ZIP desde o início, ele poderá ler entradas inválidas (excluídas), assim como aquelas que não fazem parte do diretório que está sendo excluído do arquivo.

A ordem das entradas de arquivo no diretório central não precisa coincidir com a ordem das entradas de arquivo no arquivo.

### Entradas de arquivo ZIP

As entradas no arquivo ZIP são organizadas uma após a outra, onde cada entrada consiste em:

* Cabeçalho de arquivo local
* Campos de dados extras opcionais
* Dados do usuário (opcionalmente compactados/opcionalmente criptografados)

O cabeçalho do arquivo local de cada entrada representa informações sobre o arquivo, como comentário, tamanho do arquivo e nome do arquivo. Os campos de dados extras (opcionais) podem acomodar informações para opções de extensibilidade do formato ZIP.

#### Cabeçalho do arquivo local

O cabeçalho do arquivo local possui uma estrutura de campo específica que consiste em valores de vários bytes. Todos os valores são armazenados em ordem de bytes little-endian, onde o comprimento do campo conta o comprimento em bytes. Todas as estruturas em um arquivo ZIP usam assinaturas de 4 bytes para cada entrada de arquivo. O fim da assinatura do diretório central é 0x06054b50 e pode ser distinguido usando sua própria assinatura exclusiva. A seguir está a ordem das informações armazenadas no cabeçalho do arquivo local.


|Deslocamento|Bytes|Descrição
---|---|---|
|0|4|Assinatura do cabeçalho do arquivo local # 0x04034b50 (lido como um número little-endian)
|4|2|Versão necessária para extrair (mínimo)
|6|2|Bandeira de bits de uso geral
|8|2|Método de compactação
|10|2|Hora da última modificação do arquivo
|12|2|Data da última modificação do arquivo
|14|4|CRC-32
|18|4|Tamanho compactado
|22|4|Tamanho não comprimido
|26|2|Comprimento do nome do arquivo (n)
|28|2|Comprimento de campo extra (m)
|30|n|Nome do arquivo
|30+n|m|Campo Extra

#### Cabeçalho do arquivo do diretório central


|Deslocamento|Bytes|Descrição
---|---|---|
|0|4|Assinatura do cabeçalho do arquivo do diretório central # 0x02014b50
|4|2|Versão feita por
|6|2|Versão necessária para extrair (mínimo)
|8|2|Bandeira de bits de uso geral
|10|2|Método de compressão
|12|2|Hora da última modificação do arquivo
|14|2|Data da última modificação do arquivo
|16|4|CRC-32
|20|4|Tamanho compactado
|24|4|Tamanho não comprimido
|28|2|Comprimento do nome do arquivo (n)
|30|2|Comprimento de campo extra (m)
|32|2|Comprimento do comentário do arquivo (k)
|34|2|Número do disco onde o arquivo começa
|36|2|Atributos de arquivo interno
|38|4|Atributos de arquivo externo
|42|4|Deslocamento relativo do cabeçalho do arquivo local. Este é o número de bytes entre o início do primeiro disco no qual o arquivo ocorre e o início do cabeçalho do arquivo local. Isso permite que o software leia o diretório central para localizar a posição do arquivo dentro do arquivo ZIP.
|46|n|Nome do arquivo
|46+n|m|Campo extra
|46+n+m|k|Comentário do arquivo

#### Fim do registro do diretório central


|Deslocamento|Bytes|Descrição
---|---|---|
|0|4|Fim da assinatura do diretório central # 0x06054b50
|4|2|Número deste disco
|6|2|Disco onde o diretório central começa
|8|2|Número de registros do diretório central neste disco
|10|2|Número total de registros do diretório central
|12|4|Tamanho do diretório central (bytes)
|16|4|Deslocamento do início do diretório central, relativo ao início do arquivo
|20|2|Comprimento do comentário (n)
|22|n|Comentário

## Referências

* [Especificações de formato de arquivo ZIP PKWARE](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [Estrutura do arquivo PKZip](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)

