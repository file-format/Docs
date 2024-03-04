{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AGI failas – Asterisk Gateway sąsajos failo formatas",
  "description":"Sužinokite, kas yra AGI failo formatas, pavyzdyje ir API, kurios gali kurti ir atidaryti AGI failus.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi-lt",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Kas yra AGI failas?

AGI failas yra scenarijaus failas, naudojamas atvirojo kodo telefonijos sistemoje Asterisk. Jame yra informacijos, kurią galima naudoti automatizuojant procesus ir Asterisk dialplan. Naudojant AGI scenarijaus failus, galima užmegzti ryšius su reliacinėmis duomenų bazėmis, tokiomis kaip PostgreSQL arba MySQL. Be to, AGI scenarijus taip pat galima naudoti norint pasiekti kitus išorinius išteklius. AGI scenarijus gali paversti rinkimo plano valdymą išoriniam AGI scenarijui, todėl Asterisk gali atlikti sudėtingas užduotis.

## AGI failo formatas – daugiau informacijos

AGI scenarijaus failai išsaugomi kaip tekstiniai failai ir gali būti atidaryti bet kuriame teksto rengyklėje, kad būtų atlikti pakeitimai.

### Standartinis AGI komunikacijos modelis

AGI scenarijus įkelia kintamuosius ir jų reikšmes, kurias jam siunčia Asterisk. Įprasta šių kintamųjų išvaizda yra tokia.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Po šių kintamųjų yra tuščia eilutė, kurią siunčia Asterisk, rodanti, kad AGI scenarijus dabar gali valdyti rinkimo planą.

### AGI scenarijaus failų programavimo kalba

AGI scenarijus paprastai galima parašyti Perl, [PHP](/programming/php/), [C](/programming/c/), Pascal arba Bourne Shell.

## Nuorodos

 * [Asterisk AGI Script](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

