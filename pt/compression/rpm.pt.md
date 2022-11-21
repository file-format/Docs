{
  "date" : "2021-04-08",
  "keywords" :[ "rpm file", "rpm file format", "o que é um rpm file", "file", "rpm example", "rpm file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPM - Arquivo do Gerenciador de Pacotes Red Hat",
  "description":"Saiba mais sobre o formato de arquivo RPM e APIs que podem criar e abrir arquivos RPM.",
  "linktitle" : "RPM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## O que é um arquivo RPM?

Um arquivo com extensão .rpm é um pacote do sistema operacional Red Hat Linux para instalações de programas em sistemas Linux. O Red Hat Package Manager usa o formato de arquivo RPM e é um sistema de gerenciamento de pacotes gratuito e de código aberto. Embora os arquivos RPM possam ser usados como estão para a instalação de programas, eles podem ser convertidos para outros formatos de pacote como [DEB](/pt/compression/deb/) usando o programa Debian chamado Alien.

## Formato de arquivo RPM

Um arquivo RPM é um binário que pode conter um conjunto de arquivos. Na maioria das vezes, os arquivos RPM são "RPMs binários", que são os executáveis compilados do software. O arquivo RPM pode conter RPMs de origem (SRPMs) que podem ser usados para compilar o pacote a partir do código-fonte. O formato de arquivo RPM consiste em quatro seções.

* Lead - Identifica o arquivo como um arquivo RPM
* Assinatura - Pode ser usada para garantir integridade e/ou autenticidade
* Cabeçalho - Contém metadados, incluindo nome do pacote, versão, arquitetura, lista de arquivos, etc.
* Arquivo Arquivo - Também conhecido como carga útil, que geralmente está no formato cpio, compactado com [GZIP](/pt/compression/gz/)

## Referências

* [RPM - Wikipedia](https://rpm.org)
* [Documentação do RPM](https://rpm.org/documentation.html)

