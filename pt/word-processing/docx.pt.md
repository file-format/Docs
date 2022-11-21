{
  "date" : "2019-12-03",
  "keywords" :[ "DOCX", "arquivo", "formato", "tipo de arquivo", "extensão", "o que é um arquivo DOCX?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOCX",
  "description":"Saiba mais sobre o formato de arquivo DOCX e APIs que podem criar e abrir arquivos DOCX.",
  "linktitle" : "DOCX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## O que é um arquivo DOCX? ##

DOCX é um formato bem conhecido para documentos do Microsoft Word. Introduzido a partir de 2007 com o lançamento do Microsoft Office 2007, a estrutura desse novo formato de documento foi alterada de binário simples para uma combinação de arquivos XML e binários. Os arquivos Docx podem ser abertos com o Word 2007 e versões laterais, mas não com as versões anteriores do MS Word que suportam extensões de arquivo DOC.

## Breve história ##

Depois que a Microsoft abriu as especificações para o formato de arquivo DOC, foi fácil para seus concorrentes fazer engenharia reversa do formato e fornecer o mesmo suporte em seus próprios aplicativos. Além disso, a concorrência do Open Office na forma de seu Open Document Format, obrigou a Microsoft a adotar padrões mais abertos e amplos. Foi no início de 2000 quando a Microsoft decidiu fazer a mudança para acomodar o padrão para **Office Open XML**. Os documentos sob este novo Padrão receberam [extensão .docx](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), o "X" sendo para XML. Em 2007, esse novo formato de arquivo passou a fazer parte do Office 2007 e é mantido também nas novas versões do Microsoft Office. O novo tipo de arquivo adicionou vantagens de tamanhos de arquivo pequenos, menos alterações de corrupção e representação de imagens bem formatadas.

## Especificações de formato de arquivo DOCX - Mais informações

Um arquivo Docx é composto por uma coleção de arquivos XML contidos em um arquivo ZIP. O conteúdo de um novo documento do Word pode ser visualizado descompactando seu conteúdo. A coleção contém uma lista de arquivos XML que são categorizados como:

* Arquivos de Metadados - contém informações sobre outros arquivos disponíveis no arquivo
* Documento - contém o conteúdo real do documento

### Arquivos de metadados ###

O Microsoft Word usa esses arquivos para localizar a relação entre arquivos e localizar o conteúdo do documento. Quando um arquivo de documento do Word é extraído, ele contém vários desses arquivos, conforme detalhado abaixo.

#### Relacionamentos - \_rels/.rels ####

Este arquivo contém informações que informam ao MS Word onde procurar o conteúdo do documento e outras referências. Cada relacionamento é identificado por um ID de relacionamento exclusivo e especifica o arquivo XML referenciado como destino. Um arquivo de relacionamento de amostra é mostrado a seguir:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### Tipos de conteúdo ####

Um documento pode conter vários tipos de mídia como imagens, temas, word art, etc. O [Content_Types].xml contém informações sobre esses tipos de mídia presentes no documento. O conteúdo de tal arquivo XML é mostrado a seguir:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### Referências a recursos - \_rels/document.xml.rels ####

Informações sobre recursos, como imagens incorporadas no documento, são referenciadas neste arquivo XML.

#### Conteúdo do Documento Principal ####

Refere-se ao arquivo XML principal do arquivo que contém o conteúdo de texto do documento. Este conteúdo é representado por uma variedade de nós de acordo com as especificações XML do OpenOffice. Principalmente o conteúdo deste arquivo consiste em Parágrafos e Tabelas, embora também possam ser outros nós.

### Nós de formato de arquivo ###

O arquivo document.xml principal é uma coleção de nós para representação do conteúdo geral de um arquivo. Cada nó tem um início e um fim que encapsula outros nós ou o conteúdo. Um exemplo simplificado de tal arquivo xml é o seguinte:

```
<w:document>
   <w:body>
       <w:p w:rsidR#"005F670F" w:rsidRDefault#"005F79F5">
           <w:r><w:t>Example Document</w:t></w:r>
       </w:p>
       <w:sectPr w:rsidR#"005F670F">
           <w:pgSz w:w#"12240" w:h#"15840"/>
           <w:pgMar w:top#"1440" w:right#"1440" w:bottom#"1440" w:left#"1440" w:header#"720" w:footer#"720"
                    w:gutter#"0"/>
           <w:cols w:space#"720"/>
           <w:docGrid w:linePitch#"360"/>
       </w:sectPr>
   </w:body>
</w:document>
```

A seguir estão as informações sobre alguns dos nós contidos em um arquivo DOCX para representação de conteúdo.

`<w:document> ` - Representa o elemento raiz do conteúdo principal do arquivo.

`<w:body> ` - Representa o corpo do documento que pode ser composto por muitos outros nós de elementos, como parágrafos, tabelas e seções.

#### Parágrafos ####

Um parágrafo é o principal detentor de conteúdo dentro de um documento. É representado por **<w:p> ** elemento dentro de um documento. Um parágrafo consiste ainda em uma ou mais execuções **<w:r> ** que contém o texto real do parágrafo. Além das execuções, os parágrafos também podem conter outros elementos do documento, como hiperlinks, comentários, etc. Um exemplo de estrutura de parágrafo é mostrado abaixo:

```
<w:p>
<w:pPr>
<w:pStyle> w:val#"MyStyle"/>
<w:spacing w:before#"120" w:after#"120"/>
</w:pPr>
<w:r>
<w:t xml"space#"preserve">A paragraph is main container in a document that further consists of a one or more runs where the text of paragraph is actually contained.</w:t>
</w:r>
</w:p>
```

## Referências ##

* [MS - Formato de arquivo DOCX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)
* [Office Open XML](http://officeopenxml.com/)

