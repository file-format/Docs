{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTACCESS-Datei - Apache HTACCESS-Dateiformat",
  "description" :"Ihr Dateiformat-Leitfaden, um zu erfahren, was eine HTACCESS-Datei ist",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine HTACCESS-Datei?

Eine HTACCESS-Datei ist eine Apache-Konfigurationsdatei, die einen Mechanismus bereitstellt, um Konfigurationsänderungen für verschiedene Ordner/Verzeichnisse einer Website zuzulassen. Es enthält Konfigurationsanweisungen, die auf das Verzeichnis und Unterverzeichnisse anwendbar sind.

Eine HTACCESS-Datei führt eine Reihe von Überprüfungen durch, z. B. das Definieren der Indexseite einer Website, das Auflisten der 404-Fehlerseite (Seite nicht gefunden), das Ausführen der 301- oder 302-Seitenumleitungen, das Blockieren des Zugriffs von einer bestimmten IP-Adresse oder anderen Websites. Die Verwendung von .htaccess-Dateien verlangsamt daher die Gesamtleistung Ihres Apache HTTP-Servers.

## HTACCESS-Dateiformat

HTACCESS-Dateien werden im Nur-Text-Dateiformat auf der Disc gespeichert. Das bedeutet, dass Sie diese Dateien in jedem Texteditor öffnen und bearbeiten können. Es gibt keinen Namen vor dem "." in einer .htaccess-Datei, die zeigt, dass es sich um eine versteckte Datei im Ordner handelt.

## Allgemeine Verwendung einer HTACCESS-Datei

Fünf häufige Verwendungen einer HTACCESS-Datei sind wie folgt.

### Mod_Rewrite

Eine HTACCESS-Datei kann verwendet werden, um festzulegen und zu ändern, wie URLs und Webseiten auf einer Website den Benutzern angezeigt werden.

### Authentifizierung

Die Authentifizierung kann mit .htaccess erreicht werden, indem eine Passowrd-Datei namens .htpasswd erstellt wird. Auf diese Weise können die Website-Besucher ein Passwort angeben, wenn sie einen bestimmten Abschnitt der Webseite besuchen möchten.

### Benutzerdefinierte Fehlerseiten

Sie können benutzerdefinierte Fehlerseiten wie 400 Bad Request, 401 Authorization Required, 403 Forbidden Page, 404 File not Found und 500 Internal Error with .htaccess file erstellen. Diese verlangsamen jedoch die Leistung des Servers, da alle diese Prüfungen ausgeführt werden, wenn auf die Seiten zugegriffen wird.

### MIME-Typen

Apache HTACCESS-Dateien können so geändert werden, dass sie MIME-Typen (Multipurpose Internet Mail Extensions) enthalten. Dadurch kann Ihr Server die Bereitstellung von Anwendungsdateien unterstützen, die von der Site nicht unterstützt wurden.

###SSI

Server Side Includes (SSI) sind eine große Zeitersparnis auf einer Website. SSI kann durch Einfügen des folgenden Codes in Ihre .htaccess-Datei aktiviert werden.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Beispiel einer Apache HTACCESS-Datei

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## Verweise

* [Apache HTTP Server Tutorial: .htaccess-Dateien](https://httpd.apache.org/docs/current/howto/htaccess.html)

