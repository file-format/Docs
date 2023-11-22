{
"Datum": "08.06.2023",
  "keywords": [
"crx-Datei",
"Was ist eine CRX-Datei",
"Wie installiere ich eine CRX-Datei in Google Chrome",
"Wie öffnet man eine CRX-Datei",
"Was enthält die CRX-Datei",
"Was ist das Format der CRX-Datei?",
"Datei",
"crx-Dateierweiterung",
"Verlängerung"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "CRX-Dateiformat – Google Chrome-Erweiterung",
  "description":"Erfahren Sie mehr über das CRX-Format und die APIs, mit denen CRX-Dateien erstellt und geöffnet werden können.",
"linktitle": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx",
"parent": "misc"
}
},
"lastmod": "08.06.2023"
}

## Was ist eine CRX-Datei?

Das CRX-Dateiformat ist mit den Browsererweiterungen von Google Chrome verknüpft. Eine CRX-Datei ist im Wesentlichen ein komprimiertes Paket, das die notwendigen Dateien und Metadaten für die Installation und Ausführung einer Erweiterung in Google Chrome enthält. Es verbessert die Funktionalität oder das Erscheinungsbild eines Webbrowsers, indem es eine zusätzliche Funktion oder ein zusätzliches Thema bereitstellt.

Wenn eine CRX-Datei heruntergeladen und in Google Chrome installiert wird, überprüft der Browser die Integrität der Erweiterung mithilfe eines öffentlichen Schlüssels und einer Signatur. Wenn die Überprüfung erfolgreich ist, extrahiert Chrome den Inhalt der CRX-Datei, installiert die Erweiterung und macht sie zur Verwendung verfügbar. Benutzer können ihre Erweiterungen über die Chrome-Erweiterungsseite verwalten, auf der installierte Erweiterungen aktiviert, deaktiviert oder entfernt werden können.

## Wie installiere ich eine CRX-Datei in Google Chrome?

Um eine CRX-Datei in Google Chrome zu installieren, können Sie die folgenden Schritte ausführen:

1. Öffnen Sie den Chrome-Browser.
2. Geben Sie "chrome://extensions" in die Adressleiste ein und drücken Sie die Eingabetaste.
3. Aktivieren Sie den Kippschalter "Entwicklermodus" in der oberen rechten Ecke der Seite "Erweiterungen".
4. Klicken Sie auf die Schaltfläche "Unverpackt laden".
5. Suchen Sie den Ordner mit den extrahierten Inhalten der CRX-Datei und wählen Sie ihn aus (oder wählen Sie einfach die CRX-Datei selbst aus).
6. Klicken Sie auf "Öffnen", um die Erweiterung zu installieren.

## Was enthält die CRX-Datei?

Eine CRX-Datei enthält die notwendigen Dateien und Metadaten, die für die Google Chrome-Erweiterung erforderlich sind. Hier ist eine Aufschlüsselung typischer Inhalte einer CRX-Datei:

- **Manifestdatei (manifest.json):** Bei dieser Datei handelt es sich um eine JSON-formatierte Datei, die Informationen zur Erweiterung wie Name, Version, Beschreibung, Berechtigungen und Hintergrundskripts enthält. Es definiert die Struktur und das Verhalten der Erweiterung.
- **JavaScript-Dateien:** Diese Dateien enthalten den Code, der die Funktionalität der Erweiterung definiert. Sie können Skripte zum Behandeln von Ereignissen, zum Ändern von Webseiten oder zur Interaktion mit den APIs von Chrome umfassen.
- **HTML-, CSS- und Bilddateien:** Erweiterungen umfassen häufig Elemente der Benutzeroberfläche, wie z. B. Popup-Fenster oder Optionsseiten. HTML-Dateien definieren die Struktur dieser Schnittstellen, während CSS-Dateien ihr Erscheinungsbild steuern. Bilddateien werden für Symbole oder andere grafische Elemente verwendet.
- **Optionale Ressourcendateien:** Erweiterungen können zusätzliche Ressourcen enthalten, z. B. Lokalisierungsdateien zur Unterstützung mehrerer Sprachen. Diese Dateien enthalten Übersetzungen von Texten, die in der Benutzeroberfläche der Erweiterung verwendet werden.
- **Hintergrundskripts:** Wenn eine Erweiterung über Hintergrundprozesse oder Skripts verfügt, die unabhängig von der aktiven Webseite ausgeführt werden, werden diese Skripts in die CRX-Datei aufgenommen.
- **Inhaltsskripte:** Inhaltsskripte sind Skripte, die in Webseiten eingefügt werden können, um deren Verhalten zu ändern oder mit ihren Inhalten zu interagieren. Wenn die Erweiterung Inhaltsskripts verwendet, sind die erforderlichen Dateien für diese Skripts in der CRX-Datei vorhanden.
- **Andere Assets:** Abhängig von den spezifischen Erweiterungsanforderungen können zusätzliche Dateien wie Audio- oder Videodateien, Schriftarten oder Datendateien enthalten sein.

Das CRX-Dateiformat ist im Wesentlichen ein komprimiertes Paket, das alle diese Dateien und Ordner strukturiert enthält. Wenn die CRX-Datei in Google Chrome installiert ist, extrahiert der Browser die Inhalte und platziert sie an geeigneten Orten, sodass die Erweiterung geladen und im Browser ausgeführt werden kann.

## Was ist das Format der CRX-Datei?

Das CRX-Dateiformat ist ein spezielles Format zum Verpacken und Verteilen von Google Chrome-Erweiterungen. Es handelt sich im Wesentlichen um ein komprimiertes ZIP-Archiv mit unterschiedlicher Dateierweiterung. Die Grundstruktur der CRX-Datei ist wie folgt:

- **Dateisignatur:** Die ersten 4 Bytes der Datei enthalten die magische Zahl "Cr24" (hexadezimal: 43 72 32 34), die als Signatur dient, um die Datei als CRX-Datei zu identifizieren.
- **Versionsnummer:** Die nächsten 4 Bytes stellen die Versionsnummer des CRX-Formats dar.
- **Länge des öffentlichen Schlüssels:** Die folgenden 4 Bytes geben die Länge des codierten öffentlichen Schlüssels an, der für die Überprüfung der Erweiterungssignatur verwendet wird.
- **Signaturlänge:** Die folgenden 4 Bytes geben die Länge der Signatur der Erweiterung an.
- **Öffentlicher Schlüssel:** Dieser Abschnitt enthält den codierten öffentlichen Schlüssel, der zur Überprüfung der Integrität der Erweiterung verwendet wird.
- **Signatur:** Dieser Abschnitt enthält die Signatur der Erweiterung, die durch Signieren des Inhalts der Erweiterung mit einem privaten Schlüssel generiert wird, der dem oben genannten öffentlichen Schlüssel entspricht.
- **ZIP-Archiv:** Die verbleibenden Bytes der CRX-Datei bilden ein komprimiertes ZIP-Archiv. Dieses Archiv enthält alle notwendigen Dateien und Erweiterungsordner, einschließlich Manifestdateien, JavaScript-Dateien, HTML-Dateien, CSS-Dateien, Bilder und alle anderen Ressourcen.

## Verweise
* [CRX-Formatspezifikation](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)

