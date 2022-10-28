{
  "date" : "2021-06-21",
  "keywords" :[ "UDL", "Erweiterung", "UDL-Datei", "UDL-Dateiformat", "Datenbankdateityp", "Datenbankdateiformat", "Was ist eine UDL-Datei" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das UDL-Dateiformat und APIs, die UDL-Dateien erstellen und öffnen können.",
  "title" :"UDL - Microsoft Universal Data Link-Datei",
  "linktitle" : "UDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-21"
}

## Was ist eine UDL-Datei?
Die Datei mit der Erweiterung .udl heißt Microsoft Universal Data Link-Datei; Spezifizieren von Verbindungsattributen; Wird von Windows-Apps verwendet, um eine Verbindung mit der Datenbank herzustellen. Die UDL-Datei enthält die Verbindungszeichenfolge für eine OLE DB-Datenquelle; mit Benutzername und Passwort und wesentlichen Eigenschaften der Verbindungszeichenfolge. Um zu vermeiden, dass die Eigenschaften direkt von Hand in einer Verbindungszeichenfolge angegeben werden, kann alternativ ein Dialogfeld Datenverknüpfungseigenschaften verwendet werden, um Verbindungsinformationen in einer .udl-Datei zu speichern.

## UDL-Dateiformat
Grundsätzlich ist eine UDL-Datei (Universal Data Link) eine einfache Textdatei, die aus einer Datenbankverbindungszeichenfolge mit bestimmten Attributen oder Eigenschaften besteht. Nachdem die UDL-Datei erstellt wurde, kann sie mithilfe von SQL Server Management Studio getestet werden, um die Konnektivität zu überprüfen.

### Eigenschaften der Verbindungszeichenfolge
Die folgenden Eigenschaften können in einer UDL festgelegt werden, um die ordnungsgemäße Konnektivität sicherzustellen:

- **Servername**: Standort des Servers, auf dem sich die Datenbank befindet, auf die Sie zugreifen möchten.
- **Authentifizierungsoptionen**
- **Windows-Authentifizierung**: Authentifizierung bei SQL Server mit den Anmeldeinformationen des Windows-Kontos des aktuell angemeldeten Benutzers.
- **SQL Server-Authentifizierung**: Authentifizierung mit Login-ID und Passwort.
- **Active Directory – Integriert**: Integrierte Authentifizierung mit einer Azure Active Directory-Identität; kann auch für die Windows-Authentifizierung bei SQL Server verwendet werden.
- **Active Directory - Kennwort**: Benutzer-ID und Kennwortauthentifizierung mit einer Azure Active Directory-Identität.
- **Active Directory – Universell mit MFA-Unterstützung**: Interaktive Authentifizierung mit einer Azure Active Directory-Identität.
- **Active Directory – Dienstprinzipal**: Authentifizierung mit einem Azure Active Directory-Dienstprinzipal.
- **Server-SPN**: Wenn Sie eine vertrauenswürdige Verbindung verwenden, können Sie einen Dienstprinzipalnamen (SPN) für den Server angeben.
- **Benutzername**: Geben Sie die Benutzer-ID ein, die für die Authentifizierung verwendet werden soll, wenn Sie sich bei der Datenquelle anmelden.
- **Passwort**: Geben Sie das Passwort ein, das für die Authentifizierung verwendet werden soll, wenn Sie sich bei der Datenquelle anmelden.
- **Leeres Passwort**: Wenn diese Option aktiviert ist, kann der angegebene Anbieter ein leeres Passwort in der Verbindungszeichenfolge verwenden.
- **Speichern des Passworts zulassen**: Ermöglicht das Speichern des Passworts mit der Verbindungszeichenfolge.
- **Daten stark verschlüsseln**: Daten, die über die Verbindung übertragen werden, werden verschlüsselt.
- **Serverzertifikat vertrauen**: Das Zertifikat des Servers wird validiert.
- **Datenbank**: Name der Datenbank, auf die Sie zugreifen möchten.
- **Datenbankdatei als Datenbanknamen anhängen**: Gibt den Namen der primären Datei für eine anfügbare Datenbank an.

## Verweise ##

* [Microsoft-Datenzugriffskomponenten](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)
* [Universal Data Link (UDL)-Konfiguration](https://docs.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)

