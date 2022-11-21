{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo gz", "formato de arquivo gz", "o que é um arquivo gz", "arquivo", "exemplo gz", "extensão de arquivo gz", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo GZ - Arquivo compactado GNU",
  "description":"Saiba mais sobre o que é um arquivo GZ e APIs que podem criar e abrir arquivos GZ.",
  "linktitle" : "GZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo GZ?

Um arquivo GZ é um arquivo compactado que é criado usando o algoritmo de compactação padrão [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip). Ele pode conter vários arquivos compactados, diretórios e stubs de arquivos. Esse formato foi desenvolvido inicialmente para substituir os formatos de compactação em sistemas UNIX. e ainda é um dos tipos de arquivo mais comuns em sistemas Linux. Aplicativos como [WinZip](https://www.winzip.com/en/) podem abrir arquivos GZ para visualizar seu conteúdo no Windows e no MacOS.

## Formato de arquivo GZ - Mais informações

O Gzip usa o algoritmo [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) para compactação do arquivo e difere do formato de arquivo [ZIP](/pt/compression/zip/) ao aplicar o algoritmo de compactação no arquivo completo em vez de arquivos individuais. As especificações de formato de arquivo GZIP versão 4.3 publicadas pela Internet Engineering Task Force (IETF) contêm informações detalhadas sobre o formato de arquivo. O formato do arquivo consiste em:

* Cabeçalho do arquivo
* Cabeçalhos opcionais
* Dados compactados
* Rodapé de arquivo

## Cabeçalho do arquivo GZ ##

O cabeçalho do arquivo GZ consiste em 10 bytes como segue:

|Deslocamento|Tamanho|Valor|Descrição
---|---|---|---|
|0|2|0x1f 0x8b|Número mágico que identifica o tipo de arquivo
|2|1| |Método de Compressão * 0-7 (Reservado) * 8 (Esvaziar)
|3|1| |Sinalizadores de arquivo
|4|4| | carimbo de data/hora de 32 bits
|8|1| |Sinalizadores de compressão
|9|1| |ID do sistema operacional

### Sinalizadores de arquivo ###

|Valor|Identificador|Descrição
---|---|---|
|0x01|FTEXT|Se definido, os dados descompactados precisam ser tratados como texto em vez de dados binários. Esse sinalizador sugere a conversão de fim de linha para arquivos de texto de plataforma cruzada, mas não a impõe.
|0x02|FHCRC|O arquivo contém uma soma de verificação de cabeçalho (CRC-16)
|0x04|FEXTRA|O arquivo contém campos extras
|0x08|FNAME|O arquivo contém uma string de nome de arquivo original
|0x10|FCOMMENT|O arquivo contém comentários
|0x20| |Reservado
|0x40| |Reservado
|0x80| |Reservado

### Sistema operacional ###

|Valor|Descrição
---|---|
|0|Sistema de arquivos FAT (MS-DOS, OS/2, NT/Win32)
|1|Amigos
|2|VMS (ou OpenVMS)
|3|Unix
|4|VM/CMS
|5|Atari TOS
|6|Sistema de arquivos HPFS (OS/2, NT)
|7|Macintosh
|8|Sistema Z
|9|CP/M
|10|TOP-20
|11|Sistema de arquivos NTFS (NT)
|12|QDOS
|13|Acorn RISCOS
|255|desconhecido

## Cabeçalhos opcionais GZ ##

Os cabeçalhos extras opcionais são aqueles indicados pelos sinalizadores de arquivo e incluem informações como o nome do arquivo original, campos extras, comentários e soma de verificação do cabeçalho.

## Dados compactados ##

Esta seção contém os dados compactados usando o algoritmo de compactação DEFLATE.

## Rodapé do arquivo GZ ##

O rodapé do arquivo tem 8 bytes de tamanho e contém as seguintes informações.

|Deslocamento|Tamanho|Descrição
---|---|---|
|0|4|Soma de verificação (CRC-32)
|4|4|Valor do tamanho dos dados não compactados em bytes

## Referências ##

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: especificação de formato de arquivo GZIP](http://tools.ietf.org/html/rfc1952), por IETF.

