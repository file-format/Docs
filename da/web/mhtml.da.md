{
  "date": "2019-10-11",
  "keywords": [
"mhtml",
"mhtml fil",
"mhtml filformat",
"mhtml filtype",
"fil",
"type",
"hvad er en mhtml-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MHTML - MIME HTML-fil",
  "description": "Lær om MHTML-filformat og API'er, der kan oprette og åbne MHTML-filer.",
  "linktitle": "MHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-mhtm-dal"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en MHTML fil?

Filer med MHTML-udvidelse repræsenterer et websidearkivformat, der kan oprettes af en række forskellige applikationer. Formatet er kendt som arkivformat, fordi det gemmer web-**[HTML](/web/html/)**-koden og tilhørende ressourcer i en enkelt fil. Disse ressourcer inkluderer alt, der er knyttet til websiden, såsom billeder, applets, animationer, lydfiler og så videre. MHTML-filer kan åbnes i en række forskellige programmer, såsom Internet Explorer og Microsoft Word. Microsoft Windows bruger MHTML-filformat til at optage scenarier med problemer observeret under brugen af enhver applikation på Windows, der rejser problemer. MHTML-filformatet koder sideindholdet svarende til specifikationer defineret i message/rfc822, som er almindelig tekst e-mail-relaterede specifikationer. De faktiske specifikationer for formatet er som beskrevet af [RFC 2557](https://tools.ietf.org/html/rfc2557).

## MHTML filformat

MHTML er også kendt som MIME Encapsulation of Aggregate HTML-dokumenter for dets evne til at kode HTML-websider sammen med dets ressourcer til et enkelt webarkiv. I henhold til RFC 2557-specifikationerne er et samlet dokument en MIME-kodet besked, der indeholder en rodressource (objekt) samt andre ressourcer, der er knyttet til den via URI'er. Sådanne andre ressourcer kan være repræsentation af inline-billeder, typografiark, applets osv. Derudover kan disse være roden til andre multimediedokumenter. Fuldstændige dokumentspecifikationer for MHTML-filformat er som beskrevet i [RFC 2557](https://tools.ietf.org/html/rfc2557) og bør henvises til enhver form for applikationsudvikling til læsning/skrivning af dette filformat. Standarden specificerer, at de kropsdele, der skal henvises til, kan identificeres enten ved et Content-ID eller ved en Content-Location.

### MIME-indholdsoverskrifter

En MIME-indholdsoverskrift, Content-Location, er defineret til at løse URI-referencer til ressourcer i andre kropsdele. Denne overskrift kan forekomme i enhver meddelelse eller indholdsoverskrift.

### Indhold-Placering Header

En Content-Location er en repræsentation af en URI, der mærker indholdet af en kropsdel, hvor den er placeret. Dens værdi kan være en absolut eller en relativ URI. Det kan bruges til at mærke en ressource, som ikke kan hentes af nogle eller alle modtagere af en besked. En enkelt meddelelse må kun have en enkelt Content-Location-header. Eksempel på en flerdelt/relateret struktur, der indeholder kropsdele med både Content-Location og Content-ID-etiketter:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### URI'er af MHTML-aggregater

URI'en for MHTML-aggregatet er anderledes end dens rod-URI. Indholdsplacering-headerfeltet bør gælde for hele aggregatet, hvis det bruges i overskriften til en flerdelt/relateret overskrift. På samme måde kan sættet af hentede ressourcer være forskelligt fra sættet af ressourcer, der hentes ved hjælp af indholdsplaceringerne for dets dele, når URI'en, der refererer til MHTML-aggregatet, bruges til at hente dette aggregat. For eksempel kan hentning af et MHTML-aggregat returnere en gammel version, mens hentning af root-URI'en og dets in-line-linkede objekter kan returnere en nyere version.

## Referencer

* [MIME Encapsulation of Aggregate Documents - RFC 2557](https://tools.ietf.org/html/rfc2557)

* [MHTML-filformat - af Wikipedia](https://en.wikipedia.org/wiki/MHTML)


