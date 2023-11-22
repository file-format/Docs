{
"Datum": "20.07.2023",
   "keywords":[
"BEHÄLTER",
"BIN-Datei",
"Datei",
"BIN-Dateierweiterung",
"Verlängerung",
"Datei"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title": "BIN-Dateiformat – ausführbare Unix-Datei",
   "description":"Erfahren Sie mehr über das BIN-Format und APIs, mit denen BIN-Dateien erstellt und geöffnet werden können.",
"linktitle": "BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin",
"parent": "executable"
}
},
"lastmod": "2023-07-20"
}

## Was ist eine BIN-Datei?

Eine BIN-Datei ist eine ausführbare Datei auf Unix-basierten Betriebssystemen wie Linux oder FreeBSD. Es enthält ein kompiliertes Programm, das aus vom Quellcode abgeleitetem Binärcode besteht, wodurch es mit der zugrunde liegenden Systemarchitektur kompatibel ist. Ausführbare Unix-BIN-Dateien können hinsichtlich ihrer Rolle als ausführbare Formate mit Windows-EXE-Dateien und macOS-APP-Dateien verglichen werden.

Im Bereich der Softwareentwicklung für Unix-Systeme werden BIN-Dateien häufig von Entwicklern zum Verpacken und Verteilen von Programmen verwendet. Sie bieten eine praktische Möglichkeit zur Bereitstellung von Software für Benutzer und ermöglichen eine einfache Installation und Ausführung. Neben BIN-Dateien gibt es noch andere Arten von ausführbaren Unix-Dateien, darunter [.ELF](/executable/elf/), .X86, [.RUN](/executable/run/) und .X86_64, die jeweils auf bestimmte Hardware oder zugeschnitten sind System Anforderungen.

Was die interne Struktur einer BIN-Datei betrifft, besteht sie aus codierten Daten, die das Unix-Betriebssystem verwendet, um das eingeschlossene Programm zu identifizieren, zu lesen und auszuführen. Das System verlässt sich auf bestimmte Dateisignaturen oder Header, um die BIN-Datei als ausführbare Datei zu erkennen, gefolgt von der Interpretation und Ausführung der darin enthaltenen Binäranweisungen.

BIN-Dateien werden oft mit einer begleitenden **INSTALL.TXT**-Datei geliefert, die detaillierte Anweisungen zur ordnungsgemäßen Installation und Einrichtung des Programms enthält. Diese Dokumentation stellt sicher, dass Benutzer den Installationsprozess erfolgreich durchlaufen und ohne Komplikationen mit der Nutzung der Software beginnen können.

## Wie öffne ich eine BIN-Datei?

BIN-Dateien sind nicht dafür gedacht, direkt geöffnet und angezeigt zu werden. Sie können die Programme jedoch ausführen oder die darin enthaltenen Daten extrahieren. Um auf den Inhalt einer BIN-Datei zuzugreifen, führen Sie in der Befehlszeile die folgenden Schritte aus, vorausgesetzt, der Name der BIN-Datei lautet "sample.bin":

1. **Stellen Sie ausführbare Berechtigungen sicher:**

Stellen Sie vor dem Ausführen der BIN-Datei sicher, dass sie über die erforderlichen Berechtigungen für die Ausführung als ausführbare Datei verfügt. Verwenden Sie den Befehl:

```
$ chmod +x sample.bin
```

Dieser Befehl gewährt der Datei ausführbare Berechtigungen.

2. **Führen Sie die BIN-Datei aus:**

Nachdem Sie die ausführbaren Berechtigungen festgelegt haben, können Sie die BIN-Datei ausführen, indem Sie den folgenden Befehl eingeben:

```
$ ./sample.bin
```

**Warnung**

_Seien Sie vorsichtig beim Umgang mit heruntergeladenen oder per E-Mail verschickten BIN-Dateien, da diese möglicherweise von Cyberkriminellen zur Verbreitung von Malware verwendet werden können. Führen Sie BIN-Dateien nur aus vertrauenswürdigen Quellen aus, um das Risiko böswilliger Angriffe auf ausführbare Dateien zu verringern._

## Andere BIN-Dateien

Hier sind andere Dateitypen, die die Dateierweiterung **.bin** verwenden.

- [BIN – MacBinary Encoded File](/compression/bin/)
- [BIN – Binäre Disc-Image-Datei](/disc-and-media/bin/)
- [BIN – BlackBerry IT-Richtliniendatei](/settings/bin/)
- [BIN – Sega Genesis Game ROM](/game/bin/)
- [BIN – PSX PlayStation BIOS Image](/game/bin-pcsx/)

## Verweise

* [So führen Sie Binärdateien unter Linux aus](https://linuxhint.com/execute-binary-files-in-linux/)


