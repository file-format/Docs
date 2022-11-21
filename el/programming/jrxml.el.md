{
  "date" : "2019-10-11",
  "keywords" :[ "jrxml", "αρχείο jrxml", "μορφή αρχείου jrxml", "μορφή αρχείου", "προγραμματισμός", "λήψη αρχείου jrxml", "αρχείο .jrxml", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Μάθετε σχετικά με τη μορφή αρχείου JRXML και τα API που μπορούν να ανοίξουν και να δημιουργήσουν αρχεία JRXML.",
  "title" :"Μορφή αρχείου JRXML",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο JRXML;

Ένα αρχείο JRXML δημιουργείται από το JasperReports και περιέχει ορισμό σχεδίασης σε δημοφιλή μορφή αρχείου [XML](/el/web/xml/). Αποθηκεύει όλα τα στοιχεία σχεδίασης, όπως διάταξη αναφοράς, πεδία κειμένου, εικόνες, γραφήματα, παραμέτρους και μεταβλητές. Το JasperReports είναι μια βιβλιοθήκη Java που χρησιμοποιείται για τη δημιουργία αναφορών μέσω προγραμματισμού με την ανάκτηση δεδομένων από βάσεις δεδομένων υποστήριξης και μέσα αποθήκευσης.

## Μορφή αρχείου JRXML

Τα αρχεία JRXML είναι αρχεία απλού κειμένου που δημιουργούνται με βάση τη μορφή αρχείου XML. Το πλαίσιο JasperReport μπορεί να χειριστεί διαφορετικά είδη πηγών δεδομένων. Όταν μεταγλωττίζεται ένα αρχείο .jrxml, έχει ως αποτέλεσμα το αρχείο .jasper ως έξοδο. Ένα αρχείο jrxml αποτελείται από ένα σύνολο ενοτήτων. Ορισμένες ενότητες περιέχουν πληροφορίες που σχετίζονται με τα φυσικά χαρακτηριστικά της σελίδας, όπως η διάσταση της σελίδας, η θέση των πεδίων και το ύψος των ζωνών, ενώ ορισμένες αφορούν τα λογικά χαρακτηριστικά, όπως η δήλωση των παραμέτρων και των μεταβλητών και ο ορισμός ενός ερωτήματος για επιλογή δεδομένων.

### Παράδειγμα αρχείου JRXML

Ένα απλό παράδειγμα αρχείου JRXML φαίνεται παρακάτω.
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

Ακολουθούν οι λεπτομέρειες του παραδείγματος.

`<queryString> ` − Αυτό είναι κενό (καθώς περνάμε δεδομένα μέσω Java Beans). Συνήθως περιέχει τη δήλωση SQL, η οποία ανακτά το αποτέλεσμα της αναφοράς.

`<field name> ` − Αυτό το στοιχείο χρησιμοποιείται για την αντιστοίχιση δεδομένων από πηγές δεδομένων ή ερωτήματα, σε πρότυπα αναφορών. Το όνομα χρησιμοποιείται ξανά στο σώμα της αναφοράς και γίνεται διάκριση πεζών-κεφαλαίων.

`<fieldDescription> ` − Αυτό το στοιχείο αντιστοιχίζει το όνομα του πεδίου με το κατάλληλο στοιχείο στο αρχείο XML.

`<staticText> ` − Αυτό ορίζει το στατικό κείμενο που δεν εξαρτάται από πηγές δεδομένων, μεταβλητές, παραμέτρους ή εκφράσεις αναφοράς.

`<band> ` − Οι ζώνες περιέχουν τα δεδομένα, τα οποία εμφανίζονται στην αναφορά.

## βιβλιογραφικές αναφορές

* [JRXML - Wikipedia](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [Πηγές JRXML και αρχεία Jasper](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

