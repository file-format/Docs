{
  "date" : "2021-06-28",
  "keywords" :[ "cgi-bestand", "wat is een cgi-bestand", "bestand", "cgi-voorbeeld", "cgi-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over de CGI-bestandsindeling en API's die CGI-bestanden kunnen maken en openen.",
  "title" :"CGI - Common Gateway Interface-scriptbestand",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## Wat is een CGI-bestand?
Een CGI-bestand staat bekend als een Common Gateway Interface-script dat door een webserver wordt gebruikt om een extern programma uit te voeren om gebruikersverzoeken te verwerken. Het script dat is opgeslagen in een bestand met de extensie .cgi is meestal geschreven in de programmeertalen C of Perl. Het was geïntroduceerd sinds de begindagen van het web, toen webontwikkelaars databases met hun webservers wilden verbinden. Een server die een gemeenschappelijke gateway tussen webserver en databases ondersteunde, was zeer geschikt om de CGI-code uit te voeren.

## CGI-bestandsindeling
De CGI-scripts worden door de webserver gebruikt om de eigenaar te helpen configureren hoe een URL wordt afgehandeld. De procedure wordt meestal gedaan door een nieuwe map (waar de documenten zich voornamelijk bevinden) te markeren als CGI-scripts; de algemeen bekende naam is cgi-bin. Bijvoorbeeld, /usr/local/apache/htdocs/cgi-bin kan worden gekozen als een CGI-directory op de webserver. Wanneer een webbrowser een URL aanvraagt die verwijst naar een bestand in de CGI-directory, dan, in plaats van dat bestand (/nl/usr/local/apache/htdocs/cgi-bin/printenv.pl) naar de webbrowser te sturen, server voert het opgegeven script uit en retourneert de uitvoer van het script naar de webbrowser. Kortom, alles wat het CGI-script naar de standaarduitvoer stuurt, wordt overgebracht naar de webclient in plaats van dat het wordt weergegeven in een terminal of venster.

### CGI-voorbeeld

Volgend CGI-script geschreven in Perl dat alle omgevingsvariabelen toont die door de webserver zijn doorgegeven:
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

De uitvoer zal als volgt zijn:
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
## Gebruik van CGI-scripts
De CGI-bestanden die de CGI-scripts bevatten, worden meestal gebruikt om invoergegevens van de gebruiker te verwerken en de relevante uitvoergegevens te produceren. Het implementeren van een wiki is een van de voorbeelden van een CGI-programma. Als de user-agent een verzoek om de naam van een item verzendt, voert de webserver het CGI-programma uit. Het CGI-programma haalt de bron van de pagina van dat item op, zet het om in HTML en drukt het resultaat af. De webserver ontvangt de uitvoer van het CGI-programma en stuurt deze terug naar de user-agent. Als de user-agent vervolgens de bewerkingsfunctie oproept door op de knop "Pagina bewerken" te klikken, toont het CGI-programma een HTML-tekstgebied of een ander bewerkingselement met de inhoud van de pagina. Ten slotte, als de user-agent op de knop "Pagina publiceren" klikt, converteert het CGI-programma de bijgewerkte HTML naar de bron van de pagina van dat item en slaat het op.



## Referenties

* [Common Gateway Interface - door Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

