{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl", "arquivo xbrl", "formato de arquivo xbrl", "tipo de arquivo xbrl", "arquivo", "tipo", "o que é um arquivo xbrl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - Formato de arquivo de relatórios comerciais e financeiros",
  "description":"Saiba mais sobre o formato de arquivo XBRL e APIs que podem criar e abrir arquivos XBRL.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## O que é um arquivo XBRL?

Um arquivo com extensão .xbrl (eXtensible Business Reporting Language) é uma estrutura global disponível gratuitamente para troca de informações comerciais. Atualmente, é amplamente utilizado como um dos formatos padrão que substituiu os antigos relatórios em papel por registros digitais mais úteis e precisos. Os dados trocados usando os arquivos XBRL incluem livros-razão, detalhes financeiros e balanços. Ele suporta tags de dados que permitem o processamento de dados desde a preparação até a fase de análise de informações comerciais de todos os tipos. Arquivos XBRL podem ser abertos usando software como Rivet Software Dragon View XBRL Viewer e APIs como [Aspose.Finance](https://products.aspose.com/finance).

## Formato de arquivo XBRL

XBRL é um padrão internacional aberto para relatórios de negócios digitais amplamente utilizado globalmente. É uma linguagem baseada em [XML](/pt/web/xml/) que usa elementos XBRL, conhecidos como tags, para descrever cada item de dados de negócios para formular dados para classificação e análise de relatórios. As especificações de formato de arquivo XBRL são desenvolvidas e publicadas pela XBRL International, Inc, com [XBRL versão 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) atualmente disponíveis para os usuários.

### Estrutura do Documento XBRL

Informações completas sobre as [tags XBRL 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata- 2013-02-20.html) pode ser consultado por programadores para escrever aplicativos para trabalhar neste formato de arquivo. Um XBRL consiste em uma instância XBRL e uma coleção de taxonomias.

**`XBRL Instance`** - A instância XBRL começa com o<xbrl> elemento raiz. Um documento XML grande pode conter mais de uma instância XBRL incorporada nele.

**`Taxonomia XBRL`** - A [Taxonomia XBRL](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31 +corrected-errata-2013-02-20.html#_5) é definido como estruturas de esquema XML e conjunto de elementos de links externos diretamente referenciados. Um esquema de taxonomia escalável mostrando as referências do linkbase é o seguinte.

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## Referências ##

* [XBRL - Por Wikipedia](https://en.wikipedia.org/wiki/XBRL)
* [Extensible Business Reporting Language (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected- errata-2013-02-20.html)

