{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"تعرف على تنسيق ملف DXL وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات DTSX وفتحها.",
  "title" :"تنسيق ملف DXL - تنسيق ملف لغة Domino XML",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## ما هو ملف DXL؟

ملف DXL هو ملف تخزين بيانات قائم على XML تم إنشاؤه لبرنامج التعاون التجاري على مستوى المؤسسة, Lotus Domino. يحتوي على البيانات المتعلقة بقاعدة بيانات Lotus Domino مثل المخططات وعناصر التصميم والعرض والنماذج والمستندات وبيانات قاعدة البيانات نفسها. [XML](/ar/web/xml/) هو تنسيق ملف عالمي يمكن قراءته بواسطة التطبيقات البرمجية المكتوبة بأي لغة برمجة. كما أنه قابل للقراءة بواسطة الإنسان ويمكن فتحه باستخدام أي محرر نصوص. ولهذا السبب توفر ملفات DXL القدرة على تصدير البيانات بتنسيق ملف قابل للتبديل.

## تنسيق ملف دي اكس ال

يتم حفظ ملفات DXL بتنسيق ملف XML ويمكن قراءتها بسهولة بواسطة التطبيقات المكتوبة بأي لغة برمجة. تقوم هذه الملفات بتخزين البيانات والإعدادات في علامات XML التي تصنف البيانات بالإضافة إلى ترتيبها بترتيب مناسب

### مثال على إخراج DXL

فيما يلي إخراج مقتطف النص الناتج لمستند الملاحظات.

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

## مراجع

* [تنسيق DXL - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

