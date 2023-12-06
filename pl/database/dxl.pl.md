{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Dowiedz się o formacie pliku DXL i interfejsach API, które umożliwiają tworzenie i otwieranie plików DTSX.",
  "title" :"Format pliku DXL - Format pliku języka Domino XML",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## Czym jest plik DXL?

Plik DXL to plik do przechowywania danych oparty na formacie XML utworzony dla oprogramowania do współpracy biznesowej na poziomie przedsiębiorstwa, Lotus Domino. Zawiera dane powiązane z bazą danych Lotus Domino, takie jak schematy, elementy projektu, widoki, formularze, dokumenty i same dane bazy danych. [XML](/pl/web/xml/) to uniwersalny format pliku, który może być odczytywany przez aplikacje napisane w dowolnym języku programowania. Jest również czytelny dla człowieka i można go otworzyć w dowolnym edytorze tekstu. Dlatego pliki DXL umożliwiają eksport danych w wymiennym formacie pliku.

## Format pliku DXL

Pliki DXL są zapisywane w formacie XML i są łatwo czytelne dla aplikacji napisanych w dowolnym języku programowania. Pliki te przechowują dane i ustawienia w znacznikach XML, które kategoryzują dane i porządkują je w odpowiedniej kolejności

### Przykład wyjścia DXL

Poniżej znajduje się fragment tekstu wyjściowego dla dokumentu programu Notes.

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

## Bibliografia

* [Format DXL – Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

