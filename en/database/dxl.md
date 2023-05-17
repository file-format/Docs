{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about DXL file format and APIs that can create and open DTSX files.",
  "title" : "DXL File Format - Domino XML Language File Format",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2023-05-16"
}

## What is a DXL file?

A DXL file is an XML based data storage file created for the enterprise level business collaboration software, Lotus Domino. It contains data related to a Lotus Domino database such as schemas, design elements, view, forms, documents, and the database data itself. [XML](/web/xml/) is a universal file format that can be read by software applications written in any programming language. It is also human-readable and can be opened with any text editor. That is why DXL files provide the capability to export data in interchangeable file format.

## DXL File Format

DXL files are saved in XML file format and are easily readable by applications written in any programming language. These files store data and settings in XML tags that categorize data as well as arrange it in a proper order

### DXL Output Example

Following is the output text excerpt output for a Notes document.

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

## References

 * [DXL Format - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)
