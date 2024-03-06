{
  "date": "2021-05-24",
  "keywords": [
"rjs",
"Fails",
"Pagarinājums",
"Faila formāts",
"Faila paplašinājums",
"RJS",
"Ruby Javascript fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RJS — Ruby Javascript fails",
  "description": "Uzziniet, kas ir RJS faila formāts un API, kas var izveidot un atvērt RJS failus.",
  "linktitle": "RJS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-RJ-lvS"
}
},
  "lastmod": "2021-05-24"
}

## Kas ir RJS fails?

Fails ar paplašinājumu .rjs ir Ruby koda un JavasScript kombinācija, kas ļauj Rails izstrādātājiem izmantot Ruby, lai izveidotu dinamisku JavaScript kodu. Rubīna kods ir iegults Java funkcijās un tiek apkopots tīmekļa serverī, lai serverī darbotos Ruby dzinējs. RJS ir līdzīgs [RHTML](/web/rhtml/); vienīgā atšķirība ir tā, ka sānu daļā ir Ruby kods [HTML](/web/html/), bet tajā ir Ruby kods Javascript funkcijās.

## RJS faila formāts

RJS faili ir kodēti vienkāršā tekstā tāpat kā jebkura cita skriptu vai programmēšanas valoda. Kad klients pieprasa šādu lapu, Ruby kods tiek izpildīts serverī, un klienta pārlūkprogrammā tiek atgriezts tikai HTML un Javascript kods. RJS faila sintakse ir līdzīga Ruby un JavaScript sintakses kombinācijai, tādējādi JavaScript funkcijās ir iegults tikai Ruby kods.

### RJS piemērs

Nākamajā piemērā ir parādīts vienkāršs Ruby kods neatkarīgi un pēc tam iegults JavaScript funkcijā.

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
un tālāk ir RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## Atsauces

* [RJS](https://github.com/makevoid/rjs)


