{
  "date" : "2019-10-11",
  "keywords" : [ "jrxml", "jrxml file", "jrxml file format", "file format", "programming","jrxml file download", ".jrxml file", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"JRXML ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা JRXML ফাইল খুলতে এবং তৈরি করতে পারে।",
  "title" : "JRXML ফাইল ফরম্যাট",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## একটি JRXML ফাইল কি?

একটি JRXML ফাইল JasperReports দ্বারা তৈরি করা হয়েছে এবং জনপ্রিয় [XML](/web/xml/) ফাইল বিন্যাসে ডিজাইনের সংজ্ঞা রয়েছে৷ এটি রিপোর্ট লেআউট, টেক্সট ক্ষেত্র, ছবি, চার্ট, প্যারামিটার এবং ভেরিয়েবলের মতো সমস্ত ডিজাইন উপাদান সঞ্চয় করে। JasperReports হল একটি জাভা লাইব্রেরি যা ব্যাকএন্ড ডেটাবেস এবং স্টোরেজ মিডিয়া থেকে ডেটা পুনরুদ্ধার করে প্রোগ্রামগতভাবে রিপোর্ট তৈরি করতে ব্যবহৃত হয়।

## JRXML ফাইল ফরম্যাট

JRXML ফাইল হল প্লেইন টেক্সট ফাইল যা XML ফাইল ফরম্যাটের উপর ভিত্তি করে তৈরি করা হয়। JasperReport ফ্রেমওয়ার্ক বিভিন্ন ধরণের ডেটা উত্স পরিচালনা করতে পারে। যখন একটি .jrxml ফাইল কম্পাইল করা হয়, এটি আউটপুট হিসাবে .jasper ফাইলে পরিণত হয়। একটি jrxml ফাইলে কয়েকটি বিভাগ থাকে। কিছু বিভাগে পৃষ্ঠার শারীরিক বৈশিষ্ট্যগুলির সাথে সম্পর্কিত তথ্য রয়েছে যেমন পৃষ্ঠার মাত্রা, ক্ষেত্রগুলির অবস্থান এবং ব্যান্ডগুলির উচ্চতা, কিছু অংশে যৌক্তিক বৈশিষ্ট্যগুলি যেমন প্যারামিটার এবং ভেরিয়েবলের ঘোষণা এবং একটি প্রশ্নের সংজ্ঞা রয়েছে। তথ্য নির্বাচনের জন্য।

### JRXML ফাইলের উদাহরণ

একটি সাধারণ JRXML ফাইলের উদাহরণ নীচে দেখানো হয়েছে।
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

নিম্নে উদাহরণের বিবরণ দেওয়া হল।

`<queryString> ` - এটি খালি (যেহেতু আমরা জাভা বিনসের মাধ্যমে ডেটা পাঠাচ্ছি)। সাধারণত SQL স্টেটমেন্ট থাকে, যা রিপোর্টের ফলাফল পুনরুদ্ধার করে।

`<field name> ` − এই উপাদানটি ডেটা উৎস বা কোয়েরি থেকে ডেটা ম্যাপ করতে, রিপোর্ট টেমপ্লেটে ব্যবহার করা হয়। নামটি রিপোর্টের মূল অংশে পুনরায় ব্যবহার করা হয়েছে এবং কেস-সংবেদনশীল।

`<fieldDescription> ` - এই উপাদানটি XML ফাইলের উপযুক্ত উপাদানের সাথে ক্ষেত্রের নাম ম্যাপ করে।

`<staticText> ` - এটি স্ট্যাটিক টেক্সটকে সংজ্ঞায়িত করে যা কোনো ডেটাসোর্স, ভেরিয়েবল, প্যারামিটার বা রিপোর্ট এক্সপ্রেশনের উপর নির্ভর করে না।

`<band> ` - ব্যান্ডে ডেটা থাকে, যা প্রতিবেদনে প্রদর্শিত হয়।

## তথ্যসূত্র

 * [JRXML - উইকিপিডিয়া](https://en.wikipedia.org/wiki/JasperReports#JRXML)
 * [JRXML উত্স এবং Jasper ফাইলগুলি](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

