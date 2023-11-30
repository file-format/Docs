{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Дізнайтеся про формат файлу DXL та API, які можуть створювати та відкривати файли DTSX.",
  "title" :"Формат файлу DXL - формат файлу мови Domino XML",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## Що таке файл DXL?

Файл DXL — це файл зберігання даних на основі XML, створений для корпоративного програмного забезпечення для бізнес-співпраці Lotus Domino. Він містить дані, пов’язані з базою даних Lotus Domino, такі як схеми, елементи дизайну, подання, форми, документи та самі дані бази даних. [XML](/uk/web/xml/) — це універсальний формат файлу, який можуть читати програмні додатки, написані будь-якою мовою програмування. Він також зрозумілий людині та може бути відкритий у будь-якому текстовому редакторі. Ось чому файли DXL забезпечують можливість експорту даних у форматі взаємозамінних файлів.

## Формат файлу DXL

Файли DXL зберігаються у форматі файлу XML і легко читаються програмами, написаними будь-якою мовою програмування. Ці файли зберігають дані та параметри в тегах XML, які класифікують дані, а також впорядковують їх у належному порядку

### Приклад виводу DXL

Нижче наведено уривок вихідного тексту для документа Notes.

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

## Список літератури

* [Формат DXL – Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

