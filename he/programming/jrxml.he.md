{
  "date" : "2019-10-11",
  "keywords" :[ "jrxml", "קובץ jrxml", "פורמט קובץ jrxml", "פורמט קובץ", "תכנות","הורדת קובץ jrxml", "קובץ jrxml", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ JRXML וממשקי API שיכולים לפתוח וליצור קובצי JRXML.",
  "title" :"פורמט קובץ JRXML",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ JRXML?

קובץ JRXML נוצר על ידי JasperReports ומכיל הגדרת עיצוב בפורמט קובץ [XML](/he/web/xml/) פופולרי. הוא מאחסן את כל רכיבי העיצוב כגון פריסת דוחות, שדות טקסט, תמונות, תרשימים, פרמטרים ומשתנים. JasperReports היא ספריית Java המשמשת ליצירת דוחות באופן פרוגרמטי על ידי אחזור נתונים ממסדי נתונים עורפיים וממדיה אחסון.

## פורמט קובץ JRXML

קובצי JRXML הם קבצי טקסט רגיל שנוצרים על סמך פורמט קובץ ה-XML. מסגרת JasperReport יכולה להתמודד עם סוגים שונים של מקורות נתונים. כאשר קובץ ‎.jrxml מורכב, זה גורם לקובץ ‎.jasper כפלט. קובץ jrxml מורכב מקבוצה של מקטעים. חלק מהקטעים מכילים מידע הקשור למאפיינים הפיזיים של הדף כגון מימד העמוד, מיקום השדות וגובה הפסים, בעוד שחלקם נוגעים למאפיינים הלוגיים כגון הצהרת הפרמטרים והמשתנים והגדרת שאילתה לבחירת נתונים.

### דוגמה לקובץ JRXML

דוגמה פשוטה של קובץ JRXML מוצגת להלן.
```
<a name="kanchor14"></a><?xml version="1.0" encoding="UTF-8"?>
<jasperReport xmlns="http://jasperreports.sourceforge.net/jasperreports"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xsi:schemaLocation="http://jasperreports.sourceforge.net/jasperreports
        http://jasperreports.sourceforge.net/xsd/jasperreport.xsd"
      name="My first report" pageWidth="595" pageHeight="842" columnWidth="535"
      leftMargin="20" rightMargin="20" topMargin="20" bottomMargin="20">
  <queryString language="SQL">
    <![CDATA[select * from address order by city]]>
  </queryString>
  <field name="ID" class="java.lang.Integer">
    <fieldDescription><![CDATA[]]></fieldDescription>
  </field>
  <field name="FIRSTNAME" class="java.lang.String">
    <fieldDescription><![CDATA[]]></fieldDescription>
  </field>
  <field name="LASTNAME" class="java.lang.String">
    <fieldDescription><![CDATA[]]></fieldDescription>
  </field>
  <field name="STREET" class="java.lang.String">
    <fieldDescription><![CDATA[]]></fieldDescription>
  </field>
  <field name="CITY" class="java.lang.String">
    <fieldDescription><![CDATA[]]></fieldDescription>
  </field>
```
```
<group name="CITY">
    <groupExpression><![CDATA[$F{CITY}]]></groupExpression>
    <groupHeader>
      <band height="27">
        <staticText>
          <reportElement mode="Opaque" x="0" y="0" width="139" height="27"
          forecolor="#FFFFFF" backcolor="#000000"/>
          <textElement>
            <font size="18"/>
          </textElement>
        <text><![CDATA[CITY]]></text>
      </staticText>
      <textField hyperlinkType="None">
        <reportElement mode="Opaque" x="139" y="0" width="416" height="27"
        forecolor="#FFFFFF" backcolor="#000000"/>
        <textElement>
          <font size="18" isBold="true"/>
        </textElement>
        <textFieldExpression class="java.lang.String"><![CDATA[$F{CITY}]]>
        </textFieldExpression>
      </textField>
    </band>
  </groupHeader>
  <groupFooter>
    <band height="8">
      <line direction="BottomUp">
        <reportElement key="line" x="1" y="4" width="554" height="1"/>
      </line>
    </band>
  </groupFooter>
</group>

<background>
  <band/>
</background>
  <title>
    <band height="58">
      <line>
        <reportElement x="0" y="8" width="555" height="1"/>
      </line>
      <line>
        <reportElement positionType="FixRelativeToBottom" x="0" y="51" width="555"
             height="1"/>
      </line>

      <staticText>
        <reportElement x=”65” y=”13” width ”424” height=”35”/>
        <textElement textAlignment=”Center”>
          <font size=”26” isBold=”true”/>
        </textElement>
      <text><![CDATE[Classic template]]> </text>
    </staticText>
</band>
</title>
  <pageHeader>
    <band/>
  </pageHeader>
  <columnHeader>
    <band height="18">
      <staticText>
        <reportElement mode="Opaque" x="0" y="0" width="138" height="18"
        forecolor="#FFFFFF" backcolor="#999999"/>
        <textElement>
          <font size="12"/>
        </textElement>
        <text><![CDATA[ID]]></text>
      </staticText>
      <staticText>
        <reportElement mode="Opaque" x="138" y="0" width="138" height="18"
        forecolor="#FFFFFF" backcolor="#999999"/>
        <textElement>
          <font size="12"/>
        </textElement>
        <text><![CDATA[FIRSTNAME]]></text>
      </staticText>
      <staticText>
        <reportElement mode="Opaque" x="276" y="0" width="138" height="18"
        forecolor="#FFFFFF" backcolor="#999999"/>
        <textElement>
          <font size="12"/>
        </textElement>
        <text><![CDATA[LASTNAME]]></text>
      </staticText>
      <staticText>
        <reportElement mode="Opaque" x="414" y="0" width="138" height="18"
        forecolor="#FFFFFF" backcolor="#999999"/>
        <textElement>
          <font size="12"/>
        </textElement>
        <text><![CDATA[STREET]]></text>
      </staticText>
    </band>
  </columnHeader>
```

להלן הפרטים של הדוגמה.

`<queryString> ` - זה ריק (כאשר אנו מעבירים נתונים דרך Java Beans). בדרך כלל מכיל את הצהרת SQL, אשר מאחזרת את תוצאת הדוח.

`<field name> ` - אלמנט זה משמש למיפוי נתונים ממקורות נתונים או שאילתות, לתבניות דוחות. נעשה שימוש חוזר בשם בגוף הדוח והוא תלוי רישיות.

`<fieldDescription> ` אלמנט זה ממפה את שם השדה עם האלמנט המתאים בקובץ ה-XML.

`<staticText> ` − זה מגדיר את הטקסט הסטטי שאינו תלוי במקורות נתונים, משתנים, פרמטרים או ביטויי דוח.

`<band> ` - להקות מכילות את הנתונים, המוצגים בדוח.

## הפניות

* [JRXML - ויקיפדיה](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [מקורות JRXML וקבצי Jasper](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

