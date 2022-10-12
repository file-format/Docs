{
  "date" : "2020-11-11",
  "keywords" :[ "BAK", "Erweiterung", "Datei", "Dateiformat", "BAK-Dateityp", "BAK-Dateierweiterung", "Datenbankdateityp", "Datenbankdateiformat", "Datenbankdateien" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das BAK-Dateiformat und APIs, die BAK-Dateien erstellen und öffnen können.",
  "title" :"BAK-Dateiformat - Datenbanksicherungsdatei",
  "linktitle" :"BAK",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-12-04"
}

## Was ist eine BAK-Datei?

Eine Datei mit der Erweiterung .bak ist normalerweise eine Sicherungsdatei, die von verschiedenen Softwaretools zum Speichern von Datensicherungen verwendet wird. Aus Datenbanksicht wird eine BAK-Datei von Microsoft SQL Server zum Speichern des Inhalts einer Datenbank verwendet. Alle mit der Datenbank verbundenen Daten und Dateien werden in diesem Dateiformat gespeichert, um abgerufen zu werden, falls die Datenbank aus irgendeinem Grund beschädigt oder ungültig wird. Die Sicherungsdateien können zu Sicherheitszwecken auf anderen Servern gespeichert und indiziert werden. Mehrere Anwendungen können BAK-Dateien erstellen, z. B. SQL Server Management Studio, Transact-SQL und Windows PowerShell.

## BAK-Dateiformat

Die internen Details einer BAK-Datei sind nicht bekannt, aber es wird allgemein angenommen, dass sie auf dem Microsoft Tape Format (MTF) basiert. MTF-Spezifikationen sind verfügbar und können zum Verständnis der Struktur der Datei herangezogen werden. Das Dokument enthält Details zur MTF-Speicherung für alle, die über allgemeine Kenntnisse über Speicherverwaltungsvorgänge, Bandlaufwerke und Dateisysteme verfügen.

### Datensätze

Ein Datensatz ist eine Sammlung von Objekten, die während der Datensicherung oder -wiederherstellung auf ein Speichermedium (Band, optische Platte usw.) geschrieben werden. Bei großen Datenmengen bestehen Datensätze aus mehreren Medien.

### Grundlegende Elemente von MTF

Eine MTF-Datei besteht aus einigen grundlegenden Elementen, die ihre Bausteine bilden. Diese Elemente sind:

#### Deskriptorblöcke

Deskriptorblöcke (DBLK) werden zur Formatsteuerung verwendet und bilden die primäre Grundlage einer MTF-Datei. Eine einzelne MTF-Datei definiert mehrere DBLKs für jede eindeutige Rolle. Jeder DBLK ist ein Datenblock variabler Länge, der in die folgenden vier Teile unterteilt ist:

* "Common Block Header" - Struktur mit fester Länge, die allen DBLKs gemeinsam ist. Dies ist der einzige Block-Header, der erforderlich ist.
* "DBLK Type Information" - Block fester Länge, der spezifisch für den zu definierenden DBLK-Typ ist
* „Betriebssystemdaten“ – Spezifische Daten, die basierend auf dem DBLK-Typ und den Betriebssystemen definiert werden
* "DBLK-Informationen" - DBLK-spezifische Informationen variabler Länge, die nicht mit den DBLK-Informationen fester Länge gespeichert werden können.

 {{< figure src="../bak.png" alt="Microsoft SQL-Sicherungsdateiformat" >}}

#### Datenstrom

Datenströme in einer MTF-Datei werden zur Datenkapselung und -ausrichtung verwendet. Es besteht aus einem Stream-Header, gefolgt von den Stream-Daten. Ein Stream-Header kann nur einen einzigen Typ von Stream-Daten kapseln.

{{< figure src="../bak_datastream.png" alt="Microsoft SQL-Sicherungsdateiformat" >}}

#### Dateimarken

Eine Dateimarke dient der logischen Trennung und dem schnellen Zugriff innerhalb eines Mediums. Dateimarken werden vom Gerätetreiber oder durch Verwendung des Soft Filemark Descriptor-Blocks emuliert, falls das verwendete Gerät keine Dateimarken bereitstellt.

## Verweise ##

* [[MS-BCP]: Massenkopierformat](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5?redirectedfrom=MSDN)

