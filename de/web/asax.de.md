{
  "date" : "2019-10-11",
  "keywords" :[ "asax","asax-Datei", "asax-Dateiformat", "asax-Dateityp", "Datei", "Typ", "was ist eine asax-Datei" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASAX - ASP.NET-Serveranwendungsdatei",
  "description" :"Erfahren Sie, was eine ASAX-Datei und APIs sind, die ASAX-Dateien erstellen und öffnen können.",
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-07"
}

## Was ist eine ASAX-Datei?

Eine Datei mit der Erweiterung .asax ist eine Datei, die von ASP.NET-Anwendungen verwendet wird und sich auf der Serverseite befindet. Es enthält Code zum Reagieren auf Ereignisse auf Anwendungs- und Sitzungsebene, die von ASP.NET oder von HTTP-Modulen ausgelöst werden. Dazu gehört auch die Behandlung bestimmter Ereignisse beim Starten oder Beenden der Anwendung. ASAX-Dateien sind optional und Webanwendungen wird nur eine einzige ASAX-Datei hinzugefügt, um die Ereignisse und Fehler auf Anwendungsebene auf globaler Ebene zu behandeln. Im Gegensatz zu ASPX-Seiten enthalten ASAX-Dateien keinen Code zum Implementieren der Funktionalität der Anwendung.

## ASAX-Dateiformat

ASAX-Dateien werden im Nur-Text-Dateiformat geschrieben und sind für Menschen lesbar. Die am häufigsten verwendete ASAX-Datei ist Global.asax, die sich im Stammverzeichnis einer ASP.NET-Anwendung befindet. Webserver sind so konfiguriert, dass sie alle eingehenden Aufrufe dieser Datei ablehnen, um Benutzern das Herunterladen oder Anzeigen des Codes dieser Datei zu verbieten.

### Global.ASAX - Ein Beispiel für das ASAX-Dateiformat

Eine einzelne ASAX-Datei besteht aus mehreren Abschnitten, die geschrieben werden, um die Ereignisse auf Anwendungsebene zu verarbeiten. Diese sind wie folgt.

* **Anwendungsdirektiven** – Anwendungsdirektiven sind Tags, die zum Definieren optionaler anwendungsspezifischer Einstellungen verwendet werden, die vom ASP.NET-Parser beim Verarbeiten der Datei Global.asax verwendet werden. Diese Direktiven befinden sich am Anfang der Datei Global.asax und sind wie folgt definiert.

```
<%@ Direktive Attribut=Wert [Attribut=Wert … ]%>
```
* **Code-Deklarationsblöcke** - Code-Deklarationsblöcke werden verwendet, um Abschnitte des Servercodes zu definieren, die in ASP.NET-Anwendungsdateien innerhalb des \<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

```
<html>
  <script language="C#" runat="server">
      void EnterBtn_Click(Object Src, EventArgs E) {
          Message.Text = "Hi " + Name.Text + ", welcome to ASP.NET!";
  }
  </script>

  <body>
   <form runat="server">
    Enter your name: <asp:textbox id="Name" runat=server/>
                     <asp:button text="Enter" Onclick="EnterBtn_Click" runat="server"/>
        <p>
        <asp:label id="Message" runat=server/>
    </form>
  </body>
</html>
```
* **Code-Rendering-Blöcke** – Diese definieren den Inline-Code oder die Ausdrücke, die ausgeführt werden, wenn die Seite gerendert wird. Die zwei Arten von Coderenderblöcken umfassen Inline-Code und Inline-Ausdrücke. Ersteres wird verwendet, um in sich geschlossene Codezeilen oder -blöcke zu definieren, während laterales als Abkürzung zum Aufrufen der Write-Methode verwendet wird.

## Verweise

* [Übersicht über HTTP-Handler und HTTP-Module](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
* [Global.asax-Syntax](https://learn.microsoft.com/en-us/ previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

