{
  "date" : "2021-04-21",
  "keywords" :[ "ärtfil", "ärtfilformat", "vad är en ärtfil", "fil", "ärtexempel", "ärtfiltillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEA - PeaZip Archive File Format",
  "description":"Läs mer om PEA-filformat och API:er som kan skapa och öppna PEA-filer.",
  "linktitle" : "PEA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-21"
}

## Vad är PEA fil?

En fil med filtillägget .pea, akronym för Pack, Encrypt och Authenticate, är ett [zip](/sv/compression/zip/)-arkiv skapat med [PeaZip](https://peazip.github.io/) arkiveringsprogram. Den har komprimering och utmatning av flera volymer, och erbjuder en flexibel säkerhetsmodell genom autentiserad kryptering och kryptografi. Detta ger både integritet och autentisering av data. PeaZip-verktyget är tillgängligt som öppen källkodsmotor som kan kompileras för olika operativsystem enligt kraven.

## PEA filformat

[PEA filformatspecifikationer](https://peazip.github.io/pea_help.pdf) är allmänt tillgängliga för utvecklarens referens. PEA-arkiv är binära filer med flexibel säkerhetsmodell och redundanta integritetskontroller som sträcker sig från kontrollsummor till kryptografiskt starka hash. Detta definierar tre olika nivåer av kommunikation att kontrollera:

* Strömmar - den faktiska utdataströmmen som bildas av flera indatafiler och kan skrivas till flera utdatavolymer
* Objekt - indatafiler och mappar skickade till .pea-arkivet
* Volymer - utdataarkivfil som kan spännas till användardefinierad storlek

Var och en av dessa är valfria och kan integreras enligt användarens krav. PEA-filformatet kan lagra en enda ström som innehåller ett obegränsat antal objekt. Varje ström är upp till 2^64 byte stor.

PEA-filer erbjuder valfri integritetskontroll och autentiserad kryptering med AES i EAX- eller HMAC-läge, alternativt Twofish och Serpent i EAX-läge.

### PEA Arkiv Header

Arkivhuvudet är 10 byte och är strukturerat enligt följande.

|Byte|Beskrivning|
---|---|
|1 | Magiskt bytefält för disambiguation av filformat: $EA|
|1 | Versionsnummer|
|1 | Revisionsnummer|
|1 | Volymkontrollschema|
|1 | Deklarerar operativsystemet där strömmen byggdes|
|1 | Deklarerar OS datum- och tidskodning|
|1 | Deklarerar objektnamn teckenkodning|
|1 | Deklarerar CPU-typ (kodad i 7 bitar) och endianness (i msb)|
|1 | Reserverad för framtida bruk|

## Referenser

* [PEA filformatspecifikationer](https://peazip.github.io/pea_help.pdf)
* [PEA-filformat](https://peazip.github.io/pea-file-format.html#.pea_specifications)

