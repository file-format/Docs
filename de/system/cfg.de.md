{
  "date" : "2021-06-29",
  "keywords" :[ "CFG", "Erweiterung", "Datei", "Format", "System", "Konfiguration", "Einstellungen", "Programme", "Computer", "Anwendung" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFG - Dateiformat",
  "description":"Erfahren Sie mehr über das CFG-Dateiformat und APIs, die CFG-Dateien erstellen und öffnen können.",
  "linktitle" : "CFG",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Was ist eine CFG-Datei? ##

Eine Datei mit der Erweiterung .cfg ist eine Art „Einstellungsdatei“. Es ist ein weit verbreiteter Dateityp und wird zum Speichern von Informationen bezüglich Konfiguration und Einstellungen für Computerprogramme verwendet. Die meisten Arten von CFG-Dateien werden im Textformat gespeichert und sollten nicht manuell geöffnet werden, sondern mit einem Texteditor. Es gibt jedoch verschiedene Arten von CFG-Dateien, die sich im Format unterscheiden, in dem die Informationen gespeichert werden. Die Funktionen, die CFG-Dateien bieten, variieren von Anwendung zu Anwendung. Einige Computeranwendungen ermöglichen es den Benutzern, die Syntax ihrer Konfigurationsdateien durch die Verwendung grafischer Interferenzen zu ändern oder zu entwickeln, während andere nur Änderungen unter Verwendung eines Texteditors zulassen. Nach dem Ändern dieser Dateien können die Benutzer die Anwendung anweisen, diese Dateien erneut zu lesen und die Änderungen auf das System anzuwenden.


## CFG-Dateiformat ##

CFG-Dateien werden von verschiedenen Betriebssystemen wie Unix und Unix-ähnlichen Betriebssystemen, MS-DOS, macOS, Microsoft Windows und IBM OS/2 unterstützt. Das Format, in dem diese Dateien gespeichert und in jedem dieser Betriebssysteme verwendet werden, ist unterschiedlich. Die meisten Systeme verwenden und speichern diese Dateien in einem für Menschen lesbaren und bearbeitbaren Nur-Text-Format, während andere ein komplexeres Format darin speichern, abhängig von der Dateinutzung und den Anforderungen des Betriebssystems.

In Unix und Unix-ähnlichen Betriebssystemen werden für die meisten CFG-Dateien verschiedene Formatstile für CFG-Dateien verwendet, das gebräuchlichste Format ist jedoch ein leicht lesbares Nur-Text-Format, und fast alle Formate ermöglichen das Erstellen und Bearbeiten von Kommentaren. Die gebräuchlichsten Dateierweiterungen für CFG-Dateien in diesen Betriebssystemen sind CNF, CONF, CF und INI.

Im MS-DOS-Betriebssystem gab es zunächst nur ein Konfigurationsdateiformat, nämlich Klartext, jedoch brachte MS-DOS 6 die Einführung eines INI-Konfigurationsdateiformats mit sich.

macOS verwendet eine Standard-Konfigurationsdatei für das Eigenschaftenlistenformat.

In Microsoft Windows waren Konfigurationsdateien im Klartext-INI-Stil eine wichtige Quelle zum Speichern und Bearbeiten von Informationen. 1993 wurde jedoch ein neues Datenbanksystem eingeführt, das zu einer Abnahme der Verwendung von Konfigurationsdateien in Microsoft Windows nach 1993 führte.


## CFG-Beispiel ##

Eine Beispiel-CFG-Datei ist unten zu sehen:

```
#########################
## Settings
##

genome_dir = ~/genome/hg18/

> reads_list1
fastq_100k_1_1.txt
fastq_100k_3_1.txt
<

> reads_list2
fastq_100k_1_2.txt
fastq_100k_3_2.txt
<

read_format = FASTQ
quality_format = phred-33
mapper = bowtie
annotations = all.gene.refFlat.txt
out_path = output
max_intron = 400000
max_multi_hit = 10

```
