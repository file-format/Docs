{
  "date" : "2019-10-11",
  "keywords" :[ "ascx","ascx-Datei", "ascx-Dateiformat", "ascx-Dateityp", "Datei", "Typ", "was ist eine ascx-Datei" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASCX-Dateiformat",
  "description" :"Erfahren Sie, was eine ASCX-Datei und APIs sind, die ASCX-Dateien erstellen und öffnen können.",
  "linktitle" : "ASCX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Was ist eine ASCX-Datei?

Eine Datei mit der Erweiterung .ascx ist ein Benutzersteuerelement, das als wiederverwendbare Komponente in Webseiten verwendet wird. Es wird in jeder ASP-Website referenziert, indem es aus dem Kontrollfeld auf die Seite gezogen wird. ASCX-Benutzersteuerelemente werden dem Projekt als zentrale Quelle hinzugefügt, was dazu führt, dass jede Änderung des Benutzersteuerelements auf der gesamten Website widergespiegelt wird. Im Gegensatz zu ASMX-Dateien, die einen Mechanismus zur Kommunikation innerhalb von zwei Objekten über das Internet definieren, sind ASCX-Dateien Benutzersteuerelemente zum Einbetten in Seiten oder Websites.

## ASCX-Dateiformat

ASCX-Dateien werden im Nur-Text-Format geschrieben und können Code hinter Funktionen wie Webseiten verwenden, die mit .ascx.cs enden. Der Markup-Code von Benutzersteuerelementen beginnt mit der Direktive @Control, wie im folgenden Beispiel gezeigt.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

Dieses Web-Benutzersteuerelement kann auf vielen Seiten wiederverwendet werden, z. B. als Seitenfuß, Kopfzeile oder eine Art Website-Navigation. Webbenutzer-Steuerelemente haben wie jedes andere Steuerelement Eigenschaften, Methoden und Ereignisse, die sie beim Festlegen ihres visuellen Verhaltens nützlich machen.

### Beispiel für die Registrierung von Benutzersteuerelementen in web.config

Um ein einzelnes Benutzersteuerelement auf vielen Seiten zu verwenden, kann das Websteuerelement in der web.config registriert werden. Dies ermöglicht die Kontrolle über die gesamte Website, anstatt sich auf jeder Seite einzeln zu registrieren. Der folgende Beispielcode definiert, wie ein Websteuerelement in web.config registriert wird, damit es als Fußzeile auf der gesamten Website angezeigt wird.

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## Verweise

* [ASCX vs. ASMX](https://social.msdn.microsoft.com/Forums/en-US/a27d4c2f-b972-439e-a7fe-f4b7e3637700/how-to-work-with-ascx-files?forum=aspwebforms)
* [ASCX-Benutzersteuerung](http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

