{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ DXL และ API ที่สามารถสร้างและเปิดไฟล์ DTSX",
  "title" :"รูปแบบไฟล์ DXL - รูปแบบไฟล์ภาษา Domino XML",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## ไฟล์ DXL คืออะไร??

ไฟล์ DXL เป็นไฟล์จัดเก็บข้อมูลแบบ XML ที่สร้างขึ้นสำหรับซอฟต์แวร์การทำงานร่วมกันทางธุรกิจระดับองค์กร Lotus Domino ประกอบด้วยข้อมูลที่เกี่ยวข้องกับฐานข้อมูล Lotus Domino เช่น สคีมา องค์ประกอบการออกแบบ มุมมอง แบบฟอร์ม เอกสาร และข้อมูลฐานข้อมูลเอง [XML](/th/web/xml/) เป็นรูปแบบไฟล์สากลที่แอปพลิเคชันซอฟต์แวร์ที่เขียนในภาษาการเขียนโปรแกรมใดๆ สามารถอ่านได้ นอกจากนี้ยังสามารถอ่านได้โดยมนุษย์และสามารถเปิดด้วยโปรแกรมแก้ไขข้อความใดก็ได้ นั่นคือสาเหตุที่ไฟล์ DXL มอบความสามารถในการส่งออกข้อมูลในรูปแบบไฟล์ที่ใช้แทนกันได้

## รูปแบบไฟล์ DXL

ไฟล์ DXL จะถูกบันทึกในรูปแบบไฟล์ XML และสามารถอ่านได้ง่ายโดยแอปพลิเคชันที่เขียนในภาษาการเขียนโปรแกรมใด ๆ ไฟล์เหล่านี้จัดเก็บข้อมูลและการตั้งค่าในแท็ก XML ที่จัดหมวดหมู่ข้อมูลและจัดเรียงตามลำดับที่เหมาะสม

### ตัวอย่างเอาต์พุต DXL

ต่อไปนี้เป็นเอาต์พุตข้อความที่ตัดตอนมาสำหรับเอกสาร Notes

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

## อ้างอิง

* [รูปแบบ DXL - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

