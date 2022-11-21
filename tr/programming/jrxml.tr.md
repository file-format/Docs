{
  "date" : "2019-10-11",
  "keywords" :[ "jrxml", "jrxml dosyası", "jrxml dosya biçimi", "dosya biçimi", "programlama","jrxml dosyası indirme", ".jrxml dosyası", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"JRXML dosya formatı ve JRXML dosyalarını açıp oluşturabilen API'ler hakkında bilgi edinin.",
  "title" :"JRXML Dosya Biçimi",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## JRXML dosyası nedir?

Bir JRXML dosyası, JasperReports tarafından oluşturulur ve popüler [XML](/tr/web/xml/) dosya biçiminde tasarım tanımını içerir. Rapor düzeni, metin alanları, resimler, grafikler, parametreler ve değişkenler gibi tüm tasarım öğelerini saklar. JasperReports, arka uç veritabanlarından ve depolama ortamından veri alarak programlı olarak raporlar oluşturmak için kullanılan bir Java kitaplığıdır.

## JRXML Dosya Biçimi

JRXML dosyaları, XML dosya biçimine göre oluşturulan düz metin dosyalarıdır. JasperReport çerçevesi, farklı türde veri kaynaklarını işleyebilir. Bir .jrxml dosyası derlendiğinde, çıktı olarak .jasper dosyasıyla sonuçlanır. Bir jrxml dosyası bir dizi bölümden oluşur. Bazı bölümler, sayfanın boyutu, alanların konumu ve bantların yüksekliği gibi sayfanın fiziksel özelliklerine ilişkin bilgiler içerirken, bazıları parametrelerin ve değişkenlerin bildirimi ve bir sorgunun tanımı gibi mantıksal özelliklerle ilgilidir. veri seçimi için.

### JRXML dosyası örneği

Basit bir JRXML dosyası örneği aşağıda gösterilmiştir.
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

Aşağıda, örneğin ayrıntıları verilmiştir.

`<queryString> ` − Bu boş (verileri Java Fasulyelerinden geçirdiğimiz için). Genellikle rapor sonucunu alan SQL deyimini içerir.

`<field name> ` − Bu öğe, veri kaynaklarından veya sorgulardan gelen verileri rapor şablonlarına eşlemek için kullanılır. ad, rapor gövdesinde yeniden kullanılır ve büyük/küçük harfe duyarlıdır.

`<fieldDescription> ` − Bu öğe, alan adını XML dosyasındaki uygun öğeyle eşler.

`<staticText> ` − Bu, herhangi bir veri kaynağına, değişkene, parametreye veya rapor ifadesine bağlı olmayan statik metni tanımlar.

`<band> ` − Bantlar, raporda görüntülenen verileri içerir.

## Referanslar

* [JRXML - Wikipedia](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [JRXML Kaynakları ve Jasper Dosyaları](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

