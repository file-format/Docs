{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd","o que é um arquivo xsd","como abrir um arquivo xsd", "extensão", "arquivo", "arquivo xsd","formato de arquivo xsd", "extensão .xsd" ,"exemplo de arquivo xsd"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :" Saiba mais sobre o formato de arquivo XSD e APIs que podem criar e abrir um arquivo XSD.",
  "title" :"Formato de arquivo XSD - Arquivo de definição de esquema XML",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## O que é um arquivo de esquema XSD?

Um arquivo XSD é um arquivo de definição que especifica os elementos e atributos que podem fazer parte de um documento XML. Isso garante que os dados sejam interpretados adequadamente e que os erros sejam detectados, resultando na validação de XML apropriada. Os arquivos XSD garantem que os dados inseridos sigam a mesma estrutura definida no arquivo. Os arquivos XSD são armazenados no formato de arquivo [XML](/pt/web/xml/) e podem ser abertos ou editados em qualquer editor de texto, como Microsoft Notepad, Notepad++ ou [Microsoft XML Notepad](https://microsoft.github.io /XmlNotepad/).

## Formato de arquivo XSD

Os arquivos XSD são armazenados no disco em formato de arquivo de texto simples que é legível por humanos. Um XSD define os elementos que podem ser usados nos documentos, relacionados aos dados reais com os quais deve ser codificado.

## Exemplo de arquivo XSD

Um arquivo XSD simples com um esquema de ordem de compra define os elementos usando tags conforme mostrado a seguir [exemplo XSD da Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file -simple-schema?view=vs-2022).

```
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"
           xmlns:tns="http://tempuri.org/PurchaseOrderSchema.xsd"
           targetNamespace="http://tempuri.org/PurchaseOrderSchema.xsd"
           elementFormDefault="qualified">
 <xsd:element name="PurchaseOrder" type="tns:PurchaseOrderType"/>
 <xsd:complexType name="PurchaseOrderType">
  <xsd:sequence>
   <xsd:element name="ShipTo" type="tns:USAddress" maxOccurs="2"/>
   <xsd:element name="BillTo" type="tns:USAddress"/>
  </xsd:sequence>
  <xsd:attribute name="OrderDate" type="xsd:date"/>
 </xsd:complexType>

 <xsd:complexType name="USAddress">
  <xsd:sequence>
   <xsd:element name="name"   type="xsd:string"/>
   <xsd:element name="street" type="xsd:string"/>
   <xsd:element name="city"   type="xsd:string"/>
   <xsd:element name="state"  type="xsd:string"/>
   <xsd:element name="zip"    type="xsd:integer"/>
  </xsd:sequence>
  <xsd:attribute name="country" type="xsd:NMTOKEN" fixed="US"/>
 </xsd:complexType>
</xsd:schema>
```

Aqui, as seguintes tags são usadas.

* `xs:element` - Define um elemento.
* `xs:sequence` - Indica que os elementos filhos aparecem apenas na ordem mencionada.
* `xs:complexType` - Indica que contém outros elementos.
* `xs:simpleType` - Indica que eles não contêm outros elementos.
* `type` - string, decimal, integer, boolean, date, time,

## Referências ##

- [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)
- [Exemplo de exemplo de XSD](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

