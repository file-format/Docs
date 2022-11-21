{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONETOC2 - Formato de arquivo do Microsoft OneNote",
  "description":"Saiba mais sobre o formato de arquivo ONETOC2 e APIs que podem criar e abrir arquivos ONETOC2.",
  "linktitle" : "ONETOC2",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## O que é ONETOC2? ##

Aqueles que trabalharam com o aplicativo [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) podem ter notado a presença de arquivos .onetoc2 na pasta do notebook. O Microsoft OneNote cria um arquivo binário .onetoc2 como Índice para manter um índice sobre a ordem das diferentes seções de anotações em um bloco de anotações. Um notebook é uma coleção de arquivos de seção armazenados no mesmo diretório. O arquivo .onetoc2 usa uma coleção de propriedades para especificar configurações como a ordem das seções no bloco de anotações e a cor do bloco de anotações.

Quando você cria um bloco de anotações no OneNote 2016, ele é salvo automaticamente no novo formato de arquivo 2010-2016. Você precisará desse formato se quiser que todos os recursos do OneNote 2016, como equações matemáticas e notas vinculadas, funcionem corretamente.

## Formato de arquivo ONETOC2 ##

O formato de arquivo .onetoc2 é representado como Formato de Arquivo de Armazenamento de Revisão do OneNote e é uma coleção de estruturas que especificam um armazenamento de revisão organizado em espaços de objeto com referência cruzada, contendo objetos com conjuntos de propriedades e contendo um log de transações para garantir a integridade do arquivo em escreve. As especificações completas para o formato de arquivo .onetoc2 estão disponíveis [online](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) e podem ser consultadas para desenvolvimento de aplicativos .

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
:


|Formato de arquivo|Valor
--- | --- |
|.um|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bytes):` Um inteiro sem sinal. DEVE ser um dos valores na tabela a seguir, dependendo do formato de arquivo desse arquivo.


|Formato de arquivo|Valor
--- | --- |
|.um|0x0000002A
|.onetoc2|0x0000001B

## Referências ##

* [[MS-ONESTORE] - Formato de arquivo do OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

