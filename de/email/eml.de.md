{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EML - E-Mail-Nachricht",
  "description":"Erfahren Sie mehr über das EML-Dateiformat und APIs, die EML-Dateien erstellen und öffnen können.",
  "linktitle" :"EML",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-16"
}

## Was ist eine EML-Datei?

Das EML-Dateiformat stellt E-Mail-Nachrichten dar, die mit Outlook und anderen relevanten Anwendungen gespeichert wurden. Fast alle E-Mail-Clients unterstützen dieses Dateiformat aufgrund seiner Konformität mit dem RFC-822 Internet Message Format Standard. Microsoft Outlook ist die Standardsoftware zum Öffnen von EML-Nachrichtentypen. EML-Dateien können zum Speichern auf Disc sowie zum Versenden an Empfänger mithilfe von Kommunikationsprotokollen verwendet werden.

## Kurze Geschichte der EML

EML-Dateiformatspezifikationen sind gemäß [RFC 822](http://www.ietf.org/rfc/rfc0822.txt) Standardformat verfügbar. Vor RFC-822 regelte RFC-733 die Regeln für den Austausch von Netzwerknachrichten, bis ersteres 1982 als Verbesserung von Lateral durch die Einrichtung von ARPA-Standards geschaffen wurde. Gleichzeitig hat Microsoft seine eigenen COM-Module für die Entwicklung seines eigenen E-Mail-Clients, dh Outlook Express, erstellt. RFC-822 ging den Weg, sich als proprietäres Format zu etablieren, als Microsoft vom offenen Standard abwich und das Dateiformat [PST](/de/email/pst/) erstellte, in dem E-Mails in einem hochstrukturierten Datenbankformat gespeichert werden. Dies führte zu Problemen für Benutzer von Nicht-Microsoft-E-Mail-Clients, wenn E-Mails von Microsoft Outlook weitergeleitet wurden.

Im Jahr 2001 wurde der 822-Standard auf 2822 - Internet Message Format erweitert, das derzeit zum Erstellen, Lesen und Senden von EML-Nachrichten im MIME RFC-822-Format verwendet wird.

## EML-Dateiformatspezifikationen

EML-Dateien bestehen aus zwei unterschiedlichen Abschnitten:

* Kopfzeilen - Enthält Informationen über die Nachrichtenkopfzeile
* Nachrichtentext – Enthält eine Reihe von Informationen, die Nachrichteninhalte, eingebettete Bilder und Anhänge enthalten können

### Header-Informationen ###

Eine EML-Datei besteht aus Header-Informationen und optional dem Nachrichtentext. Jede Kopfzeile in der EML besteht aus zwei Teilen, die durch einen Doppelpunkt ":" getrennt sind. Der erste heißt Header Name und der nach dem Doppelpunkt ist Header Body. Zu solchen Headern gehören beispielsweise:

* E-Mail-Adresse des Absenders
* Empfänger E-Mail-Adresse
* Betreff der E-Mail
* Zeit- und Datumsstempel der Nachricht

**Beispielkopfzeile**

Aus:<John@bmw.eml.light.com>

Zu:<Andy@fileformat.com>

Datum: Do, 8. März 2018 10:43:37 +0100

Betreff: BMW Eml Licht

### Nachrichtentext ###

Der EML-Nachrichtentext enthält die primären Informationen der E-Mail in Form von Text, Hyperlinks und Anhängen. Der E-Mail-Text kann einfach lesbaren Text enthalten, dies ist jedoch nicht erforderlich. In diesem Fall kann der Nachrichtentext leer sein oder verschlüsselte Anhangsdaten enthalten.

Der Inhalt des Nachrichtenhauptteils wird durch seinen Inhaltstyp beschrieben, der es den lesenden Anwendungen ermöglicht, die Informationen in den jeweiligen Formaten zu lesen. Es repräsentiert tatsächlich die Art und das Format eines Dokuments. Die Struktur eines MIME-Typs oder Inhaltstyps ist sehr einfach; er besteht aus einem Typ und einem Subtyp, zwei Strings, getrennt durch ein '/'. Leerzeichen sind nicht erlaubt. Der "Typ" stellt die Kategorie dar und kann ein diskreter oder ein mehrteiliger Typ sein. Der "Untertyp" ist für jeden Typ spezifisch. Die Liste der Typen, die in die Kategorie der Inhaltstypen fallen, ist lang, aber einige wichtige Inhaltstypen sind wie folgt:


|**Typ**|**Beschreibung**|**Beispiel für Untertypen**
---|---|---|
|text|Stellt ein für Menschen lesbares Format dar|text/plain, text/html, text/css, text/javascript
|image|Stellt Bilder jeglicher Art dar, ausgenommen Videos|image/bmp, image/png, image/jpg, image/gif
|audio|Repräsentiert ein beliebiges Audiodateiformat|audio/mdi, audio/wav
|application|repräsentiert jede Art von binären Daten|application/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### Darstellung des Anhangs im EML-Body ###

Der EML-Hauptteil enthält Grenzen für jeden darin enthaltenen Inhaltstyp. Der Anhang im Nachrichtentext wird durch seinen Inhaltstyp und seine Inhaltsdisposition identifiziert, wie im folgenden Beispiel gezeigt:

Inhaltstyp: Text/Plain; charset#"windows-1252"; name#"apple app store.txt"
Inhaltsdisposition: Anhang; Dateiname#"Apple App Store.txt"
Inhaltsübertragungscodierung: base64
X-Attachment-ID: f_jkhztmd02

Wie zu sehen ist, ermöglicht die auf Anhang gesetzte Inhaltsdisposition den lesenden Anwendungen, Anhangsinformationen zu erhalten, wie z. B. Dateinamen des Anhangs und die Übertragungscodierung. Auf Anhang-Header-Informationen folgen verschlüsselte Anhang-Inhalte, die gelesen werden sollen.

#### Beispiel einer Tabelle als Anhang ####

Inhaltstyp: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; name#"english_spodr.xlsx"
Inhaltsdisposition: Anhang; Dateiname#"english_spodr.xlsx"
Inhaltsübertragungscodierung: base64
X-Attachment-ID: f_jkhztmd43

## Verweise

* [RFC 822](http://www.ietf.org/rfc/rfc0822.txt)

