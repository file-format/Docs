{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OST - Formato de arquivo de armazenamento do Outlook",
  "description":"Saiba mais sobre o formato de arquivo OST e APIs que podem criar e abrir arquivos OST.",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo OST?

Os arquivos de armazenamento OST ou offline representam os dados da caixa de correio do usuário no modo offline na máquina local após o registro no Exchange Server usando o Microsoft Outlook. Ele é criado automaticamente no primeiro uso do Microsoft Outlook na conectividade com o servidor. Uma vez que o arquivo é criado, os dados são sincronizados com o servidor de e-mail para que estejam disponíveis offline também em caso de desconexão do servidor de e-mail. Os arquivos OST podem usar itens de caixa de correio, como e-mails, contatos, informações de calendário, notas, tarefas e outros dados semelhantes. Os usuários podem criar emails e outros itens de dados no arquivo OST mesmo na ausência de conexão com o servidor, mas estes não serão sincronizados com o servidor. Uma vez que a conexão é estabelecida, o arquivo local é sincronizado novamente com o servidor para que o servidor e a cópia local estejam no mesmo nível de informação.

## Formato de arquivo OST

O formato de arquivo OST (Offline Storage Table) e [PST](/pt/email/pst/) (Personal Storage Table) consiste no formato Personal Folder File (PFF) que corresponde ao armazenamento de e-mails, contatos e compromissos do usuário. Os dados em um arquivo PFF são armazenados em little-endian com todas as datas e horas representadas como FILETIME em UTC. [MS-PST] define dois tipos de PFF:

* Formato ANSI de 32 bits
* Formato Unicode de 64 bits

Formato de arquivo PST [especificações](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546), conforme disponível na Microsoft, também são aplicáveis ao formato de arquivo OST como gratuito e licenciamento de patente irrevogável por meio da Promessa de Especificação Aberta. Consiste nos seguintes elementos distinguíveis:

* Cabeçalho Fle
* Dados do cabeçalho do arquivo
* Nó de ramificação de índice
* Nó folha de índice
* (Arquivo) índice de deslocamento
* (Item) índice do descritor
* Descritores locais
* Tipo de tabela de itens

### Informações do cabeçalho

A estrutura HEADER do arquivo OST está localizada no início do arquivo no deslocamento 0. Ele contém informações de metadados sobre o arquivo OST e as informações ROOT para acessar as estruturas de dados da Camada NDB descritas acima. A estrutura HEADER difere para as versões Unicode e ANSI do formato de arquivo OST.

O cabeçalho começa com uma palavra mágica de 4 bytes **!BDN** representada por bytes (0x21, 0x42, 0x44, 0x4E). Outro número mágico de 2 bytes, **SM** (0x53, 0x4D), está localizado no deslocamento 8 do início do arquivo. As informações de versão (ANSI ou Unicode) estão em um deslocamento de 10 a partir do início do arquivo. O valor hexadecimal (0x17) especifica o arquivo Unicode OST enquanto 0x0E ou 0x0F representa o formato de arquivo ANSI.

|Campo|Descrição
---|---|
|dwMagic (4 bytes)|DEVE ser "{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")"
|dwCRCPartial (4 bytes)|O valor CRC de 32 bits dos 471 bytes de dados a partir de wMagicClient (0ffset 0x0008)
|wMagicClient (2 bytes)|DEVE ser "{ 0x53, 0x4D }".
|wVer (2 bytes)|Versão do formato do arquivo. Esse valor DEVE ser 14 ou 15 se o arquivo for um arquivo PST ANSI e DEVE ser 23 se o arquivo for um arquivo PST Unicode.
|wVerClient (2 bytes)|Versão do formato de arquivo do cliente. A versão que corresponde ao formato descrito neste documento é 19. Os criadores de um novo arquivo PST baseado neste documento DEVEM inicializar este valor para 19.
|bPlatformCreate (1 byte)|Este valor DEVE ser definido como 0x01.
|bPlatformAccess (1 byte)|Este valor DEVE ser definido como 0x01.
|dwReservado (8 bytes)|
|bidUnused (8 bytes Unicode apenas)|Preenchimento não utilizado adicionado quando o formato de arquivo Unicode PST foi criado.
|bidNextP (Unicode: 8 bytes; ANSI: 4 bytes)|Próxima página BID. As páginas têm um contador especial para alocar valores bidIndex. O valor de bidIndex para BIDs para páginas é alocado a partir deste contador.
|bidNextB (4 bytes somente ANSI): |Próximo BID. Este valor é o contador monotônico que indica o BID a ser atribuído para o próximo bloco alocado. Os valores BID avançam em incrementos de 4. Para mais detalhes, consulte a seção 2.2.2.2.
|dwUnique (4 bytes)|Este é um valor monotonicamente crescente que é modificado toda vez que a estrutura HEADER do arquivo PST é modificada. A função desse valor é fornecer um valor exclusivo e garantir que os CRCs de cabeçalho sejam diferentes após cada modificação de cabeçalho.
|rgnid[]   (128 bytes)|Um array fixo de 32 NIDs, cada um correspondendo a um dos 32 NID_TYPEs possíveis (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_TYPE_ASSOC_MESSAGE)
|qwNão utilizado (8 bytes)|Espaço não utilizado; DEVE ser definido como zero. Apenas formato de arquivo PST Unicode.
|root (Unicode: 72 bytes; ANSI: 40 bytes)|Uma estrutura ROOT (seção 2.2.2.5).
|dwAlign (4 bytes)|Bytes de alinhamento não utilizados; DEVE ser definido como zero. Apenas formato de arquivo PST Unicode.
|rgbFM (128 bytes)|FMap obsoleto. Isso não é mais usado e DEVE ser preenchido com 0xFF. Os leitores DEVEM ignorar o valor desses bytes.
|rgbFP (128 bytes)|FPMap obsoleto. Isso não é mais usado e DEVE ser preenchido com 0xFF. Os leitores DEVEM ignorar o valor desses bytes.
|bSentinel (1 byte)|Deve ser definido como 0x80.
|bCryptMethod (1 byte)|Indica como os dados no arquivo PST são codificados. DEVE ser definido para um dos valores predefinidos (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbReservado (2 bytes)| Reservado; DEVE ser definido como zero.
|bidNextB (8 bytes)|Indica o próximo valor de BID disponível. Apenas formato de arquivo PST Unicode.
|bidNextB (APENAS Unicode: 8 bytes)|Próximo BID. Este valor é o contador monotônico que indica o BID a ser atribuído para o próximo bloco alocado. Os valores BID avançam em incrementos de 4. Para mais detalhes, consulte a seção 2.2.2.2.
|dwCRCFull (4 bytes)|O valor CRC de 32 bits dos 516 bytes de dados a partir de wMagicClient até bidNextB, inclusive. Apenas formato de arquivo PST Unicode.
|ullReserved (8 bytes)|Reservado; DEVE ser definido como zero. Somente formato de arquivo ANSI PST.
|dwReservado (4 bytes)|Reservado; DEVE ser definido como zero. Somente formato de arquivo ANSI PST.
|rgbReserved2 (3 bytes)|
|bReservado (1 byte) |
|rgbReserved3 (32 bytes) |

## Referências

* [Formato de arquivo de pastas particulares do Outlook (.ost)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [Especificações de formato de arquivo de pasta pessoal](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

