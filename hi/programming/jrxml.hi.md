{
  "date" : "2019-10-11",
  "keywords" :["jrxml", "jrxml फ़ाइल", "jrxml फ़ाइल स्वरूप", "फ़ाइल स्वरूप", "प्रोग्रामिंग", "jrxml फ़ाइल डाउनलोड", ".jrxml फ़ाइल", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"JRXML फ़ाइल स्वरूप और API के बारे में जानें जो JRXML फ़ाइलें खोल और बना सकते हैं।",
  "title" :"JRXML फ़ाइल स्वरूप",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## जेआरएक्सएमएल फाइल क्या है?

एक JRXML फ़ाइल JasperReports द्वारा बनाई गई है और इसमें लोकप्रिय [XML](/hi/web/xml/) फ़ाइल स्वरूप में डिज़ाइन परिभाषा शामिल है। यह सभी डिज़ाइन तत्वों जैसे रिपोर्ट लेआउट, टेक्स्ट फ़ील्ड, चित्र, चार्ट, पैरामीटर और चर को संग्रहीत करता है। JasperReports एक जावा लाइब्रेरी है जिसका उपयोग बैकएंड डेटाबेस और स्टोरेज मीडिया से डेटा प्राप्त करके प्रोग्रामेटिक रूप से रिपोर्ट बनाने के लिए किया जाता है।

## जेआरएक्सएमएल फ़ाइल प्रारूप

JRXML फ़ाइलें सादा पाठ फ़ाइलें हैं जो XML फ़ाइल स्वरूप के आधार पर बनाई गई हैं। JasperReport फ्रेमवर्क विभिन्न प्रकार के डेटा स्रोतों को संभाल सकता है। जब एक .jrxml फ़ाइल संकलित की जाती है, तो इसका परिणाम .jasper फ़ाइल आउटपुट के रूप में होता है। एक jrxml फ़ाइल में अनुभागों का एक सेट होता है। कुछ खंडों में पृष्ठ की भौतिक विशेषताओं से संबंधित जानकारी होती है जैसे कि पृष्ठ का आयाम, फ़ील्ड की स्थिति और बैंड की ऊंचाई, जबकि कुछ तार्किक विशेषताओं जैसे मापदंडों और चर की घोषणा और क्वेरी की परिभाषा से संबंधित होते हैं। डेटा चयन के लिए।

### JRXML फ़ाइल उदाहरण

एक साधारण JRXML फ़ाइल उदाहरण नीचे दिखाया गया है।
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

निम्नलिखित उदाहरण के विवरण हैं।

`<queryString> ` - यह खाली है (जैसा कि हम जावा बीन्स के माध्यम से डेटा पास कर रहे हैं)। आमतौर पर SQL स्टेटमेंट होता है, जो रिपोर्ट के परिणाम को पुनः प्राप्त करता है।

`<field name> ` - इस तत्व का उपयोग डेटा स्रोतों या प्रश्नों से डेटा को रिपोर्ट टेम्प्लेट में मैप करने के लिए किया जाता है। रिपोर्ट बॉडी में नाम का पुन: उपयोग किया जाता है और केस-संवेदी होता है।

`<fieldDescription> ` - यह तत्व फ़ील्ड नाम को XML फ़ाइल में उपयुक्त तत्व के साथ मैप करता है।

`<staticText> ` - यह स्थैतिक पाठ को परिभाषित करता है जो किसी भी डेटा स्रोत, चर, पैरामीटर या रिपोर्ट अभिव्यक्ति पर निर्भर नहीं करता है।

`<band> ` - बैंड में डेटा होता है, जो रिपोर्ट में प्रदर्शित होता है।

## संदर्भ

* [जेआरएक्सएमएल - विकिपीडिया](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [जेआरएक्सएमएल स्रोत और जैस्पर फ़ाइलें](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

