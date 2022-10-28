{
  "date" : "2021-06-28",
  "keywords" :[ "cgi-Datei", "was ist eine cgi-Datei", "Datei", "cgi-Beispiel", "cgi-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das CGI-Dateiformat und APIs, die CGI-Dateien erstellen und öffnen können.",
  "title" :"CGI - Common Gateway Interface-Skriptdatei",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## Was ist eine CGI-Datei?
Eine CGI-Datei ist als Common Gateway Interface-Skript bekannt, das von einem Webserver verwendet wird, um ein externes Programm zur Verarbeitung von Benutzeranforderungen auszuführen. Das Skript, das in einer Datei mit der Erweiterung .cgi gespeichert wird, ist normalerweise in den Programmiersprachen C oder Perl geschrieben. Der wurde seit den Anfängen des Webs eingeführt, als Webentwickler Datenbanken mit ihren Webservern verbinden wollten. Ein Server, der ein gemeinsames Gateway zwischen Webserver und Datenbanken unterstützte, war gut geeignet, um den CGI-Code auszuführen.

## CGI-Dateiformat
Die CGI-Skripte werden vom Webserver verwendet, um dem Besitzer zu erleichtern, zu konfigurieren, wie eine URL gehandhabt wird. Das Verfahren wird normalerweise durchgeführt, indem ein neues Verzeichnis (in dem sich die Dokumente hauptsächlich befinden) als CGI-Skripte enthaltend markiert wird; sein allgemein bekannter Name ist cgi-bin. Beispielsweise könnte /usr/local/apache/htdocs/cgi-bin als CGI-Verzeichnis auf dem Webserver ausgewählt werden. Wenn ein Webbrowser eine URL anfordert, die auf eine Datei im CGI-Verzeichnis verweist, sendet HTTP Server führt das angegebene Skript aus und gibt die Ausgabe des Skripts an den Webbrowser zurück. Kurz gesagt, alles, was das CGI-Skript an die Standardausgabe sendet, wird an den Webclient übertragen, anstatt in einem Terminalfenster angezeigt zu werden.

### CGI-Beispiel

Das folgende in Perl geschriebene CGI-Skript zeigt alle vom Webserver übergebenen Umgebungsvariablen:
```
#!/usr/bin/env perl

=head1 DESCRIPTION

printenv — a CGI program that just prints its environment

=cut
print "Content-Type: text/plain\n\n";

for my $var ( sort keys %ENV ) {
    printf "%s=\"%s\"\n", $var, $ENV{$var};
}
```

Die Ausgabe sieht wie folgt aus:
```
COMSPEC="C:\Windows\system32\cmd.exe"
DOCUMENT_ROOT="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/htdocs"
GATEWAY_INTERFACE="CGI/1.1"
HOME="/home/SYSTEM"
HTTP_ACCEPT="text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8"
HTTP_ACCEPT_CHARSET="ISO-8859-1,utf-8;q=0.7,*;q=0.7"
HTTP_ACCEPT_ENCODING="gzip, deflate, br"
HTTP_ACCEPT_LANGUAGE="en-us,en;q=0.5"
HTTP_CONNECTION="keep-alive"
HTTP_HOST="example.com"
HTTP_USER_AGENT="Mozilla/5.0 (Windows NT 6.1; WOW64; rv:67.0) Gecko/20100101 Firefox/67.0"
PATH="/home/SYSTEM/bin:/bin:/cygdrive/c/progra~2/php:/cygdrive/c/windows/system32:..."
PATHEXT=".COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC"
PATH_INFO="/foo/bar"
PATH_TRANSLATED="C:\Program Files (x86)\Apache Software Foundation\Apache2.4\htdocs\foo\bar"
QUERY_STRING="var1=value1&var2=with%20percent%20encoding"
REMOTE_ADDR="127.0.0.1"
REMOTE_PORT="63555"
REQUEST_METHOD="GET"
REQUEST_URI="/cgi-bin/printenv.pl/foo/bar?var1=value1&var2=with%20percent%20encoding"
SCRIPT_FILENAME="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/cgi-bin/printenv.pl"
SCRIPT_NAME="/cgi-bin/printenv.pl"
SERVER_ADDR="127.0.0.1"
SERVER_ADMIN="(server admin's email address)"
SERVER_NAME="127.0.0.1"
SERVER_PORT="80"
SERVER_PROTOCOL="HTTP/1.1"
SERVER_SIGNATURE=""
SERVER_SOFTWARE="Apache/2.4.39 (Win32) PHP/7.3.7"
SYSTEMROOT="C:\Windows"
TERM="cygwin"
WINDIR="C:\Windows"
```
## Verwendung von CGI-Skripten
Die CGI-Dateien, die die CGI-Skripte enthalten, werden normalerweise verwendet, um Eingabedaten des Benutzers zu verarbeiten und die entsprechenden Ausgabedaten zu erzeugen. Die Implementierung eines Wikis ist eines der Beispiele für CGI-Programme. Wenn der Benutzeragent eine Anfrage nach dem Namen eines Eintrags sendet, führt der Webserver das CGI-Programm aus. Das CGI-Programm erhält die Quelle der Seite dieses Eintrags, wandelt sie in HTML um und gibt das Ergebnis aus. Der Webserver empfängt die Ausgabe des CGI-Programms und gibt sie an den Benutzeragenten zurück. Wenn dann der Benutzeragent die Bearbeitungsfunktion aufruft, indem er auf die Schaltfläche "Seite bearbeiten" klickt, zeigt das CGI-Programm einen HTML-Textbereich oder eine andere Bearbeitungssteuerung mit den Inhalten der Seite. Wenn der Benutzeragent schließlich auf die Schaltfläche "Seite veröffentlichen" klickt, konvertiert das CGI-Programm den aktualisierten HTML-Code in die Quelle der Seite dieses Eintrags und speichert ihn.



## Verweise

* [Common Gateway Interface – von Wikipedia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

