{
  "date" : "2021-06-28",
  "keywords" :[ "file cgi", "cos'è un file cgi", "file", "esempio cgi", "estensione file cgi", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file CGI e le API che possono creare e aprire file CGI.",
  "title" :"CGI - File script di interfaccia gateway comune",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## Che cos'è un file CGI?
Un file CGI è noto come script Common Gateway Interface che viene utilizzato da un server Web per eseguire un programma esterno per elaborare le richieste degli utenti. Lo script salvato in un file con estensione .cgi è tipicamente scritto nei linguaggi di programmazione C o Perl. Era stato introdotto sin dai primi giorni del Web, quando gli sviluppatori Web desideravano connettere i database ai loro server Web. Un server che supportava un gateway comune tra server Web e database era adatto per eseguire il codice CGI.

## Formato file CGI
Gli script CGI vengono utilizzati dal server Web per facilitare al proprietario la configurazione della modalità di gestione di un URL. La procedura viene solitamente eseguita contrassegnando una nuova directory (dove si trovano principalmente i documenti) come contenente script CGI; il suo nome comunemente noto è cgi-bin. Ad esempio, /usr/local/apache/htdocs/cgi-bin potrebbe essere selezionato come directory CGI sul server Web. Quando un browser Web richiede un URL che punta a un file all'interno della directory CGI, invece di inviare semplicemente quel file (/it/usr/local/apache/htdocs/cgi-bin/printenv.pl) al browser Web, l'HTTP il server esegue lo script specificato e restituisce l'output dello script al browser Web. In breve, tutto ciò che lo script CGI viene inviato allo standard output viene trasferito al client Web invece di essere mostrato in un terminale di finestra.

### Esempio CGI

Segue lo script CGI scritto in Perl che mostra tutte le variabili d'ambiente passate dal server Web:
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

L'output sarà simile al seguente:
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
## Usi degli script CGI
I file CGI contenenti gli script CGI vengono solitamente utilizzati per elaborare i dati di input dell'utente e produrre i dati di output rilevanti. L'implementazione di un wiki è uno degli esempi di programma CGI. Se l'interprete invia una richiesta per il nome di una voce, il server Web esegue il programma CGI. Il programma CGI ottiene l'origine della pagina di quella voce, la converte in HTML e stampa il risultato. Il server Web riceve l'output dal programma CGI e lo restituisce allo user agent. Quindi, se l'interprete chiama la funzione di modifica facendo clic sul pulsante "Modifica pagina", il programma CGI mostra un'area di testo HTML o un altro controllo di modifica con il contenuto della pagina. Infine, se l'interprete fa clic sul pulsante "Pubblica pagina", il programma CGI converte l'HTML aggiornato nel sorgente della pagina di quella voce e lo salva.



## Riferimenti

* [Interfaccia gateway comune - di Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

