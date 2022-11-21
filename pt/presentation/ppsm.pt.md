{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo ppsm", "formato de arquivo ppsm", "o que é um arquivo ppsm", "arquivo", "exemplo ppsm", "extensão de arquivo ppsm", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PPSM - Arquivo de apresentação do PowerPoint habilitado para macro",
  "description":"Saiba mais sobre o formato de arquivo PPSM e APIs que podem criar e abrir arquivos PPSM.",
  "linktitle" : "PPSM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo PPSM?

Arquivos com extensão PPSM representam o formato de arquivo de apresentação de slides habilitado para macro criado com o Microsoft PowerPoint 2007 ou superior. Outro formato de arquivo semelhante é [PPTM](/pt/presentation/pptm/) que difere na abertura com o Microsoft PowerPoint em formato editável em vez de ser executado como Slide Show. Quando executado como apresentação de slides, o arquivo PPSM mostra os slides da apresentação com o conteúdo intacto na apresentação de slides e está no modo somente leitura por padrão. Os arquivos PPSM ainda podem ser editados no Microsoft PowerPoint abrindo-o no PowerPoint.

## Formato de arquivo ##

O formato de arquivo PPSM foi introduzido com o PowerPoint 2007 e é baseado no formato de arquivo OpenXML que usa uma combinação de XML e [ZIP](/pt/compression/zip/) para armazenar seu conteúdo. Arquivos gerados com o formato de arquivo Office Open XML é uma coleção de arquivos XML junto com outros arquivos que fornecem links entre todos os arquivos constituintes. Esta coleção é na verdade um arquivo compactado que pode ser extraído para visualizar seu conteúdo. Para isso, basta renomear a extensão do arquivo PPSM com zip e extraí-lo para observar seu conteúdo.

As seções seguintes lançam alguma luz sobre cada uma delas.

### [Content_Types].xml ###

Este é o único arquivo encontrado no nível base quando o zip é extraído. Ele lista os tipos de conteúdo para peças dentro do pacote. Todas as referências aos arquivos XML incluídos no pacote são referenciadas neste arquivo XML. A seguir está um tipo de conteúdo para uma parte do slide:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Se novas partes precisarem ser adicionadas ao pacote, isso pode ser feito adicionando a nova parte e atualizando quaisquer relacionamentos dentro dos arquivos .rels. Deve-se ter em mente que para tal mudança, o Content_Types.xml também deve ser atualizado.

### \_rels (Pasta) ###

Os relacionamentos entre as outras partes e os recursos fora do pacote são mantidos pela parte de relacionamentos. A pasta Relacionamentos contém um único arquivo XML que armazena os relacionamentos em nível de pacote. Os links para as partes principais dos arquivos de apresentação estão contidos neste arquivo como URIs. Esses URIs identificam o tipo de relacionamento de cada parte chave com o pacote. Isso inclui o relacionamento com o documento principal do escritório localizado como ppt/presentation.xml e outras partes dentro do docProps como propriedades principais e estendidas.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Cada parte do documento que é a fonte de um ou mais relacionamentos terá sua própria parte de relacionamentos onde cada parte de relacionamento é encontrada em uma subpasta \_rels da parte e é nomeada anexando '.rels' ao nome do papel. A parte de conteúdo principal (presentation.xml) tem sua própria parte de relacionamentos (presentation.xml.rels). Ele contém relacionamentos com outras partes do conteúdo, como slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, bem como os URIs para links externos.

#### Relacionamento explícito ####

Para um relacionamento explícito, um recurso é referenciado usando o atributo Id de um<Relationship> elemento. Ou seja, o Id na origem mapeia diretamente para um Id de um item de relacionamento, com uma referência explícita ao destino.

Por exemplo, um slide pode conter um hiperlink como este:
```
<a:hlinkClick r:id#"rId2">
```
O r:id#"rId2" faz referência ao seguinte relacionamento dentro da parte de relacionamentos do slide (slide1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Relação Implícita ####

Para um relacionamento implícito, não há referência direta a um `<Relationship> ID`. Em vez disso, a referência é compreendida.

### Pasta ppt ###

Esta é a pasta principal que contém todos os detalhes sobre o conteúdo da Apresentação. Por padrão, ele possui as seguintes pastas:

* \_rels
* tema
* diapositivos
* layouts de slides
* slideMasters

e os seguintes arquivos xml:

* apresentação.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## Referências ##

* [Formato de arquivo de apresentação OpenXML](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

