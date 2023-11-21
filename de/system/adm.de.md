{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADM-Datei – Administratives Vorlagendateiformat",
  "description":"Erfahren Sie mehr über das ADM-Dateiformat und wie man ADM-Dateien öffnet.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Was ist eine ADM-Datei?

Eine ADM-Datei ist eine Vorlagendatei, die von der Microsoft-Gruppenrichtliniensoftware verwendet wird, um den Speicherort registrierungsbasierter Richtlinieneinstellungen in der Registrierungsdatei anzugeben. Es wird von Systemadministratoren verwendet, um die Richtlinie für die Verwaltung einer Gruppe von Computern zu definieren, die Teil der Gruppe sind. Diese Informationen werden Teil der Gruppenrichtlinienobjekte (GPOs), die für die Verwaltung der Gruppe erstellt werden.

Sie können ADM-Dateien mit dem Microsoft Group Policy Object Editor öffnen.

## ADM-Dateiformat – Weitere Informationen

ADM-Dateien werden als Unicode-formatierte Textdateien gespeichert. Diese wurden hauptsächlich verwendet, um den Speicherort registrierungsbasierter Richtlinieneinstellungen in der Windows Vista- und Windows 7-Registrierung zu ermitteln.

ADM-Dateien werden nicht mehr unterstützt und wurden durch die Dateien [ADMX](/system/admx/) ersetzt. GPA ignoriert die folgenden Standard-ADM-Dateien auf Computern, auf denen Microsoft Windows Vista Service Pack 1 oder höher ausgeführt wird.

* system.adm
* inetres.adm
* conf.adm
* wmplayer.adm
* wuau.adm

## Verweise

* [Administrative Vorlagendateien – ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ – Verwalten administrativer Vorlagendateien](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

