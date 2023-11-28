{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aprenda sobre o formato de arquivo DXL e APIs que podem criar e abrir arquivos DTSX.",
  "title" :"Formato de arquivo DXL - formato de arquivo de linguagem Domino XML",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## O que é um arquivo .DXL?

Um arquivo DXL é um arquivo de armazenamento de dados baseado em XML criado para o software de colaboração empresarial de nível empresarial, Lotus Domino. Ele contém dados relacionados a um banco de dados Lotus Domino, como esquemas, elementos de design, visualização, formulários, documentos e os próprios dados do banco de dados. [XML](/pt/web/xml/) é um formato de arquivo universal que pode ser lido por aplicativos de software escritos em qualquer linguagem de programação. Também é legível por humanos e pode ser aberto com qualquer editor de texto. É por isso que os arquivos DXL oferecem a capacidade de exportar dados em formatos de arquivo intercambiáveis.

## Formato de arquivo DXL

Os arquivos DXL são salvos no formato de arquivo XML e podem ser facilmente lidos por aplicativos escritos em qualquer linguagem de programação. Esses arquivos armazenam dados e configurações em tags XML que categorizam os dados e os organizam na ordem adequada.

### Exemplo de saída DXL

A seguir está o trecho do texto de saída para um documento do Notes.

```
<document form="Customers">
	<noteinfo noteid="942" unid="431A199A6FCC9C0985256A54005041A1" sequence="1">
		<created>
			<datetime dst="true">20010522T103636,81-04</datetime>
		</created>
		<modified>
			<datetime dst="true">20010522T103709,78-04</datetime>
		</modified>
		<revised>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</revised>
		<lastaccessed>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</lastaccessed>
		<addedtofile>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</addedtofile>
	</noteinfo>
	<updatedby>
		<name>CN=Michelle Lally/OU=CAM/O=Acme</name>
	</updatedby>
	<item name="date">
		<datetime>20010601</datetime>
	</item>
	<item name="name">
		<text>Harry Hill</text>
	</item>
	</document>
```

## Referências

* [Formato DXL - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

