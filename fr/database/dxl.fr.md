{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Découvrez le format de fichier DXL et les API permettant de créer et d'ouvrir des fichiers DTSX.",
  "title" :"Format de fichier DXL - Format de fichier de langage XML Domino",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## Qu'est-ce qu'un fichier DXL ?

Un fichier DXL est un fichier de stockage de données basé sur XML créé pour le logiciel de collaboration commerciale au niveau de l'entreprise, Lotus Domino. Il contient des données liées à une base de données Lotus Domino, telles que des schémas, des éléments de conception, des vues, des formulaires, des documents et les données de la base de données elle-même. [XML](/fr/web/xml/) est un format de fichier universel qui peut être lu par des applications logicielles écrites dans n'importe quel langage de programmation. Il est également lisible par l’homme et peut être ouvert avec n’importe quel éditeur de texte. C'est pourquoi les fichiers DXL offrent la possibilité d'exporter des données dans un format de fichier interchangeable.

## Format de fichier DXL

Les fichiers DXL sont enregistrés au format de fichier XML et sont facilement lisibles par les applications écrites dans n'importe quel langage de programmation. Ces fichiers stockent les données et les paramètres dans des balises XML qui catégorisent les données et les organisent dans le bon ordre.

### Exemple de sortie DXL

Voici l’extrait de texte de sortie pour un document Notes.

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

## Les références

* [Format DXL - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

