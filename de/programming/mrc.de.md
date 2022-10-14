{
  "date" : "2021-09-14", 
  "keywords" :[ "mrc", "Datei", "Erweiterung", "Dateiformat", "mrc-Implementierung", "Programmierhandbuch", "mrc-Beispiel", "mIRC", "mIRC-Skriptsprache", "Dateien der INI", " mSL-Skriptsprache", "mIRC-Sprache", "mIRC-Skripte", "Skriptsprache" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MRC - mIRC-Skriptsprachendatei",
  "description":"Erfahren Sie mehr über das MRC-Dateiformat und APIs, die MRC-Dateien erstellen und öffnen können.",
  "linktitle" :"MRK",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-14"
}

## Was ist eine MRC-Datei?

mIRC ist eine Skriptsprache, die als IRC-Client (Internet Relay Chat) in das Windows-Betriebssystem eingebettet ist. Es bietet eine Möglichkeit zum Schutz vor Spam für den persönlichen und Kanalgebrauch. Um eine bessere Erfahrung der Benutzerkompatibilität zu bieten, ermöglicht diese mIRC-Skriptsprache die Erstellung von Dialogfenstern. Die Dateien, die Skripte enthalten, meist im reinen Textformat, werden mit der Erweiterung MRC oder als Dateien von [INI](/de/system/ini/) gespeichert. Funktionen dieser Sprache sind als Befehle und Bezeichner bekannt (wenn sie einen Wert zurückgeben).

Die mIRC-Sprache ermöglicht das gleichzeitige Laden mehrerer Skriptdateien. Andererseits kann eine Datei dazu führen, dass die andere beim gleichzeitigen Laden nicht mehr verwendet wird. Befehle werden gespeichert und können automatisch im IRC existieren. Die in dieser Sprache verwendeten Befehle und Aliasnamen enthalten keinen Vorrang von Zeichen.

mIRC wird häufig verwendet, um die Bots dazu zu bringen, einen Kanal automatisch zu verwalten, aber es kann auch durch die mSL-Skriptsprache modifiziert werden. Es kann viele neue Funktionen wie Makros, Musikwiedergabe, kleine Makros und Funktionen, grundlegende Spiele oder den Betrieb kleiner Anwendungen einführen.


## Kurze Geschichte ##

Diese Skriptsprache wurde erstmals 1995 von Khaled Adam Bey entwickelt. Auch das Design der Skriptsprache stammt von Khalid. Das Ziel dieser Sprache war die ereignisgesteuerte Programmierung. Anfangs war die Dateierweiterung für die Dateien dieser Programmiersprache .mrc und .ini. Darüber hinaus wurde es unter der Lizenz von proprietärer Software entwickelt.

## Technische Spezifikation ##

Einige Funktionen werden über diese mIRC-Sprache benutzerdefinierte Skripte erstellt und sind als Aliase bekannt. Wenn diese Aliase Werte zurückgeben, werden sie als benutzerdefinierte Kennungen bezeichnet. Alle in dieser mIRC-Sprache enthaltenen Variablen sind dynamisch typisiert. Siegel werden von den mIRC-Skripten verwendet. Ein weiteres Merkmal dieser Skriptsprache sind Popups. Die Benutzer können Popups aufrufen, indem sie sie einfach auswählen. Fernbedienungen werden bestimmten Ereignissen zugewiesen. Die Remotes werden aufgerufen, wenn das entsprechende Ereignis eintritt.

Durch Leerzeichen getrennte Token werden verwendet, um jede Codezeile dieser Sprache zu unterbrechen. Es gibt einige andere beliebte Erweiterungen, die für mIRC-Dateien verwendet werden, wie MDX (mIRC Dialog Extension) und DCX (Dialog Control Extension). Beides sind Dialogerweiterungen und vergleichsweise beliebter. Die Sprachkonstrukte werden durch die Nomenklatur dieser Skriptsprache bezeichnet. Die mIRC-Sprache umfasst verschiedene Aspekte einer Skriptsprache wie lokale und globale Variablen, binäre Variablen, Hash-Tabellen und Dateihandhabung.


## Beispiel für MRC-Dateiformat ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/de/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## Bezug ##

* [MIRC – von Wikipedia](https://en.wikipedia.org/wiki/MIRC_scripting_language)



