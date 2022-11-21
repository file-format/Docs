{
  "date" : "2019-12-13",
  "keywords" :[ "arquivo ppt", "formato de arquivo ppt", "o que é um arquivo ppt", "arquivo", "exemplo de ppt", "extensão de arquivo ppt", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo PPT e APIs que podem criar e abrir arquivos PPT.",
  "title" :"PPT - Formato de arquivo PowerPoint",
  "linktitle" : "PPT",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo PPT?

Um arquivo com extensão PPT representa um arquivo PowerPoint que consiste em uma coleção de slides para exibição como SlideShow. Ele especifica o formato de arquivo binário usado pelo Microsoft PowerPoint 97-2003. Um arquivo PPT pode conter vários tipos diferentes de informações, como texto, marcadores, imagens, multimídia e outros objetos OLE incorporados. A Microsoft criou um formato de arquivo mais recente para o PowerPoint, conhecido como [PPTX](/pt/presentation/pptx/), a partir de 2007, baseado no Office OpenXML e diferente desse formato de arquivo binário. Vários outros programas de aplicativos, como OpenOffice Impress e Apple Keynote, também podem criar arquivos PPT.

## Breve história ##

A Microsoft introduziu o formato de arquivo PPT com o lançamento do PowerPoint em 1987. O formato binário estável foi compartilhado como padrão no PowerPoint 97-2003 para Windows. O formato de arquivo binário é suportado para leitura e gravação pelas versões mais recentes do PowerPoint, incluindo o PowerPoint 2016.

## Especificações de formato de arquivo ##

Desde a sua introdução, o formato de arquivo PPT passou por várias revisões para adições de novos recursos e aprimoramentos. As especificações de versão mais recentes disponíveis são as da revisão 6.0, publicadas em agosto de 2018, que não devem ser misturadas com o número real do produto do formato de arquivo PPT, pois a Microsoft não fornece mais modificações para esse formato.

### Visão geral do formato de arquivo ###

Alguns dos principais componentes de um formato de arquivo PPT são os seguintes:

#### Apresentações ####

Dados do usuário, como formas, texto, animações e mídia, são adicionados a uma apresentação dentro de um Slide. Uma apresentação pode conter um ou mais slides que são exibidos como apresentação de slides quando uma apresentação é executada. Uma apresentação contém slides mestre e slides mestre de título que atuam como modelo para as propriedades visuais comuns dos slides da apresentação. Há também um slide mestre de notas e um slide mestre de folheto que serve a um propósito semelhante e fornece propriedades visuais comuns para todos os slides de anotações e todos os folhetos impressos.

#### Formas ####

Formas são objetos que permitem aos usuários adicionar uma variedade de conteúdo a um slide na forma de formas de espaço reservado, imagens e gráficos. As formas em um slide mestre definem dados comuns para grupos de formas.

#### Formas de espaços reservados ####

Estes são espaços reservados especiais que servem como recipientes para uma variedade de objetos. Diferentes formas de espaço reservado podem ser usadas para fornecer dicas para inserir tipos específicos de formas, como tabelas ou gráficos. Dentro de um slide, uma forma de espaço reservado adota as propriedades visuais de um slide mestre principal, slide mestre de título ou slide mestre de notas.

#### Objetos Externos ####

Objetos externos como áudio incorporado e vinculado, vídeo vinculado, objetos OLE incorporados e vinculados e hiperlinks podem ser incorporados em um slide. Esses objetos podem ser usados para ativar objetos vinculados para acessar recursos externos durante uma apresentação de slides.

### Estruturas de formato de arquivo ###

Os formatos de arquivo binário do PowerPoint consistem nos seguintes fluxos para representar a estrutura e os dados gerais do documento.

* Fluxo do usuário atual
* Fluxo de documentos do PowerPoint
* Fluxo de fotos
* Informações resumidas e informações resumidas do documento (opcional)

As especificações completas para o formato de arquivo DOC podem ser encontradas conforme fornecidas pela [Microsoft](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx) e devem ser consultadas em referência às seções mencionadas nos detalhes a seguir.

#### Fluxo do usuário atual ####

Ele mantém registro do último usuário que abriu o documento e seu nome deve ser "Usuário Atual".

#### Fluxo de documentos do PowerPoint ####

Mantém registro de todas as informações sobre uma apresentação do PowerPoint e explica seu layout e conteúdo. É um fluxo obrigatório cujo nome DEVE ser "Documento do PowerPoint". O conteúdo desse fluxo é especificado por uma sequência de registros de nível superior. As restrições parciais de ordenação na sequência de registros são especificadas nos registros PersistDirectoryAtom e UserEditAtom.

Como registros de contêiner, os registros DocumentContainer, MainMasterContainer (seção 2.5.3), HandoutContainer (seção 2.5.8), SlideContainer (seção 2.5.1) e NotesContainer (seção 2.5.6) são a raiz de uma árvore de registros de contêiner e registros atômicos. Dentro de qualquer registro de contêiner, podem existir outros registros que não estejam explicitamente listados como registros filho. Registros desconhecidos são identificados quando o campo recType da estrutura RecordHeader (seção 2.3.1) contém um valor não especificado pela enumeração RecordType (seção 2.13.24). Esses registros desconhecidos, se encontrados, DEVEM ser ignorados e PODEM<1> ser preservados. Registros desconhecidos podem ser ignorados ao buscar bytes recLen de encaminhamento do final da estrutura RecordHeader.

Cada vez que esse fluxo é gravado, novos registros de nível superior, uma edição do usuário, podem ser anexados ao fluxo existente ou todo o conteúdo do fluxo pode ser substituído por uma sequência atualizada de registros de nível superior. Se o fluxo inteiro não for substituído, quaisquer registros de nível superior existentes anteriormente que compunham qualquer edição anterior do usuário podem se tornar obsoletos pelos registros de nível superior anexados subsequentemente que compõem a edição atual do usuário.

#### Fluxo de fotos ####

Este é um fluxo opcional que contém dados sobre as imagens contidas em uma apresentação do PowerPoint. Seu nome DEVE ser "Imagens". O conteúdo desse fluxo é especificado pelo registro OfficeArtBStoreDelay conforme especificado na seção [MS-ODRAW] 2.2.21.

#### Fluxo de informações resumidas ####

Mantém estatísticas sobre o documento seguindo o padrão Microsoft Office. O nome do Summary Information Stream deve ser "\005SummaryInformation", onde \005 é o caractere com valor 0x0005, não a string literal "\005". Este fluxo DEVE ser omitido para documentos criptografados. O conteúdo deste fluxo é especificado na seção [MS-OSHARED] 2.3.3.2.1.

#### Fluxo de informações do resumo do documento ####

Um fluxo opcional cujo nome DEVE ser "\005DocumentSummaryInformation", onde \005 é o caractere com valor 0x0005, não a string literal "\005". Este fluxo PODE<2> ser omitido para documentos criptografados. O conteúdo deste fluxo é especificado na seção [MS-OSHARED] 2.3.3.2.2.

#### Fluxo de informações resumidas criptografadas ####

Um fluxo opcional cujo nome DEVE ser "EncryptedSummary". Este fluxo existe apenas em um documento criptografado. O conteúdo deste fluxo é especificado na seção [MS-OFFCRYPTO] 2.3.5.4.

#### Armazenamento de assinatura digital ####

Um armazenamento opcional cujo nome DEVE ser "_xmlsignatures". PODE ser omitido e pode ser ignorado. O conteúdo deste armazenamento é especificado na seção [MS-OFFCRYPTO] 2.5.2.

#### Armazenamento de dados XML personalizado ####

Um armazenamento opcional cujo nome DEVE ser "MsoDataStore". O conteúdo do armazenamento é especificado na seção [MS-OSHARED] 2.3.6.

#### Fluxo de assinaturas ####

Um fluxo opcional cujo nome DEVE ser "_signatures". DEVE ser omitido e pode ser ignorado. O conteúdo deste fluxo é especificado na seção [MS-OFFCRYPTO] 2.5.1.

## Referências ##

* [Especificações do formato de arquivo PPT](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED]: Tipos de dados comuns do Office e estruturas de objetos](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] - Estrutura de criptografia de documentos do Office](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [Formatos de arquivo do PowerPoint](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)

