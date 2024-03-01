{
  "date": "2021-06-28",
  "keywords": [
"cgi tiedosto",
"mikä on cgi-tiedosto",
"tiedosto",
"cgi esimerkki",
"cgi tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi CGI-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CGI-tiedostoja.",
  "title": "CGI - Common Gateway Interface -skriptitiedosto",
  "linktitle": "CGI",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-cg-fii"
}
},
  "lastmod": "2021-06-28"
}

## Mikä on CGI-tiedosto?
CGI-tiedosto tunnetaan nimellä Common Gateway Interface -skripti, jota verkkopalvelin käyttää ulkoisen ohjelman suorittamiseen käyttäjien pyyntöjen käsittelemiseksi. Komentosarja, joka on tallennettu tiedostoon .cgi-tunnisteella, on yleensä kirjoitettu C- tai Perl-ohjelmointikielillä. Se oli otettu käyttöön Webin alkuajoista lähtien, jolloin web-kehittäjät halusivat yhdistää tietokannat Web-palvelimiinsa. Palvelin, joka tuki yhteistä yhdyskäytävää Web-palvelimen ja tietokantojen välillä, soveltui hyvin CGI-koodin suorittamiseen.

## CGI-tiedostomuoto
Web-palvelin käyttää CGI-komentosarjat helpottamaan omistajan määrittämistä, kuinka URL-osoitetta käsitellään. Toimenpide tehdään yleensä merkitsemällä uusi hakemisto (jossa asiakirjat pääasiassa sijaitsevat) sisältäväksi CGI-komentosarjat; sen yleinen nimi on cgi-bin. Esimerkiksi /usr/local/apache/htdocs/cgi-bin voidaan valita Web-palvelimen CGI-hakemistoksi. Kun verkkoselain pyytää URL-osoitetta, joka osoittaa CGI-hakemistossa olevaan tiedostoon, sen sijaan, että vain lähettäisi tiedoston (/usr/local/apache/htdocs/cgi-bin/printenv.pl) verkkoselaimeen, HTTP palvelin suorittaa määritetyn komentosarjan ja palauttaa komentosarjan tulosteen Web-selaimeen. Lyhyesti sanottuna kaikki, mitä CGI-skripti lähetetään vakiolähtöön, siirretään Web-asiakkaalle sen sijaan, että se näkyisi ikkunan päätteessä.

### CGI-esimerkki

Seuraava Perlissä kirjoitettu CGI-skripti, joka näyttää kaikki Web-palvelimen välittämät ympäristömuuttujat:
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

Tulos on seuraavanlainen:
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
## CGI-skriptien käyttö
CGI-komentosarjat sisältäviä CGI-tiedostoja käytetään yleensä käyttäjän syötetietojen käsittelyyn ja asiaankuuluvan lähtödatan tuottamiseen. Wikin käyttöönotto on yksi esimerkkejä CGI-ohjelmasta. Jos käyttäjäagentti lähettää pyynnön merkinnän nimeä varten, Web-palvelin suorittaa CGI-ohjelman. CGI-ohjelma hakee kyseisen merkinnän sivun lähteen, muuntaa sen HTML-muotoon ja tulostaa tuloksen. Web-palvelin vastaanottaa tulosteen CGI-ohjelmasta ja palauttaa sen käyttäjäagentille. Sitten, jos käyttäjäagentti kutsuu muokkaustoimintoa napsauttamalla Muokkaa sivua -painiketta, CGI-ohjelma näyttää HTML-tekstialueen tai muun muokkaussäätimen sivun sisällön kanssa. Lopuksi, jos käyttäjäagentti napsauttaa Julkaise sivu -painiketta, CGI-ohjelma muuntaa päivitetyn HTML-koodin kyseisen merkinnän sivun lähteeksi ja tallentaa sen.



## Viitteet 

* [Common Gateway Interface - Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)


