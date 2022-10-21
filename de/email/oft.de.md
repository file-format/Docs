{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFT - Microsoft Outlook-E-Mail-Vorlagendatei",
  "description":"Erfahren Sie mehr über das OFT-Dateiformat und APIs, die OFT-Dateien erstellen und öffnen können.",
  "linktitle" :"OFT",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine OFT-Datei?

Dateien mit der Erweiterung .oft sind Vorlagendateien, die mit Microsoft Outlook erstellt werden. Das vorformatierte Layout-Set für Nachrichtenvorlagen wird dann zum zeitsparenden Versenden von E-Mails mit gemeinsamen Informationen verwendet. Solche Dateien können generiert werden, indem Sie eine neue E-Mail erstellen, die erforderlichen Informationen hinzufügen und dann das Dropdown-Menü „Als Office-Vorlage speichern (.oft)“ von Microsoft Outlook verwenden. Benutzer können die OFT-Dateien öffnen, indem sie darauf doppelklicken, und sie werden in der zugehörigen Anwendung auf diesem bestimmten System geöffnet.

## OFT-Dateistruktur ##

Das .OFT-Dateiformat verwendet an seiner Basis das [MSG](/de/email/msg/)-Dateiformat. Der einzige Unterschied besteht darin, dass OFT-Dateien CLSID_TemplateMessage ({0006F046-0000-0000-C000-000000000046}) als Speicherklasse (WriteClassStg) haben, während MSG-Dateien CLSID_MailMessage ({00020D0B-0000-0000-C000-000000000046}) verwenden.

Das CFB_3-Format ist die Basis der MSG-Datei. Das Paradigma basiert auf den Konzepten von Speichern und Streams, ganz in der Nähe von Verzeichnissen und Dateien. Daher besteht ein Hauptunterschied zu ersterem in der gesamten Hierarchie, die in eine eigene Datei gepackt ist, die als zusammengesetzte Datei bezeichnet wird. Objekte bilden die Nachrichtendateien und bestehen aus einer einzelnen Eigenschaft oder ihren Sammlungen. Diese Fähigkeit erleichtert es Anwendungen, komplizierte, strukturierte Daten in einer einzigen Datei zu speichern. Dieses Format gibt auch mehrere Speicher an, wobei jeder Speicher das Message-Objekt als eine Hauptkomponente darstellt. Diese Speicher enthalten eine Reihe von Strömen, die eine Eigenschaft dieser Komponente darstellen. Auch eine Verschachtelung der Lagerung ist möglich.

### OFT-Eigenschaften

Auf der obersten Ebene der .msg-Datei enthalten Speicher Streams, die Eigenschaften darin speichern. Eigenschaften können wie folgt kategorisiert werden:

* Eigenschaften mit fester Länge
* Eigenschaften mit variabler Länge
* Mehrwertige Eigenschaften

Unabhängig von der Kategorie ist eine Eigenschaft entweder ein Tag oder ein Name. Für benannte Eigenschaften sind jedoch geeignete Zuordnungsinformationen erforderlich, wie durch ihren Zuordnungsspeicher angegeben.

### OFT-Speicher

Speicher bilden die Schlüsselkomponenten des Message-Objekts. Das MSG-Dateiformat gibt die folgenden Speicher an:

### Top-Level-Struktur

Das Message-Objekt repräsentiert die gesamte oberste Ebene des Msg-Dateiformats. Je nach Typ, Eigenschaften, Anzahl der Empfänger- und Anhangsobjekte kann ein Nachrichtenobjekt unterschiedliche Stromspeicher in seiner entsprechenden .MSG-Datei haben.

#### Beziehung zu anderen Strukturen

Das MSG/OFT-Dateiformat hat folgende Beziehungen zu anderen Strukturen:

* Die Basis von .msg ist das Compound File Binary File Format.
* Die vom Message and Attachment Object Protocol verwendeten Eigenschaften werden von diesem Format verwendet.

## Verweise

* [[MS-OXMSG]: Outlook MSG-Dateiformat](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

