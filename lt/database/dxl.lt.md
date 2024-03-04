{
  "date": "2023-05-16",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie DXL failo formatą ir API, kurios gali kurti ir atidaryti DTSX failus.",
  "title": "DXL failo formatas – Domino XML kalbos failo formatas",
  "linktitle": "DXL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dx-ltl"
}
},
  "lastmod": "2023-05-16"
}

## Kas yra DXL failas?

DXL failas yra XML pagrįstas duomenų saugojimo failas, sukurtas įmonės lygio verslo bendradarbiavimo programinei įrangai Lotus Domino. Jame yra duomenų, susijusių su Lotus Domino duomenų baze, pvz., schemos, dizaino elementai, rodinys, formos, dokumentai ir patys duomenų bazės duomenys. [XML](/web/xml/) yra universalus failo formatas, kurį gali skaityti bet kokia programavimo kalba parašytos programinės įrangos programos. Jis taip pat yra skaitomas žmonėms ir gali būti atidarytas naudojant bet kurį teksto rengyklę. Štai kodėl DXL failai suteikia galimybę eksportuoti duomenis keičiamu failo formatu.

## DXL failo formatas

DXL failai išsaugomi XML failo formatu ir yra lengvai skaitomi bet kuria programavimo kalba parašytomis programomis. Šiuose failuose duomenys ir nustatymai saugomi XML žymose, kurios suskirsto duomenis į kategorijas ir išdėsto juos tinkama tvarka

### DXL išvesties pavyzdys

Toliau pateikiama pastabų dokumento išvesties teksto ištrauka.

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

## Nuorodos

 * [DXL formatas – Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

