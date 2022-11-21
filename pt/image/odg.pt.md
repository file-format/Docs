{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo odg", "formato de arquivo odg", "o que é um arquivo odg", "arquivo", "exemplo odg", "extensão de arquivo odg", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo ODG",
  "description":"Saiba mais sobre o formato de arquivo ODG e APIs que podem criar e abrir arquivos ODG.",
  "linktitle" : "ODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo ODG?

O formato de arquivo ODG é usado pelo aplicativo Draw do Apache OpenOffice para armazenar elementos de desenho como uma imagem vetorial. Ele segue as especificações de formato de arquivo baseado em XML descritas pelo Advancement of Structural Information Standards (OASIS). ODG representa desenhos como imagens vetoriais usando pontos, linhas e curvas. Além do OpenOffice, o LibreOffice e outros aplicativos também oferecem suporte para trabalhar com o formato de arquivo ODG. Outros formatos suportados pelo OpenOffice, por exemplo, incluem [ODT](/pt/word-processing/odt/), ODF, [ODP](/pt/presentation/odp/) e [ODS](/pt/spreadsheet/ods/).


## Especificações de formato de arquivo ODG

O formato de arquivo ODG é baseado no formato OpenDocument que é um formato de documento XML estruturado com esquema bem definido.
Cada componente estrutural de um formato OpenDocument é representado por um elemento que possui atributos associados. A estrutura baseada em XML é comum para todos os tipos de documentos, como documento de texto, planilha ou arquivo de desenho. Um documento pode conter estilos diferentes. Uma estrutura de arquivo OpenDocument consiste nos seguintes elementos.
* Documento Raiz
* Metadados de documentos
* Tipos de elemento de corpo e documento
* Configurações do aplicativo
* Scripts
* Declarações de fonte
* Estilos
* Estilos e layouts de página

## Raízes do Documento ##

Um elemento raiz de documento contém o documento inteiro e é o elemento principal de um arquivo no formato OpenDocument. Os mesmos tipos de elementos raiz do documento são aplicáveis a todos os tipos de documento, como texto, documentos, planilhas e documentos de desenho.

### Elementos Raiz ###
Um único documento XML é representado por seu próprio elemento raiz. Os cinco elementos raiz suportados diferentes são os seguintes.

`<office:document> ` - Documento de escritório completo em um único documento XML.
`<office:document-content> ` - Conteúdo do documento e estilos automáticos usados no conteúdo.
`<office:document-styles> ` - Estilos usados no conteúdo do documento e estilos automáticos usados nos próprios estilos.
`<office:document-meta> ` - Documentar informações meta, como o autor ou a hora da última ação de salvamento.
`<office:document-settings> ` - Configurações específicas do aplicativo, como tamanho da janela ou informações da impressora.

### Metadados do Documento ODG ###
O OpenDocument contém todos os elementos de metadados no \<office:meta> elemento. Essas informações gerais sobre um documento estão contidas no início do documento e os aplicativos podem atualizar várias instâncias dos mesmos elementos.

### Elemento do corpo e tipos de documento ###
O corpo do documento indica o tipo de conteúdo contido no documento usando o elemento de tipo de documento. Esses tipos de documentos são:
* documentos de texto
* documentos de desenho
* documentos de apresentação
* planilhas de documentos
* documentos gráficos
* documentos de imagem

### Configurações do aplicativo ###
As configurações para aplicativos de escritório representam diferentes configurações relacionadas à configuração do documento ou à aparência visual do documento. Cada categoria é representada por um `<config:config-item-set> `. Exemplos de tais categorias de configuração incluem:
* Configurações do documento, por exemplo, impressora padrão
* Ver configurações, por exemplo, nível de zoom

### Scripts ###
É comum que um documento contenha vários scripts. Cada script em um arquivo OpenDocument é representado por um `<office:script> ` elemento. Esses elementos de script estão contidos em um único `<office:scripts> ` elemento. Os scripts não atualizam um documento enquanto o documento está sendo carregado.
### Declarações de tipo de fonte ###

Uma declaração de tipo de fonte contém informações sobre as fontes usadas pelo autor de um documento. Essas informações ajudam a localizar essas fontes em outros sistemas.
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### Estilos ###
Os estilos a seguir são suportados pelo formato OpenDocument.

`Estilos Comuns` - As representações XML de tais estilos são chamadas de estilos
`Estilos Automáticos` - Contém propriedades de formatação que, na visualização da interface do usuário de um documento, são atribuídas a um objeto como um parágrafo.
`Mater Styles` - um estilo comum que contém informações de formatação e conteúdo adicional que é exibido com o conteúdo do documento quando o estilo é aplicado. Um exemplo de estilo mestre são as páginas mestras.

## Referências ##
* [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Formato OpenDocument - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

