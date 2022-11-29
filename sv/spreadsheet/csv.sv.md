{
  "date" : "2019-12-10",
  "keywords" :[ "CSV", "fil", "tillägg", "filformat", "kommaseparerade värden", "kalkylblad" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om CSV-filformat och API:er som kan skapa och öppna CSV-filer.",
  "title" :"CSV-filformat",
  "linktitle" : "CSV",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Vad är en CSV-fil?

Filer med tillägget .csv (Comma Separated Values) representerar vanliga textfiler som innehåller dataposter med kommaseparerade värden. Varje rad i en CSV-fil är en ny post från den uppsättning poster som finns i filen. Sådana filer genereras när dataöverföring är avsedd från ett lagringssystem till ett annat. Eftersom alla applikationer kan känna igen poster separerade med kommatecken, görs import av sådana datafiler till databasen mycket bekvämt. Nästan alla kalkylbladsprogram som Microsoft Excel eller OpenOffice Calc kan importera CSV utan större ansträngning. Data som importeras från sådana filer är ordnade i celler i ett kalkylblad för representation för användaren.

## Kortfattad bakgrund ##

Följande är några snabba fakta om ursprunget och historien för CSV-filformat.

* 1972 - IBM Fortran (nivå H utökad) kompilator stödde dem under OS/360

* 1978 - Listriktad input/output stöddes av FORTRAN 77 som använde kommatecken och blanksteg för avgränsare

* 2005 - CSV standardiserades med [RFC4180](https://tools.ietf.org/html/rfc4180) som en MIME-innehållstyp.

* 2013 - RFC4180:s brister hanterades av en W3C-rekommendation

* 2015 - W3C gjorde de första utkasten till rekommendationer för CSV-metadatastandarder, som började som rekommendation i december 2015

## Konvertera CSV-filer ##

CSV-filer kan konverteras till flera olika filformat med de program som kan öppna dessa filer. Till exempel kan Microsoft Excel importera data från CSV-filformat och spara dem till XLS, [XLSX](/sv/spreadsheet/xlsx/), [PDF](/sv/pdf/), [TXT](/sv/ordbehandling/txt/) , XML och [HTML](/sv/web/html/) filformat. På liknande sätt ger andra stationära tjänster såväl som onlinetjänster möjlighet att exportera CSV-filer till HTML, ODS och [RTF](/sv/ordbehandling/rtf/).

## CSV-filformat ##

CSV-filformatet är känt för att specificeras under [RFC4180](https://tools.ietf.org/html/rfc4180). Den definierar vilken fil som helst som CSV-kompatibel om:

* Varje post är placerad på en separat rad, avgränsad av en radbrytning (CRLF). Till exempel:
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx CRLF
* Den sista posten i filen kan ha en slutradbrytning eller inte. Till exempel:
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx
* Det kan finnas en valfri rubrikrad som visas som den första raden i filen med samma format som vanliga postrader. Denna rubrik kommer att innehålla namn som motsvarar fälten i filen och bör innehålla samma antal fält som posterna i resten av filen (närvaro eller frånvaro av rubrikraden ska indikeras via den valfria "header"-parametern i denna MIME-typ). Till exempel:
* fältnamn, fältnamn, fältnamn CRLF
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx CRLF
* Inom rubriken och varje post kan det finnas ett eller flera fält, separerade med kommatecken. Varje rad ska innehålla samma antal fält i hela filen. Utrymmen anses vara en del av ett fält och bör inte ignoreras. Det sista fältet i posten får inte följas av ett kommatecken. Till exempel:
* aaa,bbb,ccc
* Varje fält kan eller får inte omges av dubbla citattecken (men vissa program, som Microsoft Excel, använder inte dubbla citattecken alls). Om fält inte omges av dubbla citattecken, kanske dubbla citattecken inte visas i fälten. Till exempel:\
* "aaa","bbb","ccc" CRLF
* zzz,yyy,xxx
* Fält som innehåller radbrytningar (CRLF), dubbla citattecken och kommatecken ska omges av dubbla citattecken. Till exempel:
* "aaa","b CRLF
* bb","ccc" CRLF
* zzz,yyy,xxx
* Om dubbla citattecken används för att omsluta fält, måste ett dubbelcitattecken som förekommer i ett fält undvikas genom att föregå det med ett annat citattecken. Till exempel:
* "aaa","b""bb","ccc"

Men i ljuset av modern användning är avgränsaren inte begränsad till endast kommatecken och kan också vara semikolon, tabb eller mellanslag. Applikationer som Microsoft Excel ger möjlighet att ange avgränsningstecknet för import av poster från en CSV-fil.

## Referenser

* [RFC 4180](https://tools.ietf.org/html/rfc4180)
* [RFC 2048](https://tools.ietf.org/html/rfc2048)
* [CSV - Wikipedia](https://en.wikipedia.org/wiki/Comma-separated_values)

