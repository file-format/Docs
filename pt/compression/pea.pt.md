{
  "date" : "2021-04-21",
  "keywords" :[ "arquivo de ervilha", "formato de arquivo de ervilha", "o que é um arquivo de ervilha", "arquivo", "exemplo de ervilha", "extensão de arquivo de ervilha","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEA - Formato de arquivo de arquivo PeaZip",
  "description":"Saiba mais sobre o formato de arquivo PEA e APIs que podem criar e abrir arquivos PEA.",
  "linktitle" : "PEA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-21"
}

## O que é um arquivo PEA?

Um arquivo com extensão .pea, acrônimo para Pack, Encrypt, and Authenticate, é um arquivo [zip](/pt/compression/zip/) criado com o aplicativo de software de arquivamento [PeaZip](https://peazip.github.io/). Ele apresenta compactação e saída de vários volumes e oferece um modelo de segurança flexível por meio de criptografia e criptografia autenticadas. Isso fornece privacidade e autenticação dos dados. O utilitário PeaZip está disponível como mecanismo de código aberto que pode ser compilado para diferentes sistemas operacionais conforme os requisitos.

## Formato de arquivo PEA

As [especificações de formato de arquivo do PEA](https://peazip.github.io/pea_help.pdf) estão disponíveis publicamente para referência do desenvolvedor. Os arquivos PEA são arquivos binários com modelo de segurança flexível e verificações de integridade redundantes que variam de somas de verificação a hashes criptograficamente fortes. Isso define três níveis diferentes de comunicação para controlar:

* Streams - o fluxo de dados de saída real que é formado por vários arquivos de entrada e pode ser gravado em vários volumes de saída
* Objetos - arquivos de entrada e pastas enviados para o arquivo .pea
* Volumes - arquivo de saída que pode ser estendido para o tamanho definido pelo usuário

Cada um deles é opcional e pode ser incorporado conforme os requisitos do usuário. O formato de arquivo PEA pode armazenar um único fluxo contendo objetos ilimitados. Cada fluxo tem até 2^64 bytes de tamanho.

Os arquivos PEA oferecem verificação de integridade opcional e criptografia autenticada usando AES no modo EAX ou HMAC, alternativamente Twofish e Serpent no modo EAX.

### Cabeçalho do arquivo PEA

O cabeçalho do arquivo tem 10 bytes e está estruturado da seguinte forma.

|Bytes|Descrição|
---|---|
|1 | Campo de byte mágico para desambiguação de formato de arquivo: $EA|
|1 | Número da Versão|
|1 | Número da Revisão|
|1 | Esquema de controle de volume|
|1 | Declarando o SO onde o stream foi construído|
|1 | Declarando a codificação de data e hora do SO|
|1 | Declarando a codificação de caracteres do nome dos objetos|
|1 | Declarando tipo de CPU (codificado em 7 bits) e endianness (em msb)|
|1 | Reservado para uso futuro|

## Referências

* [Especificações de formato de arquivo PEA](https://peazp.github.io/pea_help.pdf)
* [Formato de arquivo PEA](https://peazip.github.io/pea-file-format.html#.pea_specifications)

