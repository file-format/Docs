{
  "date" : "2019-10-11",
  "keywords" :[ "jrxml", "ไฟล์ jrxml", "รูปแบบไฟล์ jrxml", "รูปแบบไฟล์", "การเขียนโปรแกรม", "ดาวน์โหลดไฟล์ jrxml", "ไฟล์ .jrxml", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ JRXML และ API ที่สามารถเปิดและสร้างไฟล์ JRXML",
  "title" :"รูปแบบไฟล์ JRXML",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ JRXML คืออะไร??

ไฟล์ JRXML สร้างขึ้นโดย JasperReports และมีข้อกำหนดการออกแบบในรูปแบบไฟล์ [XML](/th/web/xml/) ยอดนิยม โดยจะจัดเก็บองค์ประกอบการออกแบบทั้งหมด เช่น เค้าโครงรายงาน ฟิลด์ข้อความ รูปภาพ แผนภูมิ พารามิเตอร์ และตัวแปร JasperReports เป็นไลบรารี Java ที่ใช้สำหรับสร้างรายงานทางโปรแกรมโดยการดึงข้อมูลจากฐานข้อมูลแบ็กเอนด์และสื่อจัดเก็บข้อมูล

## รูปแบบไฟล์ JRXML

ไฟล์ JRXML เป็นไฟล์ข้อความธรรมดาที่สร้างขึ้นตามรูปแบบไฟล์ XML กรอบ JasperReport สามารถจัดการแหล่งข้อมูลประเภทต่างๆ เมื่อคอมไพล์ไฟล์ .jrxml จะได้ผลลัพธ์เป็นไฟล์ .jasper ไฟล์ jrxml ประกอบด้วยชุดของส่วนต่างๆ บางส่วนประกอบด้วยข้อมูลที่เกี่ยวข้องกับลักษณะทางกายภาพของหน้า เช่น มิติของหน้า การวางตำแหน่งของฟิลด์ และความสูงของแถบ ขณะที่บางส่วนเกี่ยวข้องกับลักษณะเชิงตรรกะ เช่น การประกาศพารามิเตอร์และตัวแปร และคำจำกัดความของคิวรี สำหรับการเลือกข้อมูล

### ตัวอย่างไฟล์ JRXML

ตัวอย่างไฟล์ JRXML อย่างง่ายแสดงไว้ด้านล่าง
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
  <title>,
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

ต่อไปนี้เป็นรายละเอียดของตัวอย่าง

`<queryString> ` − ว่างเปล่า (เนื่องจากเรากำลังส่งข้อมูลผ่าน Java Beans) มักจะมีคำสั่ง SQL ซึ่งดึงผลลัพธ์ของรายงาน

`<field name> ` − องค์ประกอบนี้ใช้เพื่อแมปข้อมูลจากแหล่งข้อมูลหรือการสืบค้นไปยังเทมเพลตรายงาน ชื่อถูกนำมาใช้ซ้ำในเนื้อหาของรายงานและคำนึงถึงขนาดตัวพิมพ์

`<fieldDescription> ` − องค์ประกอบนี้จะจับคู่ชื่อฟิลด์กับองค์ประกอบที่เหมาะสมในไฟล์ XML

`<staticText> ` − กำหนดข้อความคงที่ที่ไม่ขึ้นกับแหล่งข้อมูล ตัวแปร พารามิเตอร์ หรือนิพจน์รายงาน

`<band> ` − แถบประกอบด้วยข้อมูล ซึ่งจะแสดงในรายงาน

## อ้างอิง

* [JRXML - วิกิพีเดีย](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [แหล่งที่มาของ JRXML และไฟล์ Jasper](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

