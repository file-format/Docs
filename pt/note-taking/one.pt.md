{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONE - Formato de arquivo do Microsoft OneNote",
  "description":"Saiba mais sobre um formato de arquivo e APIs que podem criar e abrir UM arquivo.",
  "linktitle" : "ONE",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo .ONE? ##

O arquivo representado pela extensão .ONE é criado pelo aplicativo Microsoft OneNote. O OneNote permite que você colete informações usando o aplicativo como se estivesse usando o bloco de rascunho para fazer anotações. Os arquivos do OneNote podem conter elementos diferentes que podem ser colocados em locais não fixos nas páginas do documento. Esses elementos podem conter texto, manuscrito digitalizado e objetos copiados de outros aplicativos, incluindo imagens, desenhos e clipes multimídia (áudio/vídeo). A Microsoft agora oferece a versão online do OneNote como parte do Office365, onde as notas podem ser compartilhadas com outros usuários do OneNote pela Internet.

## Especificações do formato de arquivo .ONE ##

O formato de arquivo do OneNote fornece uma maneira eficaz de representar notas digitais como conjuntos hierárquicos de seções e páginas. Cada página contém conteúdo definido pelo usuário em uma estrutura específica para representação pelo formato de arquivo Document Object Model (DOM). O modelo de dados para este formato é ilustrado abaixo.

### Visão geral da estrutura ###

Conforme ilustrado no modelo de dados para o formato de arquivo do OneNote, um documento do OneNote consiste em diferentes elementos.

#### Seção ####

Uma seção é o contêiner mais alto em um arquivo do OneNote que contém ainda diferentes elementos, como:

* Páginas
* Metadados
* Propriedades

Metadados e propriedades incluem o nome da seção, a identificação das páginas contidas na seção e a ordem em que essas páginas aparecem. O termo "seção" refere-se a todas as páginas que estão em uma seção e à representação desses dados em um arquivo de armazenamento de revisão do OneNote®, que tem uma extensão de nome de arquivo .one.

#### Página ####

O conteúdo definido pelo usuário em um documento do OneNote está contido em uma página. As informações da página incluem texto, listas, tabelas, títulos de página, imagens e etiquetas de notas. Uma página consiste em objetos de contorno aos quais a maioria dos objetos contidos é adicionada. Cada página pode receber um nome para uma representação significativa e os objetos também podem ser adicionados diretamente às páginas. Uma página pode conter ainda subpáginas em um sistema hierárquico.

#### Propriedades e conjuntos de propriedades ####

O conteúdo do OneNote consiste em propriedades, conjuntos de propriedades e objetos de dados de arquivo. Um conjunto de propriedades é uma coleção de propriedades que representa algum tipo de conteúdo. Um objeto de dados de arquivo é um bloco de dados binários que contém imagens, arquivos incorporados ou conteúdo de áudio/vídeo.

#### Bloco de notas do OneNote ####

Um notebook é uma coleção de arquivos de seção armazenados no mesmo diretório. Uma coleção de propriedades é usada para especificar configurações como ordem das seções dentro do bloco de anotações e a cor do bloco de anotações.

### Estrutura do arquivo ###

Um arquivo de armazenamento de revisão DEVE começar com uma estrutura **Header**. O restante do arquivo é particionado em blocos de bytes, onde o tamanho e a estrutura de cada bloco são especificados pelo campo que o referencia. Um bloco é alcançável se for referenciado pela estrutura **Header** ou se for referenciado por um campo em outro bloco alcançável. Dados fora da estrutura **Header** e quaisquer blocos alcançáveis DEVEM ser ignorados.

Todas as estruturas são alinhadas em limites de 1 byte. Todos os números inteiros são assinados, a menos que especificado de outra forma. Todos os campos são [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7), a menos que especificado de outra forma.

#### Cabeçalho ####

O cabeçalho do arquivo .ONE é composto por blocos que contêm diferentes ids e campos exclusivos para representação das informações do arquivo, como segue:

`guidFileType (16 bytes):` Um GUID que especifica o tipo do arquivo de armazenamento de revisão. DEVE ser um dos valores da tabela a seguir.


|Formato de arquivo|Valor
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 bytes):` Um GUID que especifica a identidade deste arquivo de armazenamento de revisão. DEVE ser globalmente único.

`guidLegacyFileVersion (16 bytes):` DEVE ser "{00000000-0000-0000-0000-000000000000}" e DEVE ser ignorado.

`guidFileFormat (16 bytes):` Um GUID que especifica que o arquivo é um arquivo de armazenamento de revisão. DEVE ser "{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}".

`ffvLastCodeThatWroteToThisFile (4 bytes):` Um inteiro sem sinal. DEVE ser um dos valores na tabela a seguir, dependendo do tipo de arquivo.

|Formato de arquivo|Valor
--- | --- |
|.um|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 bytes):` Um inteiro sem sinal. DEVE ser um dos valores na tabela a seguir, dependendo do formato de arquivo desse arquivo.


|Formato de arquivo|Valor
--- | --- |
|.um|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 bytes):` Um inteiro sem sinal. DEVE ser um dos valores na tabela a seguir, dependendo do formato de arquivo desse arquivo.

|Formato de arquivo|Valor
--- | --- |
|.um|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bytes):` Um inteiro sem sinal. DEVE ser um dos valores na tabela a seguir, dependendo do formato de arquivo desse arquivo.

