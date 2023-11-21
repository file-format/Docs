{
"Datum": "2023-07-18",
   "keywords":[
"PAR",
"PAR-Datei",
"Wie öffnet man eine PAR-Datei",
"Datei",
"PAR-Dateierweiterung",
"Verlängerung",
"Datei"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title": "PAR-Dateiformat – Parchive-Indexdatei",
   "description":"Erfahren Sie mehr über das PAR-Format und APIs, mit denen PAR-Dateien erstellt und geöffnet werden können.",
"linktitle": "PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par",
"parent": "Komprimierung"
}
},
"lastmod": "2023-07-18"
}

## Was ist eine PAR-Datei?

In Parchive-Archiven (PAR) bezieht sich eine .par-Datei auf eine Indexdatei, die eine Gruppe von Paritätsvolumes oder Paritätsblöcken enthält. Diese Indexdatei wird zur Fehlererkennung und Wiederherstellung verwendet, wenn eine oder mehrere Dateien im Archiv verloren gehen oder beschädigt werden.

Ein Parchive-Archiv besteht normalerweise sowohl aus den Originaldatendateien als auch den entsprechenden Paritätsvolumes. Paritätsvolumes werden mithilfe von Reed-Solomon-Fehlerkorrekturalgorithmen erstellt. Diese Paritätsdatenträger enthalten redundante Informationen, die zur Wiederherstellung der Originaldatendateien verwendet werden können.

Die .par-Datei, auch Paritätsdatenträgersatz genannt, enthält Informationen über die Struktur und den Speicherort der Paritätsdatenträger im Archiv. Es dient als Index oder Karte für den Wiederherstellungsprozess. Anhand der .par-Datei kann spezielle PAR-Software bestimmen, welche Paritätsdatenträger benötigt werden und wie sie zur Rekonstruktion der fehlenden oder beschädigten Dateien verwendet werden sollen.

Wenn eine oder mehrere Dateien im Parchive-Archiv nicht mehr zugänglich oder beschädigt sind, kann die .par-Datei in Verbindung mit den verfügbaren Paritätsvolumes verwendet werden, um die verlorenen Daten wiederherzustellen. Die PAR-Software liest die .par-Datei, identifiziert die fehlenden oder beschädigten Dateien und verwendet die Paritätsvolumes, um sie zu rekonstruieren.

## Wie öffne ich eine PAR-Datei?

Um .par-Dateien zu öffnen und zu verwenden, benötigen Sie spezielle PAR-Software. Hier sind einige beliebte Softwareoptionen, die mit .par-Dateien umgehen können:

- **QuickPar:** QuickPar ist eine weit verbreitete PAR-Software für Windows. Es ermöglicht Ihnen, PAR-Dateien zu erstellen, zu überprüfen und zu reparieren. Sie können eine .par-Datei in QuickPar öffnen, um ihre Integrität zu überprüfen, oder sie zum Reparieren beschädigter oder fehlender Dateien in einem Parchive-Archiv verwenden.

- **MultiPar:** MultiPar ist eine weitere beliebte PAR-Software für Windows. Es unterstützt sowohl PAR- als auch PAR2-Dateiformate und bietet erweiterte Funktionen zum Erstellen, Überprüfen und Reparieren von Archiven. MultiPar kann .par-Dateien öffnen und Fehlererkennungs- und Wiederherstellungsvorgänge basierend auf den bereitgestellten Paritätsvolumes durchführen.

- **MacPAR deLuxe:** MacPAR deLuxe ist eine PAR-Software, die speziell für macOS entwickelt wurde. Es unterstützt die Dateiformate PAR und PAR2 und bietet ähnliche Funktionen wie QuickPar und MultiPar. MacPAR deLuxe kann .par-Dateien öffnen und bei der Überprüfung von Archiven und der Wiederherstellung beschädigter oder fehlender Dateien helfen.

## PAR-Dateiformat – Weitere Informationen

Das PAR-Dateiformat, allgemein als Parchive bezeichnet, ist ein spezielles Dateiformat, das zum Erstellen von Paritätsdaten und zur Fehlererkennung und -wiederherstellung in Dateiarchiven verwendet wird. Das PAR-Dateiformat besteht normalerweise aus drei Typen: PAR, PAR2 und PAR3.

- **PAR:** Das ursprüngliche PAR-Dateiformat, auch bekannt als PAR1, wurde vom Parchive-Projekt entwickelt. Es enthält Paritätsdaten, die aus den Originaldatendateien generiert wurden. PAR-Dateien bieten ein grundlegendes Maß an Fehlererkennung und -behebung, weisen jedoch Einschränkungen hinsichtlich der Fehlerkorrekturfunktionen auf.

- **PAR2:** PAR2 ist eine verbesserte Version des PAR-Dateiformats. Es bietet erweiterte Fehlerkorrekturfunktionen und erweiterte Wiederherstellungsfunktionen. PAR2-Dateien werden normalerweise zum Erstellen von Paritätsdaten verwendet, mit denen verlorene oder beschädigte Dateien in einem Archiv wiederhergestellt werden können. PAR2-Dateien bieten einen besseren Schutz vor Datenbeschädigung und werden häufig für Dateiarchivierungszwecke verwendet.

- **PAR3:** PAR3 ist die neueste Version des PAR-Dateiformats und bietet weitere Verbesserungen bei der Fehlerkorrektur und Wiederherstellung. Im Vergleich zu PAR2 bietet es ein noch höheres Maß an Redundanz und Fehlerkorrekturmöglichkeiten. PAR3-Dateien sollen robustere Schutz- und Wiederherstellungsoptionen für in Archiven gespeicherte Daten bieten.

Sowohl PAR2- als auch PAR3-Dateiformate werden von PAR-Software weitgehend unterstützt und bieten die Möglichkeit, die Integrität von Dateien in einem Archiv zu überprüfen und verlorene oder beschädigte Daten wiederherzustellen. PAR- und PAR2-Dateien werden immer noch häufig verwendet, während PAR3-Dateien aufgrund ihrer verbesserten Fehlerkorrekturfunktionen allmählich an Bedeutung gewinnen.

## Verweise
* [Archiv](https://en.wikipedia.org/wiki/Archiv)

