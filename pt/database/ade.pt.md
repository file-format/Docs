{
  "date" : "2021-08-29",
  "keywords" :[ "ade", "extensão", "arquivo", "formato de arquivo", "Tipo de arquivo de banco de dados", "Formato de arquivo de banco de dados", "Microsoft Access" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo ADE e APIs que podem criar e abrir arquivos ADE.",
  "title" :"ADE - Acessar Arquivo de Extensão do Projeto",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## O que é um arquivo ADE?

Um arquivo com extensão .ade é um arquivo de projeto do Microsoft Access que contém a saída compilada das informações contidas no arquivo de projeto ADP do Microsoft Access. As informações no arquivo de projeto do Access, além do Visual Basic for Applications (VBA), estão disponíveis em formato compilado em arquivos ADE. Os dados são armazenados em formato compactado nesses arquivos para reduzir o tamanho do arquivo e melhorar o desempenho no Access. Como o ADE é a saída compilada do arquivo de projeto do Access, qualquer código-fonte VBA que faça parte do projeto permanece protegido por não permitir que faça parte da saída. Os arquivos ADE podem ser abertos no Microsoft Access 365.

## Formato de arquivo ADE - Mais informações

ADE são arquivos de banco de dados de acesso compilados que são armazenados em disco como arquivos binários. A estrutura interna de arquivos desses arquivos não é conhecida.

Os arquivos ADE podem criar problemas na abertura com base na versão do Microsoft Access que foi usada para criar esses arquivos. Os bancos de dados do Access que estão usando a versão de 64 bits do Microsoft Access 2010 e que são compilados como arquivos MDE, [ACCDE](/pt/database/accde/) ou ADE precisam ser recompilados no Microsoft Access 2021 Service Pack 1 (SP1) para funcionam corretamente com o Access 2010 SP1. Esse problema ocorre porque o Access 2010 SP1 usa uma versão mais recente do arquivo VBE7.dll (versão 7.00.1619).

## Referências

* [Problema com arquivos do Access ADE](https://docs.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [Quais formatos de arquivo de acesso usar](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

