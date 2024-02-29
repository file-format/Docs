{
  "date": "2023-05-16",
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل DXL و APIهایی که می توانند فایل های DTSX را ایجاد و باز کنند، بیاموزید.",
  "title": "فرمت فایل DXL - فرمت فایل زبان دومینو XML",
  "linktitle": "DXL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dx-fal"
}
}،
  "lastmod": "2023-05-16"
}

## فایل DXL چیست؟

یک فایل DXL یک فایل ذخیره‌سازی داده مبتنی بر XML است که برای نرم‌افزار همکاری تجاری سطح سازمانی، Lotus Domino، ایجاد شده است. این شامل داده های مربوط به پایگاه داده Lotus Domino مانند طرحواره ها، عناصر طراحی، نماها، فرم ها، اسناد و داده های خود پایگاه داده است. [XML](/web/xml/) یک فرمت فایل جهانی است که می تواند توسط برنامه های کاربردی نرم افزار نوشته شده به هر زبان برنامه نویسی خوانده شود. همچنین برای انسان قابل خواندن است و با هر ویرایشگر متنی قابل باز شدن است. به همین دلیل است که فایل‌های DXL قابلیت صادرات داده‌ها را در قالب فایل قابل تعویض فراهم می‌کنند.

## فرمت فایل DXL

فایل های DXL در فرمت فایل XML ذخیره می شوند و به راحتی توسط برنامه های نوشته شده به هر زبان برنامه نویسی قابل خواندن هستند. این فایل‌ها داده‌ها و تنظیمات را در تگ‌های XML ذخیره می‌کنند که داده‌ها را دسته‌بندی می‌کنند و همچنین آن‌ها را به ترتیب مناسب مرتب می‌کنند

### نمونه خروجی DXL

در زیر خروجی گزیده متن خروجی برای یک سند Notes آمده است.

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

## منابع

 * [فرمت DXL - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

