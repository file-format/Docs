{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST - Formato de arquivo de armazenamento de informações pessoais do Outlook",
  "description":"Saiba mais sobre o formato de arquivo PST e APIs que podem criar e abrir arquivos PST.",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo PST?

Arquivos com extensão .pst representam arquivos de armazenamento pessoal do Outlook (também chamados de tabela de armazenamento pessoal) que armazenam várias informações do usuário. As informações do usuário são armazenadas em pastas de diferentes tipos que incluem e-mails, itens de calendário, notas, contatos e vários outros formatos de arquivo. Os arquivos PST são usados para arquivar dados de e-mail offline que podem ser carregados e visualizados posteriormente em vários aplicativos.

## Especificações de formato de arquivo PST

Formato de arquivo PST [especificações](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546) estão disponíveis na Microsoft como licença de patente gratuita e irrevogável por meio da Open Specification Promise .

### Tipo de formatos PST

Os formatos de arquivo PST são categorizados em dois tipos com base na codificação do tipo de arquivo. Os arquivos PST codificados em ANSI são formatos de arquivo mais antigos e são suportados apenas pelo Outlook 2002 e versões anteriores. Esses arquivos têm um limite de tamanho máximo de 2 GB (2^^31^^ Bytes) e não suportam Unicode. Um tipo de formato de arquivo mais moderno, baseado na codificação Unicode, remove a limitação de tamanho de arquivo e pode atingir o tamanho máximo de dados de 50 GB.

### Organização lógica do formato de arquivo PST

Na base do formato de arquivo PST está o B-Tree que mantém os dados ordenados e permite buscas, acessos seqüenciais, inserções, exclusões etc. em tempo logarítmico. A estrutura geral de um arquivo PST é organizada em três camadas.

![Logical layers of a PST file](/pt/email/PST-1.png "Logical layers of a PST file")

`Camada de banco de dados de nós (NDB)` - A camada de banco de dados de nós está no nível inferior de um arquivo PST e inclui banco de dados de nós. Esses nós representam, na verdade, instalações de armazenamento de nível inferior do formato de arquivo PST. A camada NDB é composta por cabeçalho, informações de alocação de arquivos, blocos e BTrees (Node BTree e Block BTree) do ponto de vista de armazenamento. Nós e Blocos da Camada NDB são vinculados via Data BID, que é uma das quatro propriedades de referência do Node, ou seja, NID (Node ID), Pai NID, Data BID (Block BID) e SubNode BID.

`Listas, Tabelas e Camadas de Propriedades -` A camada LTP fornece a compreensão lógica de conceitos de nível superior sobre o NDB. Além de outros elementos, a camada LTP compreende principalmente o Contexto de Propriedade (PC) e o Contexto de Tabela (TC). PC é uma coleção de propriedades, enquanto TC representa uma matriz bidimensional de coleção de propriedades versus a presença destas. Implementação eficiente de PCs e TCs, a camada LTP usa os seguintes dois tipos de estruturas de dados sobre o NDB Node:

* Heap On Node (HN) - permite sub-alocar o fluxo de dados de um nó em pequenos fragmentos de tamanho variável.
* BTree on Heap (BTH) - BTH fornece uma maneira conveniente e prática de pesquisar através de dados PCs, descritos acima, são implementados como BTHs e por isso é implementado construindo dentro de uma estrutura HN.

`Messaging Layer -` Regras de nível superior e lógica de negócios para trabalhar com arquivos PST são implementadas nesta camada. A saída lógica desta camada resulta em objetos Pasta, Objetos Mensagem, Objetos Anexos e Propriedades que é possível através da combinação de camadas LTP e NDB. Regras e requisitos, que precisam ser seguidos ao modificar o conteúdo do PST, também são definidos nesta camada.

### Organização física do formato de arquivo PST

O alto nível de organização de arquivos do arquivo PST é mostrado na figura abaixo. Esta é apenas uma visão geral de diferentes conceitos de elementos lógicos do arquivo PST.

![Physical organization of the PST file format](/pt/email/PST-2.png "Physical organization of the PST file format")


#### Informações do cabeçalho PST

A estrutura HEADER do arquivo PST está localizada no início do arquivo no deslocamento 0. Ele contém informações de metadados sobre o arquivo PST e as informações de ROOT para acessar as estruturas de dados da Camada NDB descritas acima. A estrutura HEADER difere para as versões Unicode e ANSI do formato de arquivo PST.

O cabeçalho começa com uma palavra mágica de 4 bytes **!BDN** representada por bytes (0x21, 0x42, 0x44, 0x4E). Outro número mágico de 2 bytes, **SM** (0x53, 0x4D), está localizado no deslocamento 8 do início do arquivo. As informações de versão (ANSI ou Unicode) estão em um deslocamento de 10 a partir do início do arquivo. O valor hexadecimal (0x17) especifica o arquivo PST Unicode enquanto 0x0E ou 0x0F representa o formato de arquivo ANSI.

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

### Proteção de dados ###

Por segurança, os arquivos PST também podem ser protegidos por senha, o que exige que o aplicativo de carregamento aplique a senha antes de poder ser visualizado. A senha aplicada ao arquivo PST é armazenada no armazenamento de mensagens. No entanto, isso não fornece proteção de dados forte, pois a senha pode ser removida pelas ferramentas disponíveis. Além disso, a senha especificada pelo usuário não é usada como parte da chave para codificação e decodificação de algoritmos de cifra. Assim, não há benefício em proteger os dados para serem acessados por partes não autorizadas. O armazenamento de senha como hash CRC-32 da string original também o torna um método fraco para segurança de dados contra abordagem de força bruta.

## Referências ##

* [Formato de arquivo de pastas particulares (.pst) do Outlook](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [Especificações de formato de arquivo de pasta pessoal](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

