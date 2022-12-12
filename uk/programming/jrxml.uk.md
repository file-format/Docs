{
  "date" : "2019-10-11",
  "keywords" :[ "jrxml", "файл jrxml", "формат файлу jrxml", "формат файлу", "програмування", "завантаження файлу jrxml", "файл .jrxml", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Дізнайтеся про формат файлу JRXML та API, які можуть відкривати та створювати файли JRXML.",
  "title" :"Формат файлу JRXML",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл JRXML?

Файл JRXML створюється JasperReports і містить визначення дизайну в популярному форматі [XML](/uk/web/xml/). Він зберігає всі елементи дизайну, такі як макет звіту, текстові поля, зображення, діаграми, параметри та змінні. JasperReports — це бібліотека Java, яка використовується для програмного створення звітів шляхом отримання даних із внутрішніх баз даних і носіїв даних.

## Формат файлу JRXML

Файли JRXML — це звичайні текстові файли, створені на основі формату XML. Фреймворк JasperReport може працювати з різними типами джерел даних. Під час компіляції файлу .jrxml він виводить файл .jasper. Файл jrxml складається з набору розділів. Деякі розділи містять інформацію, пов’язану з фізичними характеристиками сторінки, такими як розміри сторінки, розташування полів і висота смуг, а деякі стосуються логічних характеристик, таких як оголошення параметрів і змінних і визначення запиту. для вибору даних.

### Приклад файлу JRXML

Нижче наведено простий приклад файлу JRXML.
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

Нижче наведено деталі прикладу.

`<queryString> ` − Це пусте (оскільки ми передаємо дані через Java Beans). Зазвичай містить оператор SQL, який отримує результат звіту.

`<field name> ` − Цей елемент використовується для відображення даних із джерел даних або запитів у шаблони звітів. Ім'я повторно використовується в тілі звіту та чутливе до регістру.

`<fieldDescription> ` − Цей елемент зіставляє назву поля з відповідним елементом у файлі XML.

`<staticText> ` − Це визначає статичний текст, який не залежить від жодних джерел даних, змінних, параметрів або виразів звіту.

`<band> ` − Смуги містять дані, які відображаються у звіті.

## Список літератури

* [JRXML - Вікіпедія](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [Джерельні коди JRXML і файли Jasper](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

