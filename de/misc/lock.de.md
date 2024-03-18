{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOCK-Dateiformat - Was ist eine Lock-Datei?",
  "description":"Erfahren Sie mehr über das LOCK-Dateiformat und sein .",
  "linktitle" : "LOCK",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Was ist eine LOCK-Datei?

Eine **LOCK**-Datei ist eine umbenannte Datei, die von Anwendungen und Betriebssystemen verwendet wird, um eine Datei oder ein Gerät als gesperrt zu markieren. Dies weist andere Anwendungen an, die Datei nicht zu verwenden, es sei denn, sie ist frei von der Anwendung, die sie verwendet. In den meisten Fällen sind diese Sperrdateien leer, aber in anderen Fällen können sie Informationen enthalten, die sich auf die Sperre beziehen, wie z. B. Eigenschaften und Einstellungen.

Manchmal wird die .lock-Datei von Microsofts .NET Framework verwendet, um **lockeed**-Kopien einer Datenbankdatei zu erstellen. In einem solchen Fall wird eine Kopie der Datenbankdatei mit der Erweiterung .lock geöffnet. Dies erlaubt dem Benutzer nicht, Änderungen an der Datei vorzunehmen, während sie von einem anderen Benutzer verwendet wird.

## LOCK-Dateiformat - Weitere Informationen

Eine LOCK-Datei wird von jeder Anwendung erstellt und ihr Dateiformat ist anwendungsspezifisch. Diese Sperrdateien können sowohl im Text- als auch im Binärdateiformat gespeichert werden.

Das Vorhandensein von Sperrdateien verhindert den gleichzeitigen Zugriff einer Ressource auf mehrere Dateien, die versuchen, auf diese Ressource zuzugreifen. Eine Kopie der Originaldatei wird mit der Erweiterung .lock an den Namen erstellt. Dies weist andere Anwendungen an, nur Lesezugriff auf die Datei zu haben. Beispielsweise wird resource.dat zu resource.data.lock.

Für die Programmiersprache Ruby stoßen Sie möglicherweise auf die Datei **gemfile.lock**. Hier zeichnet Bundler die genauen Versionen auf, die installiert wurden. Wenn also ein Projekt/eine Bibliothek auf einen anderen Computer verschoben wird, sucht das laufende Bundle in der Gemfile nach der exakt relevanten Version.

## Datei sperren unter Linux

Linux unterstützt zwei Arten von Dateisperren: Advisory Locks und Mandatory Locks.

* **Advisory Locks**: Art der Sperrung, die nicht erzwungen wird. In diesem Fall kooperieren beteiligte Prozesse miteinander und erwerben explizit Sperren. Ist dies nicht möglich, werden Hinweissperren ignoriert.

* **Obligatorische Sperren**: Im Falle von obligatorischen Sperren erzwingt das Betriebssystem die Dateisperre, indem es andere Prozesse daran hindert, die Datei zu lesen oder zu schreiben. Dazu ist keine Zusammenarbeit zwischen den Prozessen erforderlich.

Das obligatorische Sperren erfordert keine Zusammenarbeit zwischen den beteiligten Prozessen. Sobald eine obligatorische Sperre für eine Datei aktiviert ist, hindert das Betriebssystem andere Prozesse daran, die Datei zu lesen oder zu schreiben.

## Verweise

* [GemFile und Gemfile.lock in Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)
* [Locking in Linux](https://www.baeldung.com/linux/file-locking)
