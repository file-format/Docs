{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TNEF",
  "description":"Erfahren Sie mehr über das TNEF-Dateiformat und APIs, die TNEF-Dateien erstellen und öffnen können.",
  "linktitle" : "TNEF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine TNEF-Datei?

Transport Neutral Encapsulation Format (TNEF) ist ein Microsoft-eigenes Format zum Verkapseln von E-Mail-Anhängen auf der Grundlage von Messaging Application Programming Interface (**MAPI**). Microsoft Outlook und Microsoft Exchange Server unterstützen TNEF vollständig, während TNEF später in MAPI dekodiert und die formatierten E-Mails angezeigt werden. Ein E-Mail-Anhang mit TNEF-Codierung hat den MIME-Typ MS-TNEF und wird als winmail/win.dat gespeichert. Der Anhang in winmail .dat kapselt die folgenden Informationen:


|Nachricht|OLE-Objekte|Outlook-Features
---|---|---|
|<ul><li> Ursprüngliche Nachrichtenanhänge</li><li> Original formatierte Version</li><li> Schriftarten, Textgrößen und Textfarben</li></ul> |<ul><li> eingebettete Bilder</li><li> eingebettete Office-Dokumente</li></ul> |<ul><li> benutzerdefinierte Formulare</li><li> Abstimmungsknöpfe</li><li> Anfragen erfüllen</li></ul>


Andere E-Mail-Dienste, die TNEF nicht unterstützen, präsentieren Klartext für TNEF-formatierte Nachrichten. Outlook bettet ein Rich-Format der Nachricht in TNEF-Dateien (OLE) oder bestimmte Outlook-Features (Formulare, Umfrageschaltflächen und Konferenzanfragen) ein. Eine explizite TNEF-Kodierung innerhalb des Outlook-E-Mail-Clients zu sanktionieren ist nicht möglich, jedoch erleichtert die Wahl des RTF-Formats für den Versand einer E-Mail implizit die TNEF-Kodierung.

## TNEF-Dateiformat

Der TNEF-Datenalgorithmus erstellt eine abgeflachte Struktur aus reichhaltigen hierarchischen Nachrichteneigenschaften. Diese abgeflachten Strukturen werden dann verwendet, um einen seriellen Datenstrom darzustellen, der aus bestimmten Eigenschaften besteht.

In einigen Situationen, in denen Eigenschaften in Gruppen auftreten oder mehrere Werte haben, kann der Stream Zählwerte und Auffüllungen enthalten, um eine bestimmte Datenausrichtung zu erzwingen. Eine besondere Situation, in der die Verwendung dieses Algorithmus vorteilhaft ist, ist in einer nicht unterstützenden Messaging-Umgebung. In solchen Umgebungen wird eine reichhaltige Nachrichteneigenschaft von einem TNEF-Writer in einen seriellen Datenstrom codiert. Außerdem können die Eigenschaften, die nicht zum zugrunde liegenden TNEF gehören, während der Übertragung eingekapselt werden. Diese eingekapselten Eigenschaften werden dann durch Dekodierung über einen TNEF verfügbar gemacht, um die Verfügbarkeit aller Eigenschaften der ursprünglichen Nachricht für die Client-Anwendung sicherzustellen.

In TNEF sind alle numerischen Datentypen Little-Endian und ihre Größe ist größer als ein Byte. Die Handhabung dieser numerischen Werte auf Nicht-Little-Endian-Plattformen erfordert die Durchführung der entsprechenden Transformationen, um korrekte Werte zu erhalten. String-Werte werden im ABNF-Format (Augmented Backus-Naur Form) gemäß den [RFC5234]-Spezifikationen dargestellt. Wenn die Zeichenfolge mit einem Nullzeichen endet, wird sie ebenfalls eingeschlossen; zum Beispiel `"worker@specimen.com" %x00`.

{{< figure src="../TNEF.png" alt="TNEF-Dateiformat" >}}

## TNEF-Attribute und Verarbeitungsregeln ##

Der Datenstrom in TNEF beginnt mit einer Legacy-Versionsnummer, einer Signatur, einem primitiven Schlüsselwert und einem Attribut, das die Codepage darstellt. Diese Codepage wird generiert, wenn der Encoder ANSI-Attribute und -Eigenschaften aufzeichnet. Danach wurde der Stream zu einer Reihe von Attributen, in denen Nachrichtenattribute zuerst aneinandergereiht wurden und dann von Anhangsattributen gefolgt wurden. Unterschiedliche Eigenschaften von Nachrichten und Anhängen sind in speziellen Attributen wie attMsgProps, attAttachment und attRecipTable enthalten. Die Attribute, die im TNEF-Stream erscheinen, enthalten die Struktur, Nachrichteneigenschaften und Konvertierungen, die erforderlich sind, um sie mit Nachrichteneigenschaften zu verknüpfen. Jedes Attribut besteht aus einer ID, Größe und Daten des Attributs, einer Prüfsumme und einer Ebene entsprechend seiner Anwendung.

## Beziehung zu Protokollen und anderen Algorithmen ##

Die Systeme, die einen schlechten Mechanismus haben, um das reichhaltige Nachrichtenformat nativ anzuzeigen, benötigen den TNEF-Datenalgorithmus für den Transport. Unter Verwendung des Medientyps ms-TNEF besteht die Ausgabe des Algorithmus aus einer Anhangsdatei (winmail.dat) und einem Hauptteil des in [RFC2045] spezifizierten MIME. Der Klartext-Nachrichtentext wird unter Verwendung von UUENCODE gemäß der [MSDN-UAF]-Spezifikation übertragen und dieser Nachrichtentext oder ein gleichwertiges Verfahren auf der Empfängerseite dekodiert. Darüber hinaus kann TNEF Nachrichtendaten über verschiedene Internetprotokolle wie SMTP, POP3, IMAP4 und diejenigen übertragen, die MIME gemäß dem RFC2045-Standard integrieren.

## Erklärung zur Anwendbarkeit ##

Zusätzlich zur einfachen Nachrichtenübertragung sollte die ursprüngliche Anwendung von TNEF erstellt werden, um Nachrichtenklassen zu verwenden und zusätzliche Funktionen zu unterstützen, die keine ursprüngliche Unterstützung im Transportprotokoll haben. Diese Anwendung wurde für die Übertragung umfangreicher Nachrichteneigenschaften und benannter Eigenschaften, die moderne Messaging-Clients heutzutage verwenden, weiter verfeinert. Zur Übereinstimmung mit der ursprünglichen Implementierung wird die ursprüngliche Attributsyntax beibehalten und ein spezielles Attribut hält die neuen Nachrichteneigenschaften separat.

## Verweise

* [Transportneutrales Kapselungsformat](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)
* [E-Mail-Adressen und Adressbücher in Exchange Server](https://learn.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# Exchangeserver-2019)
* [[MS-OXTNEF]: TNEF-Datenalgorithmus (Transport Neutral Encapsulation Format)](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)

