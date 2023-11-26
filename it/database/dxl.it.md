{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Informazioni sul formato file DXL e sulle API in grado di creare e aprire file DTSX.",
  "title" :"Formato file DXL - Formato file di lingua Domino XML",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## Cos'è un file DXL?

Un file DXL è un file di archiviazione dati basato su XML creato per il software di collaborazione aziendale a livello aziendale, Lotus Domino. Contiene dati relativi a un database Lotus Domino come schemi, elementi di progettazione, viste, moduli, documenti e i dati del database stesso. [XML](/it/web/xml/) è un formato di file universale che può essere letto da applicazioni software scritte in qualsiasi linguaggio di programmazione. È anche leggibile dall'uomo e può essere aperto con qualsiasi editor di testo. Ecco perché i file DXL offrono la possibilità di esportare dati in formato file intercambiabile.

## Formato file DXL

I file DXL vengono salvati in formato file XML e sono facilmente leggibili da applicazioni scritte in qualsiasi linguaggio di programmazione. Questi file memorizzano dati e impostazioni in tag XML che classificano i dati e li organizzano in un ordine corretto

### Esempio di uscita DXL

Di seguito è riportato l'output dell'estratto di testo di output per un documento Notes.

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

## Riferimenti

* [Formato DXL - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEments_XML.html)

