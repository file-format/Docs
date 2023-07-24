{
  "date" : "2020-03-16",
  "keywords" :[ "DWF", "Formato de arquivo", "Abrir", "Ler", "Criar", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo DWF e as APIs que podem criar e abrir arquivos DWF.",
  "title" :"Formato de arquivo DWF",
  "linktitle" : "DWF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo DWF?

Design Web Format (DWF) representa desenho 2D/3D em formato compactado para visualização, revisão ou impressão de arquivos de projeto. Ele contém gráficos e texto como parte dos dados do projeto e reduz o tamanho do arquivo devido ao seu formato compactado. O tamanho reduzido do arquivo torna eficiente a distribuição e comunicação de dados de projeto avançados. O DWF não exige que o destinatário saiba sobre o uso do software CAD que criou o desenho original. O conteúdo do formato de arquivo DWF pode ser simples e incluir apenas uma única folha ou complexo o suficiente para ter fontes, cores e imagens.

## Breve história ##

A Autodesk introduziu o formato de arquivo DWF em 1995 como parte do plug-in de navegação do Netscape, WHIP. O formato evoluiu de formato somente 2D para incluir conteúdo 3D com o passar do tempo. Muitos aplicativos de terceiros também usam esse formato.

## Formato de arquivo DWF ##

DWF é um formato aberto e seguro projetado especificamente para compartilhar dados avançados de projetos de engenharia. É independente do software de aplicativo original, hardware e sistema operacional usado para criar esses dados de projeto. Isso permite que os membros da equipe que não usam aplicativos CAD participem dos processos digitais visualizando construções, GIS ou projetos de produtos. Um arquivo DWF consiste em vários arquivos XML e binários que são empacotados juntos em um arquivo compactado criado com compactação [ZIP](/pt/compression/zip/). Você pode renomear uma extensão de arquivo DWF para ZIP e visualizar o conteúdo do arquivo. O pacote DWF pode conter vários tipos de dados de projeto, como gráficos 2D, gráficos 3D, metadados de pacote e seção e outros arquivos de recursos.

**Arquivos de metadados DWF** – arquivos XML que contêm informações relativas a metadados e estrutura (autor, título, tempo de criação, dependências de seção, ordenação de seção, descrições de arquivo de recurso, funções, mimetypes, etc.) e pertencentes à seção (página informações, metadados de projeto, etc.). Os metadados estruturais são usados para criar objetos lógicos (coleções de arquivos para representar uma parte ou página, etc.).

**Arquivos de recursos** – mídia ou outros arquivos de conteúdo que são referenciados nos metadados do pacote/seção e geralmente são apresentações de dados de design em vários formatos (ZGL, W2D, [JPG](/pt/image/jpeg/), [PNG](/pt/image/png/), AVI, XML, [TXT](/pt/word-processing/txt/), [DOC](/pt/word-processing/doc/), etc.)

### Detalhes do formato de arquivo ###

Os arquivos DWF são organizados em três seções principais, conforme mostrado abaixo.

* Cabeçalho de identificação do arquivo
* Bloco de dados de arquivo
* Trailer de encerramento de arquivo

#### Cabeçalho do identificador de arquivo ####

O cabeçalho do identificador de arquivo permite a identificação de arquivos DWF por aplicativos. Ele também identifica qual versão das especificações DWF foi usada para codificar o arquivo. É um cabeçalho de 12 bytes que é organizado da seguinte forma:


|Byte|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Caractere|(|D|W|F|(espaço)|V|0|0|.|3|0|)

Aqui está um resumo desta tabela:

* Os primeiros seis bytes do cabeçalho sempre representam caracteres ASCII "(DWF V"
* Os 5 bytes a seguir contêm informações sobre o número da versão, por exemplo, "00.30" com o valor da versão principal e secundária do formato

Os aplicativos que criam um arquivo DWF devem especificar o número de versão mais baixo possível que um aplicativo de leitura precisa suportar para usar os dados corretamente.

#### Bloco de dados do arquivo ####

O bloco de dados do arquivo começa no 13º byte de um arquivo DWF e é uma série de pares de opcodes e operandos, como na tabela a seguir.

|Campo 1|Campo 2|Campo 3|Campo 4|Campo 5|Campo 5
--- | --- |--- | --- |--- | --- |
|opcode|operando|opcode|operando|opcode|operando

Um arquivo DWF pode conter pares opcode-operando como ASCII legível, bem como código binário ou uma mistura de ambos. Todas as operações DWF têm um formato de operando/código de operação ASCII legível, e a maioria das operações também tem um código de operação/forma de operando binário codificado. Opcodes estão em byte único, permitindo mais de 200 operações. ASCII estendido e binário estendido são casos excepcionais. Os valores dos Opcodes podem variar de 0 a 255 com algumas exceções. Exceto para os dois tipos especiais de opcodes ASCII estendido e binário estendido, um leitor de arquivos deve saber como calcular o comprimento do operando.

##### Opcodes proibidos #####

As representações ASCII para o seguinte não podem ser usadas como opcodes:

As seguintes representações ASCII não podem ser usadas como opcodes:

* Espaço (0x20)
* Aba (0x09)
* Hífen (0x2D)
* Dígitos ASCII 0-9 (0x30 - 0x39)
* Retorno de carro (0x0D)
* Alimentação de linha (0x0A)
* Aspas Simples (0x27)
* Aspas duplas (0x22)
* Período (0x2E)
* Parênteses (0x28 e 0x29)
* Chaves (0x7B e 0x7D)
* Colchetes (0x5B e 0x5D)
* Barra invertida (0x5C)

#### Trailer de encerramento de arquivo ####

O trailer de finalização de arquivo para DWF é simplesmente um opcode especial que indica o final do arquivo. Alguns aplicativos podem armazenar dados não DWF seguindo o opcode de encerramento. O trailer é mostrado abaixo:


|Byte|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Personagem|(|E|n|d|0|f|D|W|F|)

## Referências ##

* [DWF - Por Wikipedia](https://en.wikipedia.org/wiki/Design_Web_Format)
* [Formato de dados WHIP](http://paulbourke.net/dataformats/whip/)
* [https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1](https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1)

