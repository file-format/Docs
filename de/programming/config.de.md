{
  "date" : "2021-04-23",
  "keywords": [ "Konfigurationsdatei", "Konfigurationsdateien", "Konfigurationsdateiformat", "Erweiterung", "Format", "Git-Konfigurationsdatei", "Konfigurationsdateien unter Linux", "Was ist eine Konfigurationsdatei", "Konfigurationsdatei php", "ssh-Konfigurationsdateibeispiel", "aws-Konfigurationsdateibeispiel", "python-Konfigurationsdateibeispiel" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - Konfigurationsdatei",
  "description":"Erfahren Sie mehr über das CONFIG-Dateiformat mit dem CONFIG-Beispiel und APIs, die CONFIG-Dateien erstellen und öffnen können.",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Was ist eine CONFIG-Datei?
Eine CONFIG-Datei wird als Konfigurationsdatei bezeichnet; Wird verwendet, um die Parameter und primären Einstellungen für verschiedene Computersoftware zu konfigurieren. Manche Software liest ihre **Konfigurationsdateien** nur beim Start. Andere überprüfen die Konfigurationsdateien regelmäßig auf Änderungen.

## CONFIG Dateiformat
Das **CONFIG-Dateiformat** wird für Serverprozesse, Softwareanwendungen und Betriebssystemeinstellungen verwendet. Ein Programmierer kann Code schreiben, um eine Software anzuweisen, die Konfigurationsdateien nach einer bestimmten Zeitspanne immer wieder zu lesen und die Änderungen auf den aktuellen Prozess anzuwenden. Es gibt keine endgültigen Standards oder strengen Konventionen für die Syntax der CONFIG-Datei. Zum Beispiel gehört die Web.config-Datei von Microsoft zum CONFIG-Dateiformat, das aus [XML](https://docs.fileformat.com/web/xml/)-basierten Tagsets besteht; kann mit Microsoft Visual Studio oder einem anderen Texteditor bearbeitet werden.

## Beispiele für Konfigurationsdateien:
Da die Konfigurationsdateien nicht nach irgendwelchen Regeln, Standards oder Konventionen erstellt werden, könnten diese Dateien in anderen Formaten geschrieben worden sein. Eine .config-Datei kann auf XML, [JSON](https://docs.fileformat.com/web/json/) oder einem anderen Format basieren. Im Folgenden finden Sie Beispiele für Konfigurationsdateien für bekannte Betriebssysteme und Software:

### Konfigurationsdateien unter Linux
Jedes Linux-Programm ist eine ausführbare Datei, die die Liste der **Opcodes** enthält, die die CPU ausführt, um typische Operationen auszuführen. Der Betrieb fast jedes Programms kann an Ihre Anforderungen angepasst werden, indem Sie seine Konfigurationsdateien ändern. Mehrere Konfigurationsdateien im Linux-System befinden sich im Verzeichnis /etc. Die Konfigurationsdateien können in die folgenden Kategorien eingeteilt werden:
|Kategorie|Beispiel| Kommentare|
---|---|---|
|Zugriff auf Dateien|/etc/host.conf|Teilt dem Netzwerkdomänenserver mit, wie er nach Hostnamen suchen soll.|
|Booten und Anmelden/Abmelden|/etc/rc.d/rc.local|Nicht offiziell. Kann von rc, rc.sysinit oder /etc/inittab.| aufgerufen werden
|Dateisystem|/etc/mtools.conf|Konfiguration für alle Operationen (mkdir, kopieren, formatieren usw.) auf einem DOS-Dateisystem.|
|Systemadministration|/etc/shells|Enthält die Liste möglicher „Shells“, die dem System zur Verfügung stehen.|
|Networking|/etc/gated.conf|Konfiguration für gated. Wird nur vom gated-Daemon verwendet.|
|Systembefehle|/etc/logrotate.conf|Konfiguration für den dynamischen Linker.|
|Daemons|/etc/httpd.conf|Die Konfigurationsdatei für Apache, den Webserver. Diese Datei befindet sich normalerweise nicht in /etc.|
|Benutzerprogramme| /etc/lynx.cfg| Proxy-Einstellungen|
### AWS CONFIG-Dateibeispiel
Die häufig verwendeten Konfigurationseinstellungen und Anmeldeinformationen können in CONFIG-Dateien gespeichert werden, die von der AWS CLI verwaltet werden. Die CONFIG-Datei muss eine Klartextdatei sein, die das folgende Format verwendet:
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### Beispiel für eine SSH-CONFIG-Datei
Die clientseitige OpenSSH-Konfigurationsdatei heißt CONFIG und wird im Verzeichnis .ssh gespeichert. Die SSH-CONFIG-Datei besteht aus der folgenden Struktur:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Beispiel einer Python-CONFIG-Datei
Eine Python-CONFIG-Datei könnte so aussehen:

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## Verweise

* [Linux-Konfigurationsdateien verstehen](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [Konfigurations- und Berechtigungsdateieinstellungen](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [Konfigurationsdateien in Python](https://martin-thoma.com/configuration-files-in-python/)

