{
  "date": "2023-05-16",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi DXL-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DTSX-tiedostoja.",
  "title": "DXL-tiedostomuoto - Domino XML-kielen tiedostomuoto",
  "linktitle": "DXL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dx-fil"
}
},
  "lastmod": "2023-05-16"
}

## Mikä on DXL-tiedosto?

DXL-tiedosto on XML-pohjainen tallennustiedosto, joka on luotu yritystason yritysyhteistyöohjelmistoa, Lotus Dominoa varten. Se sisältää Lotus Domino -tietokantaan liittyviä tietoja, kuten skeemoja, suunnitteluelementtejä, näkymää, lomakkeita, asiakirjoja ja itse tietokantatietoja. {{HYPERLINKKI}} on yleinen tiedostomuoto, jota voivat lukea millä tahansa ohjelmointikielellä kirjoitetut ohjelmistosovellukset. Se on myös ihmisten luettavissa ja voidaan avata millä tahansa tekstieditorilla. Siksi DXL-tiedostot tarjoavat mahdollisuuden viedä tietoja vaihdettavassa tiedostomuodossa.

## DXL tiedostomuoto

DXL-tiedostot tallennetaan XML-tiedostomuodossa, ja ne ovat helposti luettavissa millä tahansa ohjelmointikielellä kirjoitetuilla sovelluksilla. Nämä tiedostot tallentavat tiedot ja asetukset XML-tunnisteisiin, jotka luokittelevat tiedot ja järjestävät sen oikeaan järjestykseen

### DXL-ulostuloesimerkki

Seuraavassa on Notes-asiakirjan tulostetekstiote.

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

## Viitteet

 * [DXL-muoto – Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

