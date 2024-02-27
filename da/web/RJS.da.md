{
  "date": "2021-05-24",
  "keywords": [
"rjs",
"Fil",
"Udvidelse",
"Filformat",
"Filudvidelse",
"RJS",
"Ruby Javascript-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RJS - Ruby Javascript-fil",
  "description": "Lær om, hvad RJS filformat og API'er er, der kan oprette og åbne RJS filer.",
  "linktitle": "RJS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-RJ-daS"
}
},
  "lastmod": "2021-05-24"
}

## Hvad er en RJS fil?

En fil med filtypenavnet .rjs er en kombination af Ruby-kode og Javascript, der tillader Rails-udviklere at bruge Ruby til at producere dynamisk JavaScript-kode. Ruby-kode er indlejret i Java-funktioner og er kompileret på webserveren, der kræver, at Ruby engine skal køre på serveren. RJS ligner [RHTML](/web/rhtml/); den eneste forskel er, at lateralen indeholder Ruby-kode i [HTML](/web/html/), mens den indeholder Ruby-kode i Javascript-funktioner.

## RJS filformat

RJS-filer er kodet i almindelig tekst som ethvert andet script- eller programmeringssprog. Når en sådan side anmodes af klienten, udføres Ruby-koden på serveren, og kun HTML- og Javascript-kode returneres til klientens browser. Syntaksen for RJS-filen ligner syntaksen for kombination af Ruby og JavaScript-syntaks, således at kun Ruby-koden er indlejret i JavaScript-funktioner.

### RJS-eksempel

Følgende eksempel viser en simpel Ruby-kode uafhængigt og derefter indlejret i en JavaScript-funktion.

```Ruby
### Default Ruby Functions

def foo
  "bar"
end
```

```JavaScript
# JS style which looks like JS

foo = -> { return "bar" }
```
og følgende er RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## Referencer

* [RJS](https://github.com/makevoid/rjs)


