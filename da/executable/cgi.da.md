{
  "date": "2021-06-28",
  "keywords": [
"cgi fil",
"hvad er en cgi-fil",
"fil",
"cgi eksempel",
"cgi filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om CGI-filformat og API'er, der kan oprette og åbne CGI-filer.",
  "title": "CGI - Common Gateway Interface Script File",
  "linktitle": "CGI",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-cg-dai"
}
},
  "lastmod": "2021-06-28"
}

## Hvad er en CGI fil?
En CGI-fil er kendt som et Common Gateway Interface-script, der bruges af en webserver til at køre et eksternt program til at behandle brugeranmodninger. Scriptet, der er gemt i en fil med filtypenavnet .cgi, er typisk skrevet i programmeringssprogene C eller Perl. Det var blevet introduceret siden internettets tidlige dage, hvor webudviklere ønskede at forbinde databaser med deres webservere. En server, som understøttede en fælles gateway mellem webserver og databaser, var velegnet til at udføre CGI-koden.

## CGI filformat
CGI-scripts bruges af webserveren for at gøre det lettere for ejeren at konfigurere, hvordan en URL skal håndteres. Proceduren udføres normalt ved at markere en ny mappe (hvor dokumenterne hovedsageligt er placeret) som indeholdende CGI-scripts; dets almindeligt kendte navn er cgi-bin. For eksempel kan /usr/local/apache/htdocs/cgi-bin vælges som en CGI-mappe på webserveren. Når en webbrowser anmoder om en URL, der peger på en fil i CGI-biblioteket, så, i stedet for blot at sende den fil (/usr/local/apache/htdocs/cgi-bin/printenv.pl) til webbrowseren, vil HTTP serveren udfører det angivne script og returnerer outputtet af scriptet til webbrowseren. Kort sagt, alt, som CGI-scriptet sendes til standardoutput, overføres til webklienten i stedet for at blive vist i en terminal i vinduet.

### CGI-eksempel

Følgende CGI-script skrevet i Perl, som viser alle miljøvariabler, der sendes af webserveren:
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

Outputtet vil være som følgende:
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
## Brug af CGI-scripts
CGI-filerne, der indeholder CGI-scripts, bruges normalt til at behandle inputdata fra brugeren og producere de relevante outputdata. Implementering af en wiki er et af eksemplerne på CGI-program. Hvis brugeragenten sender en anmodning om navnet på en post, kører webserveren CGI-programmet. CGI-programmet henter kilden til denne posts side, konverterer den til HTML og udskriver resultatet. Webserveren modtager outputtet fra CGI-programmet og returnerer det til brugeragenten. Så, hvis brugeragenten kalder redigeringsfunktionen ved at klikke på knappen Rediger side, viser CGI-programmet et HTML-tekstområde eller en anden redigeringskontrol med sidens indhold. Til sidst, hvis brugeragenten klikker på knappen Udgiv side, konverterer CGI-programmet den opdaterede HTML til kilden til den pågældende posts side og gemmer den.



## Referencer 

* [Common Gateway Interface - af Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)