|Formato de arquivo|Valor
--- | --- |
|.um|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 bytes):` Uma estrutura **FileChunkReference32** que DEVE ter um valor de "fcrZero".

`fcrLegacyTransactionLog (8 bytes):` Uma estrutura **FileChunkReference32** que DEVE ser "fcrNil".

`cTransactionsInLog (4 bytes):` Um inteiro sem sinal que especifica o número de transações no log de transações. NÃO DEVE ser zero.

`cbLegacyExpectedFileLength (4 bytes):` Um inteiro sem sinal que DEVE ser zero e DEVE ser ignorado.

`rgbPlaceholder (8 bytes):` Um inteiro sem sinal que DEVE ser zero e DEVE ser ignorado.

`fcrLegacyFileNodeListRoot (8 bytes):` Uma estrutura **FileChunkReference32** que DEVE ser "fcrNil".

`cbLegacyFreeSpaceInFreeChunkList (4 bytes):` Um inteiro sem sinal que DEVE ser zero e DEVE ser ignorado.

`fNeedsDefrag (1 byte):` DEVE ser ignorado.

`fRepairedFile (1 byte):` DEVE ser ignorado.

`fNeedsGarbageCollect (1 byte):` DEVE ser ignorado.

`fHasNoEmbeddedFileObjects (1 byte):` Um inteiro sem sinal que DEVE ser zero e DEVE ser ignorado.

`guidAncestor (16 bytes):` Um GUID que especifica o campo **Header.guidFile** do arquivo de índice, fornecido pela tabela a seguir:


|Formato do arquivo de índice|Localização do arquivo de índice
--- | --- |
|Arquivo de Seção - .One|O arquivo de índice está localizado no mesmo diretório que este arquivo.
|Arquivo de índice - .onetoc2|O arquivo de índice está localizado no diretório pai deste arquivo.

Se o GUID for {00000000-0000-0000-0000-000000000000}, esse campo não fará referência a um arquivo de índice.

`crcName (4 bytes):` Um inteiro sem sinal que especifica o valor CRC do nome deste arquivo de armazenamento de revisão. O nome é a representação Unicode do nome do arquivo com sua extensão e um caractere nulo adicional no final. Esse CRC é sempre calculado usando o algoritmo CRC para o arquivo .one, independentemente desse formato de arquivo de armazenamento de revisão.

`fcrHashedChunkList (12 bytes):` Uma estrutura **FileChunkReference64x32** que especifica uma referência ao primeiro **FileNodeListFragment** em uma lista de partes com hash. Se o valor da estrutura **FileChunkReference64x32** for "fcrZero" ou "fcrNil", a lista de partes com hash não existe.

`fcrTransactionLog (12 bytes):` Uma estrutura **FileChunkReference64x32** que especifica uma referência à primeira estrutura **TransactionLogFragment** em um log de transações. O valor do campo **fcrTransactionLog** NÃO DEVE ser "fcrZero" e NÃO DEVE ser "fcrNil".

`fcrFileNodeListRoot (12 bytes):` Uma estrutura **FileChunkReference64x32** que especifica uma referência a uma lista de nós de arquivo raiz. O valor do campo **fcrFileNodeListRoot** NÃO DEVE ser "fcrZero" e NÃO DEVE ser "fcrNil".

`fcrFreeChunkList (12 bytes):` Uma estrutura **FileChunkReference64x32** que especifica uma referência à primeira estrutura **FreeChunkListFragment**. Se o valor da estrutura **FileChunkReference64x32** for "fcrZero" ou "fcrNil", a lista de partes livres não existirá.

`cbExpectedFileLength (8 bytes):` Um inteiro sem sinal que especifica o tamanho, em bytes, deste arquivo de armazenamento de revisão.

`cbFreeSpaceInFreeChunkList (8 bytes):` Um inteiro sem sinal que DEVE especificar o tamanho, em bytes, do espaço livre especificado pela lista de blocos livres.

`guidFileVersion (16 bytes):` Um GUID. Quando o valor do campo **cTransactionsInLog** ou o campo **guidDenyReadFileVersion** estiver sendo alterado, **guidFileVersion** DEVE ser alterado para um novo GUID.

`nFileVersionGeneration (8 bytes):` Um inteiro sem sinal que especifica o número de vezes que o arquivo foi alterado. DEVE ser incrementado quando o campo **guidFileVersion** for alterado.

`guidDenyReadFileVersion (16 bytes):` Um GUID. Quando o conteúdo existente do arquivo estiver sendo alterado, excluindo a estrutura **Header** do arquivo e os blocos de armazenamento não utilizados, **guidDenyReadFileVersion** DEVE ser alterado para um novo GUID.

`grfDebugLogFlags (4 bytes):` DEVE ser zero. DEVE ser ignorado.

`fcrDebugLog (12 bytes):` Uma estrutura **FileChunkReference64x32** que DEVE ter um valor "fcrZero". DEVE ser ignorado.

`fcrAllocVerificationFreeChunkList (12 bytes):` Uma estrutura **FileChunkReference64x32** que DEVE ser "fcrZero". DEVE ser ignorado.

`bnCreated (4 bytes):` Um inteiro sem sinal que especifica o número de compilação do aplicativo que criou este arquivo de armazenamento de revisão. DEVE ser ignorado.

`bnLastWroteToThisFile (4 bytes):` Um inteiro sem sinal que especifica o número de compilação do aplicativo que gravou pela última vez neste arquivo de armazenamento de revisão. DEVE ser ignorado.

`bnOldestWritten (4 bytes):` Um inteiro sem sinal que especifica o número de compilação do aplicativo mais antigo que gravou neste arquivo de armazenamento de revisão. DEVE ser ignorado.

`bnNewestWritten (4 bytes):` Um inteiro sem sinal que especifica o número de compilação do aplicativo mais recente que gravou neste arquivo de armazenamento de revisão. DEVE ser ignorado.

`rgbReserved (728 bytes):` DEVE ser zero. DEVE ser ignorado.

## Referências ##

* [[MS-ONESTORE] - Formato de arquivo do OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

