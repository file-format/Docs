{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDB", "extensão", "arquivo", "formato de arquivo", "Tipo de arquivo de banco de dados", "Formato de arquivo de banco de dados", "Arquivos de banco de dados" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo ACCDB e APIs que podem criar e abrir arquivos ACCDB.",
  "title" :"Formato de arquivo ACCDB - Arquivo de banco de dados do Microsoft Access 2007",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## O que é um arquivo ACCDB?

Um arquivo com extensão .accdb é um arquivo de banco de dados do Microsoft Access 2007 que armazena dados de usuários em tabelas. Ele suporta o armazenamento formulários personalizados, consultas SQL e outros dados. Os arquivos ACCDB substituíram os arquivos [MDB](/pt/database/mdb/) depois que a Microsoft mudou para a estrutura de arquivos baseada em XML. Os arquivos ACCDB ainda podem ser convertidos em MDB com compatibilidade antiga. No entanto, o ACCDB é o formato de arquivo de banco de dados do Access amplamente usado agora. A Microsoft também deu suporte a recursos adicionais no formato ACCDB, como a possibilidade de armazenar anexos de arquivos, dados binários e suporte a campos multivalorados.

## Formato de arquivo ACCDB

Assim como o MDB, não há especificações públicas disponíveis para o formato de arquivo ACCDB. A Microsoft oferece suporte para acessar esses arquivos programaticamente por meio do padrão ODBC (Open Database Connectivity) e do Visual Basic for Applications (VBA).

### Introspecção

Um dump hexadecimal de um arquivo ACCDB simples sugere que há semelhanças gerais na estrutura com as versões mais recentes da família de formatos MDB predecessor. Ambos os formatos de arquivo usam tamanhos de página fixos de 4096 bytes. Outra semelhança entre ACCDB e MDB é a forma do número mágico, que inclui a string "Standard ACE DB" para ACCDB. Uma versão ou código de compatibilidade está no mesmo local em ambos os formatos. O mdbtools | O arquivo HACKING afirma "O deslocamento 0x14 contém a versão Jet deste banco de dados" e o Guia MDB não oficial concorda. As informações nessas fontes, combinadas com a entrada da Wikipedia para [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), sugerem que um valor de 0x02 indica ACE 12 (Access 2007) e 0x03 indica ACE 14 (Acesso 2010). No entanto, um banco de dados mínimo criado no Access 2010 e um semelhante criado no Access 2016 têm 0x02 neste local. Um banco de dados mínimo criado no Access 2016, mas definindo uma coluna com o tipo de dados "grande inteiro" recém-introduzido, tinha um valor de 0x05. Em arquivos ACCDB, esse indicador parece refletir a compatibilidade do arquivo em vez da versão do mecanismo ACE usado para criá-lo.

## Referências

* [Access File Format](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)
* [Access 2016 Specifications](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [Qual formato de arquivo do Access devo usar?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?ui=en-us&rs=en-us&ad=us)
