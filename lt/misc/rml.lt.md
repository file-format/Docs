{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "RML – eliksyro ataskaitos šablono failas",
  "description":"Sužinokite apie RML failą ir API, kurios gali kurti ir atidaryti RML failus.",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml-lt",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Kas yra RML failas?

RML failas yra ataskaitų šablono failas su [Elixir Repertoire](https://elixirtech.com/repertoire-2/) ataskaitų teikimo varikliu. Šablono failas naudojamas ataskaitoms generuoti su duomenų šaltiniu, prijungtu prie Elixir FileSystem. Duomenys nuskaitomi ir užpildomi RML šablono faile ir gali būti eksportuojami į įvairius failų formatus, pvz., [PDF](/pdf/), [RTF](/word-processing/rtf/) ir skaičiuoklę [XLS](/spreadsheet/xls/). Elixir Repertuaro ataskaitų teikimo variklis gali būti prijungtas prie įvairių JDBC duomenų šaltinių.

## RML failo formatas

RML failo formato vidinės failų struktūros detalės nėra viešai prieinamos. Failus sukuria ir išsaugo viduje Elixir Repertuaro programa, kad būtų sukurtos ataskaitos su duomenimis, užpildytais iš prijungtų duomenų šaltinių. RML šablono faile yra bendra galutinės ataskaitos, kuri turi būti sugeneruota iš duomenų, išdėstymo ir vietos rezervavimo ženklų informacija.

## Kaip sukurti RML šablono failą?

Norint sugeneruoti RML šabloną Elixir Repertuare, galima atlikti šiuos veiksmus.

1. Prijunkite JDBC duomenų šaltinį prie failų sistemos.
1. Paleiskite ataskaitos šablono vedlį
1. Naudokite programinę įrangą, kad surastumėte duomenų šaltinio .ds failą
1. Pasirinkite lentelių ataskaitą kaip eksporto pasirinkimą
1. Pasirinkite laukus, kuriuos norite įtraukti į ataskaitos šabloną
1. Galiausiai, spustelėjus mygtuką Baigti, First report.rml pridedamas prie saugyklos ir atidaromas, kad būtų rodomas skirtukas Maketas.

## Nuorodos

* [Eliksyro repertuaras](https://elixirtech.com/repertoire-2/)


