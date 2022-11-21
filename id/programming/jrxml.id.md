{
  "date" : "2019-10-11",
  "keywords" :[ "jrxml", "file jrxml", "format file jrxml", "format file", "pemrograman", "unduhan file jrxml", "file .jrxml", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file JRXML dan API yang dapat membuka dan membuat file JRXML.",
  "title" :"Format File JRXML",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file JRXML?

File JRXML dibuat oleh JasperReports dan berisi definisi desain dalam format file [XML](/id/web/xml/) populer. Ini menyimpan semua elemen desain seperti tata letak laporan, bidang teks, gambar, bagan, parameter, dan variabel. JasperReports adalah pustaka Java yang digunakan untuk membuat laporan secara terprogram dengan mengambil data dari database backend dan media penyimpanan.

## Format File JRXML

File JRXML adalah file teks biasa yang dibuat berdasarkan format file XML. Framework JasperReport dapat menangani berbagai jenis sumber data. Ketika file .jrxml dikompilasi, hasilnya adalah file .jasper sebagai output. File jrxml terdiri dari sekumpulan bagian. Beberapa bagian berisi informasi yang berkaitan dengan karakteristik fisik halaman seperti dimensi halaman, posisi bidang, dan tinggi pita, sementara beberapa lainnya membahas karakteristik logis seperti deklarasi parameter dan variabel serta definisi kueri. untuk pemilihan data.

### Contoh file JRXML

Contoh file JRXML sederhana ditunjukkan di bawah ini.
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

Berikut detail contohnya.

`<queryString> ` − Ini kosong (karena kami mengirimkan data melalui Java Beans). Biasanya berisi pernyataan SQL, yang mengambil hasil laporan.

`<field name> ` − Elemen ini digunakan untuk memetakan data dari sumber data atau query, ke dalam template laporan. name digunakan kembali di badan laporan dan peka huruf besar-kecil.

`<fieldDescription> ` − Elemen ini memetakan nama bidang dengan elemen yang sesuai dalam file XML.

`<staticText> ` − Ini mendefinisikan teks statis yang tidak bergantung pada sumber data, variabel, parameter, atau ekspresi laporan apa pun.

`<band> ` − Band berisi data, yang ditampilkan dalam laporan.

## Referensi

* [JRXML - Wikipedia](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [Sumber JRXML dan File Jasper](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

