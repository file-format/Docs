{
  "date": "2022-04-07",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HAML faila formāts — Haml avota koda fails",
  "description": "Uzziniet par HAML faila formātu un API, kas var izveidot un atvērt HAML failu.",
  "linktitle": "HAML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ham-lvl"
}
},
  "lastmod": "2022-04-07"
}

## Kas ir HAML fails?

HAML fails ir HTML abstrakcijas iezīmēšanas valodas fails, kas satur avota kodu, kas rakstīts [Haml](https://haml.info/) valodā. To var izmantot kā ERB (Ruby template skriptu) aizstājēju. HAML fails satur veidnes avota kodu, kas paredzēts tīmekļa dokumenta HTML ģenerēšanai. ERB failus var aizstāt, vienkārši aizstājot šos failus lietotņu/skatu mapē uz Haml, mainot faila paplašinājumu. HAML failus var atvērt ar jebkuru teksta redaktoru, piemēram, Microsoft Notepad, Notepad++, Apple TextEdit,

## HAML faila formāts

HAML faili ir avota faili, kas saglabāti diskā kā teksta faili. Tajā ir kods, kas rakstīts HAML sintaksē. HAML aizstāj tagus **<>** ar zīmi **%**, lai padarītu kodu vienkāršāku un vienkāršāku. ERB failus var aizstāt ar HAML, kā parādīts šajā vienkāršajā piemērā.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### HAML piemērs

Tālāk ir sniegts HAML piemērs Hello World.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
kas tiek renderēts uz šādu HTML izvadi.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Atsauces

* [HAML — Github](https://github.com/haml/haml)


