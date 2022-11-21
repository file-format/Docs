{
  "date" : "2019-12-13",
  "keywords" :[ "arquivo pptx", "formato de arquivo pptx", "o que é um arquivo pptx", "arquivo", "exemplo pptx", "extensão de arquivo pptx","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo PPTX e APIs que podem criar e abrir arquivos PPTX.",
  "title" :"PPTX - Formato de arquivo de apresentação do PowerPoint",
  "linktitle" : "PPTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo PPTX?

Arquivos com extensão PPTX são arquivos de apresentação criados com o popular aplicativo Microsoft PowerPoint. Ao contrário da versão anterior do formato de arquivo de apresentação PPT, que era binário, o formato PPTX é baseado no formato de arquivo de apresentação XML aberto do Microsoft PowerPoint. Um arquivo de apresentação é uma coleção de slides em que cada slide pode conter texto, imagens, formatação, animações e outras mídias. Esses slides são apresentados ao público na forma de apresentações de slides com configurações de apresentação personalizadas.

## Breve história

O formato de arquivo PPTX foi introduzido em 2007 e usa o padrão Open XML adaptado pela Microsoft em 2000. Antes do PPTX, o formato de arquivo comum usado era o PPT, que era o formato de arquivo binário puro. O novo tipo de arquivo adicionou vantagens de tamanhos de arquivo pequenos, menos alterações de corrupção e representação de imagens bem formatadas. Foi no início de 2000, quando a Microsoft decidiu fazer a mudança para acomodar o padrão para **Office Open XML**. Em 2007, esse novo formato de arquivo passou a fazer parte do Office 2007 e é mantido também nas novas versões do Microsoft Office.

## Especificações de formato de arquivo PPTX

Arquivos gerados com o formato de arquivo Office Open XML é uma coleção de arquivos XML junto com outros arquivos que fornecem links entre todos os arquivos constituintes. Esta coleção é na verdade um arquivo compactado que pode ser extraído para visualizar seu conteúdo. Para isso, basta renomear a extensão do arquivo PPTX com zip e extraí-la para observar seu conteúdo (Consulte [especificações de formato de arquivo PPTX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-pptx/ efd8bb2d-d888-4e2e-af25-cad476730c9f) pela Microsoft).

As seções seguintes lançam alguma luz sobre cada uma delas.

### [Content_Types].xml

Este é o único arquivo encontrado no nível base quando o zip é extraído. Ele lista os tipos de conteúdo para peças dentro do pacote. Todas as referências aos arquivos XML incluídos no pacote são referenciadas neste arquivo XML. A seguir está um tipo de conteúdo para uma parte do slide:

```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```

Se novas partes precisarem ser adicionadas ao pacote, isso pode ser feito adicionando a nova parte e atualizando quaisquer relacionamentos dentro dos arquivos .rels. Deve-se ter em mente que para tal mudança, o Content_Types.xml também deve ser atualizado.

### \_rels (Pasta) ###

Os relacionamentos entre as outras partes e os recursos fora do pacote são mantidos pela parte de relacionamentos. A pasta Relacionamentos contém um único arquivo XML que armazena os relacionamentos em nível de pacote. Os links para as partes principais dos arquivos PPTX estão contidos neste arquivo como URIs. Esses URIs identificam o tipo de relacionamento de cada parte chave com o pacote. Isso inclui o relacionamento com o documento principal do escritório localizado como ppt/presentation.xml e outras partes dentro do docProps como propriedades principais e estendidas.

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
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
<Relationship Id#"rId2" Type#"http://. . ./hyperlink" Target#"http://www.google.com/" TargetMode#"External"/>
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

* [[MS-PPTX] - Formato de arquivo PPTX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-pptx/efd8bb2d-d888-4e2e-af25-cad476730c9f)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

