{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru DXL a rozhraních API, která mohou vytvářet a otevírat soubory DTSX.",
  "title" :"Formát souboru DXL - Formát jazykového souboru Domino XML",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## Co je soubor DXL?

Soubor DXL je soubor úložiště dat založený na XML vytvořený pro software pro obchodní spolupráci na podnikové úrovni, Lotus Domino. Obsahuje data související s databází Lotus Domino, jako jsou schémata, prvky návrhu, pohled, formuláře, dokumenty a samotná data databáze. [XML](/cs/web/xml/) je univerzální formát souboru, který lze číst softwarovými aplikacemi napsanými v jakémkoli programovacím jazyce. Je také čitelný pro člověka a lze jej otevřít v libovolném textovém editoru. To je důvod, proč soubory DXL poskytují možnost exportovat data ve vyměnitelném formátu souborů.

## Formát souboru DXL

Soubory DXL jsou uloženy ve formátu XML a jsou snadno čitelné aplikacemi napsanými v jakémkoli programovacím jazyce. Tyto soubory ukládají data a nastavení do značek XML, které data kategorizují a také je uspořádají do správného pořadí

### Příklad výstupu DXL

Následuje výstup výstupního úryvku textu pro dokument Notes.

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

## Reference

* [Formát DXL – Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

