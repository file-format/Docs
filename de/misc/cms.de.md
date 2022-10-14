{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CMS-Dateiformat - Verbindungsmanager-Dienstprofildatei",
  "description":"Erfahren Sie mehr über CMS-Dateien und APIs, die CMS-Dateien erstellen und öffnen können.",
  "linktitle" :"CMS",
  "menu" : {
    "docs" : {
"identifier": "misc-cms",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Was ist eine CMS-Datei?

Eine CMS-Datei ist eine Datendatei, die Profilinformationen enthält, die von Microsoft Windows Connection Manager verwendet werden. Es ermöglicht entfernten Benutzern, sich mit diesen Profilinformationen mit einem Netzwerk zu verbinden. Zu den in einer CMS-Datei gespeicherten Informationen gehören Daten über das Betriebssystem des Benutzers und Berechtigungen, die zum Herstellen einer Verbindung zwischen einem entfernten Benutzer und dem Netzwerk verwendet werden. CMS-Administratoren verwenden das Connection Manager Administrator Kit (CMAK), um CMS-Dateien zu generieren.

## CMS-Dateiformat – Weitere Informationen

CMS-Dateien werden häufig nicht auf Benutzercomputern gefunden. Da diese speziell verwendet werden, um entfernten Benutzern den Zugang zu einem Netzwerk zu ermöglichen, finden Sie diese auf Computern, die verwendet werden, um eine Verbindung zu einem Firmennetzwerk oder einem speziell dafür eingerichteten Büro herzustellen. In den meisten Fällen wird es verwendet, um eine Verbindung zu einem Organisationsnetzwerk wie einem Virtual Private Network (VPN) herzustellen, das nur einem Unternehmen gewidmet ist. Als Netzwerkadministrator richten Sie den Zugriff auf ein solches Netzwerk mit Connection Manager ein, damit er von einem entfernten Standort aus auf das Unternehmensnetzwerk zugreifen kann.

### Was ist insdie CMS?

Eine CMS-Profildatei wird mit Connection Manager erstellt und mit anderen Konfigurationsdateien gepackt, bevor sie dem Remotebenutzer bereitgestellt wird. Diese zusätzlichen Dateien können eine CMP- und eine INF-Datei enthalten, die zusammen in einer [EXE](/de/executable/exe/)-Datei gepackt sind. Dieses vollständige Paket wird dem entfernten Benutzer zur Verbindung mit dem Netzwerk bereitgestellt.

## Verweise

* [Windows Connection Manager verstehen und konfigurieren](https://docs.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)

