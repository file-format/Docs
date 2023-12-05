{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Научете за файловия формат DXL и API, които могат да създават и отварят DTSX файлове.",
  "title" :"DXL файлов формат – Domino XML езиков файлов формат",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## Какво е DXL файл?

DXL файлът е базиран на XML файл за съхранение на данни, създаден за софтуера за бизнес сътрудничество на корпоративно ниво, Lotus Domino. Той съдържа данни, свързани с база данни на Lotus Domino, като схеми, елементи на дизайна, изглед, формуляри, документи и самата база данни. [XML](/bg/web/xml/) е универсален файлов формат, който може да се чете от софтуерни приложения, написани на всеки език за програмиране. Освен това е четим от хора и може да се отвори с всеки текстов редактор. Ето защо DXL файловете предоставят възможност за експортиране на данни във взаимозаменяем файлов формат.

## DXL файлов формат

DXL файловете се записват в XML файлов формат и са лесни за четене от приложения, написани на всеки език за програмиране. Тези файлове съхраняват данни и настройки в XML тагове, които категоризират данните, както и ги подреждат в правилен ред

### Пример за DXL изход

Следва изходният изваден текст за документ на Notes.

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

## Препратки

* [DXL формат - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

