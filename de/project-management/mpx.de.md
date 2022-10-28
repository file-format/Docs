{
  "date" : "2019-10-11",
  "keywords" :[ "mpx-Datei", "mpx-Dateiformat", "was ist eine mpx-Datei", "Datei", "mpx-Beispiel", "mpx-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPX - Microsoft Project Exchange-Dateiformat",
  "description":"Erfahren Sie mehr über das MPX-Dateiformat und APIs, die MPX-Dateien erstellen und öffnen können.",
  "linktitle" : "MPX",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## Was ist eine MPX-Datei? ##

Eine Datei mit der Erweiterung .mpx ist ein Microsoft Exchange-Dateiformat. Ein MPX-Dateiformat wurde von Microsoft Project (MSP) entwickelt, um den Austausch von Projektinformationen zwischen MSP und anderen Anwendungen zu erleichtern, die das MPX-Dateiformat unterstützen, einschließlich Primavera Project Planner, Sciforma und Timerline Precision Estimating. Mithilfe der MPX-Dateien können Sie alle Arten von Informationen aus einem Projekt in ein anderes System übertragen, z. B. detaillierte Ressourcenzuweisungsinformationen, Kalenderinformationen oder Informationen aus dem Dialogfeld „Projektinformationen“.

Microsoft Project 4.0 führte die Unterstützung zum Erstellen und Lesen von MPX-Dateiformaten ein, die weiterhin über Microsoft Project 98 verwendet wurden. Die Unterstützung zum Erstellen von MPX-Dateien wurde jedoch mit der Veröffentlichung von Microsoft Project 2000 eingestellt, und die Versionen bis Microsoft Project 2010 unterstützen nur das Lesen von MPX. Das MPX-Dateiformat wird in Versionen nach MSP 2010 nicht unterstützt.

## MPX-Dateiformat ##

Dieser Abschnitt gibt einen Überblick über die Spezifikationen der MPX-Datei. Vollständige Spezifikationen finden Sie in dieser [Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) Artikel und kann für Details verwiesen werden.

### Aufzeichnungen ###

Ein Datensatz der MPX-Datei besteht aus Informationen für das Projekt. Es gibt verschiedene Arten von Datensätzen, bei denen jeder Datensatz seine eigene Reihenfolge hat. Jeder Datensatztyp wird durch seine Datensatznummer identifiziert. Für eine MPX-Datei muss der Datensatztyp Dateierstellung enthalten sein. Andere Arten von Aufzeichnungen sind nicht obligatorisch. Die folgende Tabelle zeigt alle Datensatztypen, ihre Datensatznummern und die Anzahl der Datensätze, die jeder Typ in der MPX-Datei enthalten kann. Die Aufnahme von Datensätzen in die MPX-Datei muss der Tabellenreihenfolge folgen, wobei Kommentare überall eingefügt werden müssen.

|Datensatzname|Datensatznummer|Maximale Anzahl von Datensätzen
---|---|---|
|Dateierstellung (erforderlich)|keine|1
|Währungseinstellungen|10|1
|Standardeinstellungen|11|1
|Datums- und Uhrzeiteinstellungen|12|1
|Basiskalenderdefinition|20|250
|Basiskalenderstunden|25| 7 pro Basiskalender-Definitionsdatensatz
|Basiskalender-Ausnahme|26| 250 pro Basiskalender-Definitionsdatensatz
|Projektkopf|30|1
|Text-Ressourcentabellen-Definition|140|1- (Oder Sie können den numerischen Ressourcentabellen-Definitionsdatensatz verwenden)
|Definition der numerischen Ressourcentabelle|41|1
|Ressource|50|9.999
|Ressourcenhinweise|51| 1 pro Ressourcendatensatz
|Ressourcenkalender-Definition|55| 1 pro Ressourcendatensatz
|Ressourcenkalenderstunden|56| 7 pro Ressourcenkalender
|Ressourcenkalender-Ausnahme| 57|250 pro Ressourcenkalender
|Text-Aufgabentabellen-Definition|60|1 (Sie können auch den numerischen Aufgabentabellen-Definitionsdatensatz verwenden)
|Numerische Aufgabentabellendefinition|61|1
|Aufgabe|70|9
|Aufgabenhinweise|71| 1 pro Aufgabendatensatz
|Wiederkehrende Aufgabe|72| 1 pro Aufgabendatensatz
|Ressourcenzuordnung|75| 100 pro Aufgabendatensatz
|Zuordnung Arbeitsgruppenfelder|76| 1 pro Zuordnungsdatensatz
|Projektnamen|80|500
|DDE- und OLE-Client-Links|81|500
|Kommentare|0|unbegrenzt

### Dateistruktur ###

Eine MPX-Datei besteht aus den oben erwähnten Datensätzen, die innerhalb der Datei in voreingestellter Weise angeordnet sind. Einzelheiten zu diesen Datensatztypen werden wie folgt besprochen:

**File Creation Record (FCR):** Dies ist ein obligatorischer Datensatz, dessen Zweck es ist, Folgendes zu identifizieren:

* Dateiformat (MPX)
* Listentrennzeichen, das in der Datei verwendet wird
* Programm- und Versionsnummer, mit der die Datei erstellt wurde
* Versionsnummer des in der Datei verwendeten MPX-Dateiformats
* Codepage, die zum Erstellen der Datei verwendet wird

Dies muss der erste Datensatz in der Datei sein. Beim Exportieren aus Microsoft Project wird das Listentrennzeichen im Element Ländereinstellungen in der Windows-Systemsteuerung angegeben. Ein FCR-Eintrag enthält die folgenden Felder:

* MPX unmittelbar gefolgt vom Listentrennzeichen
* Programmname/-kennung
* Versionsnummer der Datei
* Codepage (850, 437, MAC, ANSI)

Beispielsweise kann der Datensatz die Information **MPX, Microsoft Project, 3.0** enthalten, die angibt, dass in dieser MPX-Datei ein Komma als Listentrennzeichen verwendet wird. Die in der Datei verwendete Version des MPX-Formats wird aus Microsoft Project Version 3.0 exportiert.

**Währungseinstellungen** Dieser Datensatz mit der Datensatznummer 10 gibt Einstellungen für die Währungsoptionen im Dialogfeld „Optionen“ an. Wenn dieser Datensatz nicht enthalten ist, werden die aktuellen Einstellungen im Dialogfeld Optionen verwendet. Die Tausender- und Dezimaltrennzeichen werden im Element Ländereinstellungen in der Windows-Systemsteuerung angegeben.
Die in diesem Datensatz enthaltenen Felder sind:

* Währungszeichen
* Symbolposition (0 # danach, 1 # davor, 2 # danach mit Leerzeichen, 3 # davor mit Leerzeichen)
* Währungsziffern (0,1,2)
* Tausendertrennzeichen
* Dezimaltrennzeichen

**Beispiel:** 10,$,1,2,",",.
Dieses Beispiel gibt an, dass Währungswerte ein Dollarzeichen ($) davor enthalten, dass zwei Ziffern nach dem Dezimalkomma enthalten sind, dass ein Komma verwendet wird, um Tausender zu trennen, und dass ein Punkt als Dezimalkomma verwendet wird. Da das Listentrennzeichen im Feld Tausendertrennzeichen enthalten ist, ist das Feld in Anführungszeichen eingeschlossen.

**Standardeinstellungen:** Dieser Datensatz mit der Datensatznummer 11 gibt Einstellungen für die Standardoptionen im Dialogfeld „Optionen“ an. Wenn keine Dauer angegeben ist, muss die Standard-Dauereinheit für korrekte Berechnungen der Dauereinheit festgelegt werden. Wenn dieser Datensatz nicht enthalten ist, werden die aktuellen Einstellungen im Dialogfeld Optionen verwendet.
Die in diesem Datensatz enthaltenen Felder sind:

* Standarddauereinheiten (0 # Minuten, 1 # Stunden, 2 # Tage, 3 # Wochen)
* Standarddauertyp (0 # nicht festgelegt, 1 # festgelegt)
* Standardarbeitseinheiten (0 # Minuten, 1 # Stunden, 2 # Tage, 3 # Wochen)
* Standard Stunden/Tag
* Standard Stunden/Woche
* Standard-Standardpreis
* Standardsatz für Überstunden
* Aktualisieren des Aufgabenstatus aktualisiert den Ressourcenstatus (0 # nein, 1 # ja)
* In Bearbeitung befindliche Aufgaben aufteilen (0 # nein, 1 # ja)

**Datums- und Zeiteinstellungen:** Dieser Datensatz mit der Datensatznummer 12 legt Einstellungen für die Datums- und Zeitoptionen im Dialogfeld „Optionen“ und die Option „Balkentext-Datumsformat“ im Dialogfeld „Layout“ fest. Wenn dieser Datensatz nicht enthalten ist, werden die aktuellen Einstellungen im Dialogfeld Optionen verwendet.
\\Die in diesem Datensatz enthaltenen Felder sind:

* Datumsreihenfolge (0 # Monat/Tag/Jahr, 1 # Tag/Monat/Jahr, 2 # Jahr/Monat/Tag)
* Zeitformat (0 # 12 Stunden, 1 # 24 Stunden)
* Standardzeit (Anzahl der Minuten nach Mitternacht)
* Datumstrennzeichen
* Zeittrennzeichen
* 0:00 bis 11:59 Text
* 12:00 bis 23:59 Text
* Datumsformat (0 -14)*
* Balkentext Datumsformat (0 -194)*

**Definition des Basiskalenders:** Diese Datensätze mit der Datensatznummer 20 definieren Basiskalender und ihre Arbeits- und arbeitsfreien Tage der Woche. Wenn für einen Tag kein Eintrag vorhanden ist, werden die Standardeinstellungen verwendet. Die Standardeinstellungen sind Montag bis Freitag für Werktage und Samstag und Sonntag für arbeitsfreie Tage. In diesem Datensatz ist das Feld Name erforderlich. Für jeden der Tage zeigt ein Eintrag von 0 an, dass der Tag ein arbeitsfreier Tag ist, und ein Eintrag von 1 zeigt an, dass der Tag ein Arbeitstag ist.
Die in diesem Datensatz enthaltenen Felder sind:

* Name
* Sonntag
* Montag
* Dienstag
* Mittwoch
* Donnerstag
* Freitag
* Samstag

**Basiskalenderstunden:** Diese Datensätze mit der Datensatznummer 25 geben die Arbeitszeiten für die Wochentage an, wenn sie von den Standardeinstellungen abweichen. Die Standardarbeitszeiten sind 8:00 bis 12:00 Uhr und 13:00 bis 17:00 Uhr. Jeder Basiskalenderstunden-Datensatz bezieht sich auf den vorhergehenden Basiskalender-Definitionsdatensatz. Auf jeden Basiskalender-Definitionsdatensatz können bis zu sieben dieser Datensätze folgen.

* Wochentag (1 - 7, wobei 1 # Sonntag und 7 # Samstag)
* Ab Zeit 1
* Bis Zeit 1
* Ab Zeit 2
* Bis Zeit 2
* Ab Zeit 3
* Bis Zeit 3

**Basiskalenderausnahme:** Diese Datensätze mit der Datensatznummer 26 definieren die Ausnahmen zu den Tagen und Stunden, die in den vorherigen zwei Datensatztypen angegeben sind. Auf jeden Datensatz der Basiskalenderdefinition können bis zu 250 dieser Datensätze folgen. Diese Aufzeichnungen müssen in chronologischer Reihenfolge aufgeführt werden. Wenn eine Ausnahme ein Tag ist, können Sie das Feld Bis Datum leer lassen. Wenn keine Zeiten angegeben sind, werden die Standardzeiten von 8:00 bis 12:00 Uhr und 13:00 bis 17:00 Uhr verwendet.
Die in diesem Datensatz enthaltenen Felder sind:

* Ab Datum
* Miteinander ausgehen
* Nicht arbeitend/Arbeitend (0 # nicht arbeitend, 1 # arbeitend)
* Ab Zeit 1
* Bis Zeit 1
* Ab Zeit 2
* Bis Zeit 2
* Ab Zeit 3
* Bis Zeit 3

**Projektkopf:** Dieser Datensatz mit dem Datensatzwert 30 legt globale Projektfelder fest, wie z. B. das Projektstartdatum und das Projektenddatum. Die Felder in diesem Datensatz entsprechen den Informationen in den Dialogfeldern Projektinfo und Statistik.
Die in diesem Datensatz enthaltenen Felder und Registerkarten sind:

* Registerkarte Projekt
* Gesellschaft
* Manager
* Kalender (Standard verwendet, wenn kein Eintrag)
* Startdatum (entweder dieses Feld oder das nächste Feld wird für eine importierte Datei berechnet, abhängig von der Einstellung „Planen von“)
* Enddatum
* Zeitplan von (0 # Start, 1 # Ende)
* Aktuelles Datum*
* Kommentare
* Kosten
* Basiskosten
* Tatsächliche Kosten
* Arbeit
* Basisarbeit
* Eigentliche Arbeit
* Arbeit
* Dauer*
* Baseline-Dauer*
* Tatsächliche Dauer
* Prozent abgeschlossen
* Basisstart
* Basis-Finish
* Tatsächlicher Start
* Tatsächliches Ende
* Varianz starten
* Finish-Varianz
* Thema
* Autor
* Schlüsselwörter

**Definition der Textressourcentabelle**: Dieser Datensatz listet die Ressourcenfelder der Reihe nach auf, die importiert oder exportiert werden. Bei importierten Dateien müssen die Namen mit den in Microsoft Project verwendeten Feldnamen übereinstimmen. Bei exportierten Dateien stammt dieser Datensatz aus der Exporttabelle der Ressource. Entweder dieser Datensatz oder der Datensatz der Definition der numerischen Ressourcentabelle muss verwendet werden. Beim Exportieren aus Microsoft Project sind diese beiden Datensätze enthalten.

**Definition der numerischen Ressourcentabelle:** Unter Verwendung von Zahlen anstelle von Namen listet dieser Datensatz die Ressourcenfelder in der Reihenfolge auf, die importiert oder exportiert werden. Dies ist eine alternative Methode zum Identifizieren der Ressourcenfelder, die in jedem Ressourcendatensatz enthalten sind, und ist nützlich, wenn Sie eine MPX-Datei definieren, die von einem fremdsprachigen Produkt erstellt wurde.

**Ressource:** Diese Datensätze enthalten die Informationen für jede Ressource, die importiert oder exportiert wird. Jeder Ressourcendatensatz beschreibt eine Ressource. Wenn Sie Informationen importieren, werden die eingeschlossenen Felder durch den Textressourcentabellen-Definitionsdatensatz oder den numerischen Ressourcentabellendefinitionsdatensatz definiert. Beim Exportieren von Informationen sind die Felder enthalten, die in der Exporttabelle der Ressource aufgeführt sind.

**Ressourcenhinweise:** Diese Datensätze enthalten Hinweise zum unmittelbar vorhergehenden Ressourcendatensatz. Für eine neue Zeile innerhalb der Notiz wird das ASCII-Zeichen 127 verwendet. Wenn die Notiz das Listentrennzeichen enthält, schließen Sie die Notiz in Anführungszeichen ein.

**Ressourcenkalenderdefinition:** Diese Datensätze definieren die Arbeitstage für die Ressource, die im unmittelbar vorhergehenden Ressourcendatensatz angegeben ist. Wenn für importierte Dateien kein Eintrag im Feld Basiskalendername vorhanden ist, wird Standard verwendet. Kein Eintrag für den bestimmten Tag zeigt an, dass der Tag auf den Standardwert (2) eingestellt ist. Wenn keine Ressourcenkalender-Definitionsdatensätze vorhanden sind, wird Standard als Basiskalender für die Ressource verwendet, wobei Standard für die Tage verwendet wird. Für jeden der Tage gibt ein Eintrag von 0 an, dass der Tag ein arbeitsfreier Tag ist, 1 gibt an, dass der Tag ein Arbeitstag ist, und 2 gibt an, dass der Standardwert verwendet wird.

**Ressourcenkalenderstunden:** Diese Datensätze definieren die Arbeitszeiten für die Ressource, die sich von dem von der Ressource verwendeten Basiskalender unterscheiden. Diese Datensätze gelten für den Ressourcenkalender-Definitionsdatensatz, der diesem Datensatz unmittelbar vorausgeht. Auf jeden Ressourcenkalender-Definitionsdatensatz können bis zu sieben dieser Datensätze folgen.

**Ressourcenkalender-Ausnahme:** Diese Datensätze definieren die Ausnahmen zu den Tagen und Stunden, die in den vorherigen zwei Datensatztypen angegeben sind. Bis zu 250 dieser Datensätze können jedem Ressourcenkalender-Definitionsdatensatz folgen. Diese Aufzeichnungen müssen in chronologischer Reihenfolge aufgeführt werden. Wenn die Ausnahme nur ein Tag ist, können Sie das Feld Bis Datum leer lassen. Wenn keine Zeiten angegeben sind, werden die Standardzeiten von 8:00 bis 12:00 Uhr und 13:00 bis 17:00 Uhr verwendet.

**Definition der Textaufgabentabelle:** Dieser Datensatz listet die Aufgabenfelder der Reihe nach auf, die importiert oder exportiert werden. Bei importierten Dateien müssen die Namen mit den in Microsoft Project verwendeten Feldnamen übereinstimmen. Wenn die Datei exportiert wird, stammt dieser Datensatz aus der Exporttabelle der Aufgabe. Beim Exportieren aus Microsoft Project sind diese beiden Datensätze enthalten. Felder, die von Microsoft Project berechnet werden, wie z. B. Geplanter Start und Geplantes Ende, werden beim Import ignoriert. Wenn Sie feste Anfangs- oder Endtermine für Aufgaben haben, verwenden Sie die Felder Einschränkungstyp und Einschränkungsdatum.

**Definition der numerischen Aufgabentabelle:** Unter Verwendung von Zahlen anstelle von Namen listet dieser Datensatz die Aufgabenfelder in der Reihenfolge auf, die importiert oder exportiert werden. Dies ist eine alternative Methode zum Identifizieren der Aufgabenfelder, die in jedem Aufgabendatensatz enthalten sind, und ist nützlich, wenn Sie eine MPX-Datei definieren, die von einem fremdsprachigen Produkt erstellt wurde.

**Aufgabe:** Diese Datensätze enthalten die Informationen für jede Aufgabe, die importiert oder exportiert wird. Jeder Aufgabendatensatz beschreibt eine Aufgabe. Wenn Sie Informationen importieren, werden die eingeschlossenen Felder durch den Datensatz „Textaufgabentabellendefinition“ oder den Datensatz „Numerische Aufgabentabellendefinition“ definiert. Beim Exportieren von Informationen sind die Felder enthalten, die in der Task-Exporttabelle aufgeführt sind.

**Aufgabennotizen:** Diese Datensätze enthalten Notizen zum unmittelbar vorhergehenden Aufgabendatensatz. Verwenden Sie das ASCII-Zeichen 127, um eine neue Zeile innerhalb der Notiz anzuzeigen. Wenn die Notiz das Listentrennzeichen enthält, schließen Sie die Notiz in Anführungszeichen ein.

**Ressourcenzuweisung**: Diese Datensätze listen Informationen über die Ressourcen auf, die der Aufgabe zugewiesen sind, die im vorherigen Aufgabendatensatz definiert wurde. Wenn Sie Dateien zusammenführen und Informationen zur Ressourcenzuweisung beibehalten möchten, müssen Sie die Informationen in die MPX-Datei aufnehmen. Wenn Sie zusammenführen, werden alle vorhandenen Zuweisungen zu zusammengeführten Aufgaben gelöscht. Wenn Sie Dateien basierend auf eindeutigen IDs zusammenführen, werden Ressourcen anhand der eindeutigen Ressourcen-IDs und nicht anhand von IDs zugewiesen.

**Arbeitsgruppenfelder für Ressourcenzuweisungen:** Diese Datensätze listen die Informationen auf, die mit jeder Zuweisung für die Arbeitsgruppenfunktionen von Microsoft Project 4.0 und 4.1 gespeichert werden. Wenn Sie die Workgroup-Funktionen verwenden, müssen Sie diesen Eintrag hinzufügen, um sicherzustellen, dass keine Informationen verloren gehen.

**Projektnamen:** Diese Datensätze listen alle DDE-Verbindungsnamen auf, die im Projekt gespeichert sind.

**DDE- und OLE-Client-Links:** Diese Datensätze listen die DDE-Links in das Projekt auf.

**Kommentare:** Diese Datensätze können zum Hinzufügen von Kommentaren zur Datei verwendet werden und können an jeder Position in der Datei erscheinen. Jeder Kommentardatensatz muss mit einer „0“ beginnen.

## Probleme beim Öffnen einer MPX-Datei ##

Hier ist die Liste einiger häufiger Probleme, die auftreten und Fehlfunktionen des MPX-Formats verursachen können:

* Keine unterstützende Software
* Beschädigte Datei
* Infizierte Datei aufgrund eines Virus
* Kein Zugriffsrecht im System zum Öffnen der Dateien
* Veraltetes Laufwerk in Ihrem System
* Erweiterung der Datei wird umbenannt

## Verweise ##

* [MPX – Microsoft Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)

