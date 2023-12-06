{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier DXL și despre API-urile care pot crea și deschide fișiere DTSX.",
  "title" :"Format de fișier DXL - Format de fișier Domino XML Language",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## Ce este un fișier DXL?

Un fișier DXL este un fișier de stocare a datelor bazat pe XML creat pentru software-ul de colaborare în afaceri la nivel de întreprindere, Lotus Domino. Conține date legate de o bază de date Lotus Domino, cum ar fi scheme, elemente de proiectare, vizualizare, formulare, documente și datele bazei de date în sine. [XML](/ro/web/xml/) este un format de fișier universal care poate fi citit de aplicațiile software scrise în orice limbaj de programare. De asemenea, este ușor de citit și poate fi deschis cu orice editor de text. De aceea, fișierele DXL oferă capacitatea de a exporta date în format de fișier interschimbabil.

## Format de fișier DXL

Fișierele DXL sunt salvate în format de fișier XML și sunt ușor de citit de aplicațiile scrise în orice limbaj de programare. Aceste fișiere stochează datele și setările în etichete XML care clasifică datele și le aranjează într-o ordine adecvată

### Exemplu de ieșire DXL

Mai jos este rezultatul extras de text de ieșire pentru un document Notes.

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

## Referințe

* [Format DXL - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

