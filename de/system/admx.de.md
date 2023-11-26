{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADMX-Datei – Format der administrativen Vorlagendatei für Gruppenrichtlinien",
  "description":"Erfahren Sie mehr über das ADMX-Dateiformat und wie man ADMX-Dateien öffnet.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Was ist eine ADMX-Datei?

Eine ADMX-Datei ist eine Richtlinienkonfigurationsdatei, die von der Microsoft Windows-Gruppenrichtliniensoftware verwendet wird, die eine Gruppe von Computern in einer Gruppe verwaltet. Es handelt sich um eine XML-basierte Verwaltungsvorlagendatei, die mit Windows Vista Service Pack 1 eingeführt wurde. ADMX-Dateien enthalten Konfigurationseinstellungen für Benutzerkonten, Betriebssystemkonfigurationen und Anwendungen. ADMX-Dateien werden zum Speichern und Bereitstellen der Konfigurationen für die zentrale Verwaltung vieler Computersysteme verwendet.

Sie können ADMX-Dateien mit jedem XML-kompatiblen Texteditor oder Microsoft-Gruppenrichtlinienobjekt-Editor erstellen oder bearbeiten.

## ADMX-Dateiformat – Weitere Informationen

ADMX-Dateien werden im universellen Dateiformat [XML](/web/xml/) gespeichert, das für Menschen lesbar ist. Es ist ein mehrsprachiges Dateiformat und ermöglicht Systemadministratoren verschiedener Sprachen, mit denselben ADMX-Dateien zu arbeiten. ADMX-Dateien ersetzten das alte Dateiformat [ADM](/system/adm/), bei dem es sich um ein Unicode-formatiertes Textdateiformat handelt. ADMX-Dateien geben die Registrierungsschlüssel an, die geändert werden, wenn eine bestimmte Gruppenrichtlinieneinstellung geändert wird.

### Was kann ich mit der ADMX-Datei machen?

ADMX-Dateien legen fest, welche Aktionen Benutzercomputern, die Teil einer Gruppe sind, erlaubt sein sollen. Die Gruppenrichtlinie erzwingt die in Kombination mit der Active Directory-Software festgelegten Regeln. ADMX-Dateien werden vom zentralen Speicher auf dem Windows-Betriebssystem verwaltet, der ein zentraler Ort in der Domäne ist.

Eine in einer Arbeitsumgebung bereitgestellte ADMX-Datei kann es Administratoren ermöglichen, Richtlinien zu implementieren wie:

* Kontrollieren Sie die Nutzung des Internets
* Herunterladen bestimmter Dateitypen
* Verwendung von Wechseldatenträgern auf den Systemen

## Verweise

* [Administrative Vorlagendateien – ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ – Verwalten administrativer Vorlagendateien](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

