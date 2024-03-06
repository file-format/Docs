{
  "date": "2019-10-11",
  "keywords": [
"mhtml",
"mhtml failu",
"mhtml faila formātā",
"mhtml faila tips",
"failu",
"veids",
"kas ir mhtml fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MHTML — MIME HTML fails",
  "description": "Uzziniet par MHTML faila formātu un API, kas var izveidot un atvērt MHTML failus.",
  "linktitle": "MHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-mhtm-lvl"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir MHTML fails?

Faili ar MHTML paplašinājumu ir tīmekļa lapu arhīva formāts, ko var izveidot ar vairākām dažādām lietojumprogrammām. Formāts ir pazīstams kā arhīva formāts, jo tas saglabā tīmekļa **[HTML](/web/html/)** kodu un saistītos resursus vienā failā. Šie resursi ietver visu, kas saistīts ar tīmekļa lapu, piemēram, attēlus, sīklietotnes, animācijas, audio failus un tā tālāk. MHTML failus var atvērt dažādās lietojumprogrammās, piemēram, Internet Explorer un Microsoft Word. Microsoft Windows izmanto MHTML faila formātu, lai ierakstītu tādu problēmu scenārijus, kas novērotas, lietojot jebkuru lietojumprogrammu sistēmā Windows, kas rada problēmas. MHTML faila formāts kodē lapas saturu līdzīgi specifikācijām, kas noteiktas ziņojumā/rfc822, kas ir ar vienkārša teksta e-pastu saistītās specifikācijas. Faktiskās formāta specifikācijas ir norādītas vietnē [RFC 2557](https://tools.ietf.org/html/rfc2557).

## MHTML faila formāts

MHTML ir pazīstams arī kā MIME apkopoto HTML dokumentu iekapsulēšana, jo tā spēj kodēt HTML tīmekļa lapas kopā ar tā resursiem vienā tīmekļa arhīvā. Saskaņā ar RFC 2557 specifikācijām apkopotais dokuments ir MIME kodēts ziņojums, kas satur saknes resursu (objektu), kā arī citus resursus, kas ar to saistīti, izmantojot URI. Šādi citi resursi var būt iekļauti attēli, stila lapas, sīklietotnes utt. Turklāt tie var būt citu multivides dokumentu saknes. Pilnas dokumenta specifikācijas MHTML faila formātam ir norādītas [RFC 2557](https://tools.ietf.org/html/rfc2557), un tās ir jāatsaucas uz jebkāda veida lietojumprogrammu izstrādi šī faila formāta lasīšanai/rakstīšanai. Standarts nosaka, ka ķermeņa daļas, uz kurām jāatsaucas, var identificēt vai nu pēc Content-ID, vai pēc satura atrašanās vietas.

### MIME satura galvenes

MIME satura galvene Content-Location ir definēta, lai atrisinātu URI atsauces uz resursiem citās ķermeņa daļās. Šī galvene var būt jebkura ziņojuma vai satura virsrakstā.

### Satura atrašanās vietas galvene

Satura atrašanās vieta ir URI attēlojums, kas iezīmē tās ķermeņa daļas saturu, kurā tā ir novietota. Tā vērtība var būt absolūts vai relatīvs URI. To var izmantot, lai iezīmētu resursu, ko daži vai visi ziņojuma saņēmēji nevar izgūt. Vienam ziņojumam var būt tikai viena Content-Location galvene. Vairāku daļu/saistītas struktūras piemērs, kurā ir ķermeņa daļas ar satura atrašanās vietas un satura ID iezīmēm:

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

### MHTML apkopojumu URI

MHTML apkopojuma URI atšķiras no tā saknes URI. Satura atrašanās vietas galvenes lauks ir jāpiemēro visam apkopojumam, ja tas tiek izmantots vairāku daļu/saistītas virsraksta virsrakstā. Tāpat izgūto resursu kopa var atšķirties no resursu kopas, kas izgūta, izmantojot tās daļu satura atrašanās vietas, ja šī apkopojuma izgūšanai tiek izmantots URI, kas attiecas uz MHTML apkopojumu. Piemēram, MHTML apkopojuma izgūšana var atgriezt veco versiju, savukārt saknes URI un ar to saistītos objektus var atgriezt jaunāku versiju.

## Atsauces

* [Apkopoto dokumentu MIME iekapsulēšana — RFC 2557](https://tools.ietf.org/html/rfc2557)

* [MHTML faila formāts — Wikipedia](https://en.wikipedia.org/wiki/MHTML)


