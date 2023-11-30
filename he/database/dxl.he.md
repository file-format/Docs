{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ DXL וממשקי API שיכולים ליצור ולפתוח קובצי DTSX.",
  "title" :"פורמט קובץ DXL - פורמט קובץ שפת XML של Domino",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## מהו קובץ DXL?

קובץ DXL הוא קובץ אחסון נתונים מבוסס XML שנוצר עבור תוכנת שיתוף פעולה עסקי ברמה הארגונית, Lotus Domino. הוא מכיל נתונים הקשורים למסד נתונים של Lotus Domino כגון סכמות, רכיבי עיצוב, תצוגה, טפסים, מסמכים ונתוני מסד הנתונים עצמם. [XML](/he/web/xml/) הוא פורמט קובץ אוניברסלי שניתן לקרוא על ידי יישומי תוכנה הכתובים בכל שפת תכנות. זה גם קריא אנושי וניתן לפתוח אותו עם כל עורך טקסט. זו הסיבה שקובצי DXL מספקים את היכולת לייצא נתונים בפורמט קובץ שניתן להחלפה.

## פורמט קובץ DXL

קבצי DXL נשמרים בפורמט קובץ XML וניתנים לקריאה בקלות על ידי יישומים הכתובים בכל שפת תכנות. קבצים אלה מאחסנים נתונים והגדרות בתגיות XML שמסווגות נתונים וכן מסדרים אותם בסדר מתאים

### דוגמה לפלט DXL

להלן פלט קטע טקסט פלט עבור מסמך Notes.

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

## הפניות

* [פורמט DXL - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

