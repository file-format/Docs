{
  "date" : "2021-06-28",
  "keywords" :[ "cgi-fil", "vad är en cgi-fil", "fil", "cgi-exempel", "cgi-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om CGI-filformat och API:er som kan skapa och öppna CGI-filer.",
  "title" :"CGI - Common Gateway Interface Script File",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## Vad är en CGI fil?
En CGI-fil är känd som ett Common Gateway Interface-skript som används av en webbserver för att köra ett externt program för att behandla användarförfrågningar. Skriptet som sparas i en fil med filtillägget .cgi är vanligtvis skrivet i programmeringsspråken C eller Perl. Det hade introducerats sedan webbens tidiga dagar, när webbutvecklare ville ansluta databaser till sina webbservrar. En server som stödde en gemensam gateway mellan webbserver och databaser var väl lämpad för att exekvera CGI-koden.

## CGI filformat
CGI-skripten används av webbservern för att underlätta för ägaren att konfigurera hur en URL ska hanteras. Proceduren görs vanligtvis genom att markera en ny katalog (där dokumenten huvudsakligen finns) som innehållande CGI-skript; dess allmänt kända namn är cgi-bin. Till exempel kan /usr/local/apache/htdocs/cgi-bin väljas som en CGI-katalog på webbservern. När en webbläsare begär en URL som pekar på en fil i CGI-katalogen, istället för att bara skicka filen (/sv/usr/local/apache/htdocs/cgi-bin/printenv.pl) till webbläsaren, kommer HTTP servern kör det angivna skriptet och returnerar utdata från skriptet till webbläsaren. Kort sagt, allt som CGI-skriptet skickas till standardutdata överförs till webbklienten istället för att visas i en terminal eller fönster.

### CGI-exempel

Följande CGI-skript skrivet i Perl som visar alla miljövariabler som skickas av webbservern:
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

Utgången kommer att se ut som följande:
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
## Användning av CGI-skript
CGI-filerna som innehåller CGI-skripten används vanligtvis för att bearbeta indata från användaren och producera relevanta utdata. Att implementera en wiki är ett av exemplen på CGI-program. Om användaragenten skickar en begäran om namnet på en post, kör webbservern CGI-programmet. CGI-programmet hämtar källan till den postens sida, konverterar den till HTML och skriver ut resultatet. Webbservern tar emot utdata från CGI-programmet och returnerar det till användaragenten. Sedan, om användaragenten anropar redigeringsfunktionen genom att klicka på knappen "Redigera sida", visar CGI-programmet ett HTML-textområde eller annan redigeringskontroll med sidans innehåll. Slutligen, om användaragenten klickar på knappen "Publicera sida" konverterar CGI-programmet den uppdaterade HTML-koden till källan för den postens sida och sparar den.



## Referenser

* [Common Gateway Interface - av Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

