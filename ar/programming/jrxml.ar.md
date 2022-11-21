{
  "date" : "2019-10-11",
  "keywords" :["jrxml" , "ملف jrxml" , "تنسيق ملف jrxml" , "تنسيق الملف" , "البرمجة" , "تنزيل ملف jrxml" , "ملف jrxml" , ".jrxml"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف JRXML وواجهات برمجة التطبيقات التي يمكنها فتح وإنشاء ملفات JRXML." ,
  "title" :"تنسيق ملف JRXML" ,
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف JRXML؟

يتم إنشاء ملف JRXML بواسطة JasperReports ويحتوي على تعريف تصميم بتنسيق ملف [XML] (/ar/ web / xml /) شائع. يخزن جميع عناصر التصميم مثل تخطيط التقرير وحقول النص والصور والمخططات والمعلمات والمتغيرات. JasperReports هي مكتبة Java تُستخدم لإنشاء التقارير برمجيًا عن طريق استرداد البيانات من قواعد البيانات الخلفية ووسائط التخزين.

## تنسيق ملف JRXML

ملفات JRXML هي ملفات نصية عادية يتم إنشاؤها بناءً على تنسيق ملف XML. يمكن لإطار عمل JasperReport التعامل مع أنواع مختلفة من مصادر البيانات. عندما يتم تجميع ملف .jrxml ، ينتج عنه ملف .jasper كإخراج. يتكون ملف jrxml من مجموعة من الأقسام. تحتوي بعض الأقسام على معلومات تتعلق بالخصائص المادية للصفحة مثل أبعاد الصفحة ، وموضع الحقول ، وارتفاع النطاقات ، بينما يتعلق البعض بالخصائص المنطقية مثل إعلان المعلمات والمتغيرات وتعريف الاستعلام لاختيار البيانات.

مثال على ملف JRXML

يظهر أدناه مثال لملف JRXML بسيط.
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

فيما يلي تفاصيل المثال.

"<queryString> "- هذا فارغ (لأننا نقوم بتمرير البيانات عبر Java Beans). يحتوي عادةً على جملة SQL ، والتي تسترجع نتيجة التقرير.

"<field name> "- يُستخدم هذا العنصر لتعيين البيانات من مصادر البيانات أو الاستعلامات في قوالب التقارير. يُعاد استخدام الاسم في نص التقرير ويكون حساسًا لحالة الأحرف.

"<fieldDescription> `- يرسم هذا العنصر اسم الحقل بالعنصر المناسب في ملف XML.

"<staticText> `- يحدد هذا النص الثابت الذي لا يعتمد على أي مصادر بيانات أو متغيرات أو معلمات أو تعبيرات تقرير.

"<band> "- تحتوي النطاقات على البيانات التي يتم عرضها في التقرير.

## مراجع

* [JRXML - ويكيبيديا] (https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [مصادر JRXML وملفات جاسبر] (https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

