{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "extension", "file", "format", "system", "Control Panel File", "Windows", "programs", "computer", "application" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - Systemsteuerungsdatei",
  "description":"Erfahren Sie mehr über das CPL-Dateiformat und APIs, die CPL-Dateien erstellen und öffnen können.",
  "linktitle" :"CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Was ist eine CPL-Datei? ##

Eine CPL-Datei ist eine Art "System"-Datei. Es wird vom Windows-Betriebssystem verwendet. Eine CPL-Datei ist die Abkürzung für Control Panel File. Diese Dateien sind Binärdateien, die mit der Systemsteuerung in einem Microsoft Windows-Betriebssystem geöffnet werden und verwendet werden, um die in der Systemsteuerung verfügbaren Tools darzustellen und zu öffnen, wie z. B. Maus, Displays, Netzwerk usw. Die CPL-Dateien werden normalerweise im Systemordner auf Ihrem Gerät gespeichert. Diese Dateien sollten nicht manuell geöffnet werden.


## CPL-Dateiformat ##

Verschiedene CPL-Dateien in Ihrem Windows-Betriebssystem sind verbunden, um verschiedene Elemente der Systemsteuerung darzustellen. Alle Bedienfeldelemente sind mit einer CPL-Datei verknüpft und haben das Suffix „.cpl“ an ihren Elementen angehängt.

Einige gängige Arten von CPL-Dateien mit ihren Formaten sind:

* Inetcpl.cpl – Für Internet-Eigenschaften auf Ihrem Gerät
* Appwiz.cpl – Zum Hinzufügen oder Entfernen von Programmeigenschaften auf Ihrem Gerät
* Desk.cpl – Für die Anzeigeeigenschaften
* Main.cpl – Für Eigenschaften, die sich auf Maus, Schriftarten, Tastatur und Drucker beziehen.
* Netcpl.cpl – Für netzwerkbezogene Eigenschaften
* System.cpl – Für systembezogene Eigenschaften und den Assistenten zum Hinzufügen neuer Hardware
* TimeDate.cpl – Für Datums- oder Zeiteigenschaften
* Mlcfg32.cpl – Für Microsoft Exchange- oder Windows Messaging-Eigenschaften
* Intl.cpl – Dies bezieht sich auf die Eigenschaften der Ländereinstellungen
* Modem.cpl – Für Modem-bezogene Eigenschaften
* Themes.cpl – Speichert Desktop-Designs und -Eigenschaften.
* Password.cpl – Für Passworteigenschaften
* Mmsys.cpl – Für Multimedia-Eigenschaften
* Wgpocpl.cpl – Bezieht sich auf Microsoft Mail Post Office

## Kurze Geschichte ##

Der Dateityp CPL wurde von Microsoft Windows entwickelt und ist seit Windows 1.0 ein integraler Bestandteil des Windows-Betriebssystems. Es wird immer noch in allen Windows-Versionen verwendet, und alle Eigenschaften von Elementen der Systemsteuerung werden mit diesem Dateityp gespeichert.

## CPL-Beispiel ##

Eine Beispiel-CPL-Datei ist unten zu sehen:

```
<!-- Copyright (c) Microsoft Corporation -->
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity name="Microsoft.Windows.Net.ncpa" processorArchitecture="x86" version="5.1.0.0" type="win32"/>
<description>NCPA CPL</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="x86" 
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
    <security>
        <requestedPrivileges>
            <requestedExecutionLevel level="asInvoker" uiAccess="false"/>
        </requestedPrivileges>
    </security>
</trustInfo>
</assembly>

```
