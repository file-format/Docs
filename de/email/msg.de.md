{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSG - Microsoft Outlook-E-Mail-Format",
  "description":"Erfahren Sie mehr über das MSG-Dateiformat und APIs, die MSG-Dateien erstellen und öffnen können.",
  "linktitle" : "MSG",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine MSG-Datei?

MSG ist ein Dateiformat, das von [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) und Exchange zum Speichern von E-Mail-Nachrichten verwendet wird , Kontakt, Termin oder andere Aufgaben. Solche Nachrichten können ein oder mehrere E-Mail-Felder mit Absender, Empfänger, Betreff, Datum und Nachrichtentext oder Kontaktinformationen, Terminangaben und eine oder mehrere Aufgabenspezifikationen enthalten. Die Eigenschaften, die das Message-Objekt bilden, einschließlich sind ebenfalls Teil der MSG-Datei. Die MSG-Datei enthält Kopfzeilen, Hauptnachrichtentext und Hyperlinks als reinen ASCII-Text. MSG-Dateien eignen sich auch für Programme, die die Messaging Applications Programming Interface (MAPI) von Microsoft benötigen.

## MSG-Dateistruktur

Das CFB_3-Format ist die Basis der MSG-Datei. Das Paradigma basiert auf den Konzepten von Speichern und Streams, ganz in der Nähe von Verzeichnissen und Dateien. Daher besteht ein Hauptunterschied zu ersterem in der gesamten Hierarchie, die in eine eigene Datei gepackt ist, die als zusammengesetzte Datei bezeichnet wird. Objekte bilden die Nachrichtendateien und bestehen aus einer einzelnen Eigenschaft oder ihren Sammlungen. Diese Fähigkeit erleichtert es Anwendungen, komplizierte, strukturierte Daten in einer einzigen Datei zu speichern. Dieses Format gibt auch mehrere Speicher an, wobei jeder Speicher das Message-Objekt als eine Hauptkomponente darstellt. Diese Speicher enthalten eine Reihe von Strömen, die eine Eigenschaft dieser Komponente darstellen. Auch eine Verschachtelung der Lagerung ist möglich.

## Mapi-Eigenschaften

Auf der obersten Ebene der .msg-Datei enthalten Speicher Streams, die Eigenschaften darin speichern. Eigenschaften können wie folgt kategorisiert werden:

* Eigenschaften mit fester Länge
* Eigenschaften mit variabler Länge
* Mehrwertige Eigenschaften

Unabhängig von der Kategorie ist eine Eigenschaft entweder ein Tag oder ein Name. Für benannte Eigenschaften sind jedoch geeignete Zuordnungsinformationen erforderlich, wie durch ihren Zuordnungsspeicher angegeben.

## Speicher

Speicher bilden die Schlüsselkomponenten des Message-Objekts. Das MSG-Dateiformat gibt die folgenden Speicher an:

## Top-Level-Struktur

Das Nachrichtenobjekt repräsentiert die gesamte oberste Ebene des MSG-Dateiformats. Je nach Typ, Eigenschaften, Anzahl der Empfänger- und Anhangsobjekte kann ein Nachrichtenobjekt unterschiedliche Stromspeicher in seiner entsprechenden .MSG-Datei haben.

### Beziehung zu anderen Strukturen

Das Msg-Dateiformat hat die folgenden Beziehungen zu anderen Strukturen:

* Die Basis von .msg ist das Compound File Binary File Format.
* Die vom Message and Attachment Object Protocol verwendeten Eigenschaften werden von diesem Format verwendet.

## Szenarien zur Vermeidung von MSG-Formaten

Das Nachrichtenobjekt kann von Clients oder Nachrichtenspeichern gemeinsam genutzt werden, die das .msg-Dateisystem verwenden. Es gibt wenige Umstände, unter denen das Speichern eines Message-Objekts im .msg-Dateiformat nicht angemessen wäre. Zum Beispiel:

* Im Falle der Aufrechterhaltung eines großen eigenständigen Archivs ist es besser, ein voll funktionsfähiges Format zu verwenden, in dem Ansichten präziser gerendert werden können.
* Wenn der Empfänger unbekannt ist, ist es möglich, dass das Format von der Empfängerseite nicht unterstützt wird und möglicherweise privat oder irrelevant geliefert wird.

## Beispiel einer MSG-Datei

Um eine Vorstellung davon zu bekommen, wie eine MSG-Datei aussieht, können Sie eine [Beispiel-MSG-Datei](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) herunterladen und auf Ihrem öffnen Computer, um seinen Inhalt anzuzeigen.

## Verweise

* [[MS-OXMSG]: Outlook MSG-Dateiformat](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

