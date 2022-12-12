{
  "date" : "2019-10-11",
  "keywords" :[ "jrxml", "jrxml file", "jrxml file format", "file format", "programming","jrxml file download", ".jrxml file", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp JRXML và API có thể mở và tạo tệp JRXML.",
  "title" :"Định dạng tệp JRXML",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp JRXML là gì?

Tệp JRXML được tạo bởi JasperReports và chứa định nghĩa thiết kế ở định dạng tệp [XML](/vi/web/xml/) phổ biến. Nó lưu trữ tất cả các yếu tố thiết kế như bố cục báo cáo, trường văn bản, hình ảnh, biểu đồ, tham số và biến. JasperReports là một thư viện Java được sử dụng để tạo báo cáo theo chương trình bằng cách truy xuất dữ liệu từ cơ sở dữ liệu phụ trợ và phương tiện lưu trữ.

## Định dạng tệp JRXML

Các tệp JRXML là các tệp văn bản thuần túy được tạo dựa trên định dạng tệp XML. Khung JasperReport có thể xử lý các loại nguồn dữ liệu khác nhau. Khi một tệp .jrxml được biên dịch, nó sẽ tạo ra tệp .jasper dưới dạng đầu ra. Tệp jrxml bao gồm một tập hợp các phần. Một số phần chứa thông tin liên quan đến các đặc điểm vật lý của trang chẳng hạn như kích thước của trang, vị trí của các trường và chiều cao của các dải, trong khi một số liên quan đến các đặc điểm logic như khai báo các tham số và biến và định nghĩa của một truy vấn cho việc lựa chọn dữ liệu.

### Ví dụ về tệp JRXML

Một ví dụ về tệp JRXML đơn giản được hiển thị bên dưới.
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

Sau đây là chi tiết của ví dụ.

`<queryString> ` − Cái này trống (vì chúng ta đang chuyển dữ liệu qua Java Beans). Thường chứa câu lệnh SQL, truy xuất kết quả báo cáo.

`<field name> ` − Phần tử này được sử dụng để ánh xạ dữ liệu từ các nguồn dữ liệu hoặc truy vấn vào các mẫu báo cáo. tên được sử dụng lại trong nội dung báo cáo và phân biệt chữ hoa chữ thường.

`<fieldDescription> ` − Phần tử này ánh xạ tên trường với phần tử thích hợp trong tệp XML.

`<staticText> ` − Điều này xác định văn bản tĩnh không phụ thuộc vào bất kỳ nguồn dữ liệu, biến, tham số hoặc biểu thức báo cáo nào.

`<band> ` − Các dải chứa dữ liệu, được hiển thị trong báo cáo.

## Người giới thiệu

* [JRXML - Wikipedia](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [Nguồn JRXML và tệp Jasper](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

