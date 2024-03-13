{
  "date": "2023-05-16",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "DXL fayl formatı və DTSX fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "DXL Fayl Format - Domino XML Dil Fayl Format",
  "linktitle": "DXL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dx-azl"
}
},
  "lastmod": "2023-05-16"
}

## DXL faylı nədir?

DXL faylı korporativ səviyyəli işgüzar əməkdaşlıq proqramı olan Lotus Domino üçün yaradılmış XML əsaslı məlumat saxlama faylıdır. O, sxemlər, dizayn elementləri, görünüş, formalar, sənədlər və verilənlər bazası məlumatlarının özü kimi Lotus Domino verilənlər bazası ilə əlaqəli məlumatları ehtiva edir. [XML](/web/xml/) istənilən proqramlaşdırma dilində yazılmış proqram proqramları tərəfindən oxuna bilən universal fayl formatıdır. O, həmçinin insanlar tərəfindən oxuna bilər və istənilən mətn redaktoru ilə açıla bilər. Buna görə DXL faylları məlumatları dəyişdirilə bilən fayl formatında ixrac etmək imkanı verir.

## DXL fayl formatı

DXL faylları XML fayl formatında saxlanılır və istənilən proqramlaşdırma dilində yazılmış proqramlar tərəfindən asanlıqla oxunur. Bu fayllar məlumatları və parametrləri XML teqlərində saxlayır ki, onlar məlumatları kateqoriyalara ayırır və onları müvafiq qaydada təşkil edir

### DXL Çıxış Nümunəsi

Aşağıda Notes sənədi üçün çıxış mətnindən çıxarış verilmişdir.

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

## İstinadlar

 * [DXL Format - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

