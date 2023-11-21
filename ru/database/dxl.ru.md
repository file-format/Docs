{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Узнайте о формате файлов DXL и API, с помощью которых можно создавать и открывать файлы DTSX.",
  "title" :"Формат файла DXL — формат файла языка Domino XML",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## .DXL вариант №

Файл DXL — это файл хранения данных на основе XML, созданный для программного обеспечения для совместной работы на уровне предприятия Lotus Domino. Он содержит данные, связанные с базой данных Lotus Domino, такие как схемы, элементы дизайна, представления, формы, документы и сами данные базы данных. [XML](/ru/web/xml/) — универсальный формат файлов, который могут читаться программными приложениями, написанными на любом языке программирования. Он также удобен для чтения и может быть открыт в любом текстовом редакторе. Вот почему файлы DXL предоставляют возможность экспортировать данные в взаимозаменяемом формате файлов.

## Формат файла DXL

Файлы DXL сохраняются в формате XML и легко читаются приложениями, написанными на любом языке программирования. Эти файлы хранят данные и настройки в тегах XML, которые классифицируют данные, а также упорядочивают их в правильном порядке.

### Пример вывода DXL

Ниже приведен отрывок выходного текста для документа Notes.

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

## Рекомендации

* [Формат DXL — Microsoft] (https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

