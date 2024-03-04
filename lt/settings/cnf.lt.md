{
  "date": "2023-03-22",
  "keywords": [
"cnf failą",
"kas yra cnf failas",
"kaip atidaryti cnf failą",
"failą",
"cnf failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CNF failo formatas – „MySQL“ konfigūracijos failas",
  "description": "Sužinokite apie CNF formatą ir API, kurios gali kurti ir atidaryti CNF failus.",
  "linktitle": "CNF",
  "menu": {
    "docs": {
      "identifier": "settings-cnf-lt",
      "parent": "settings"
}
},
  "lastmod": "2023-03-22"
}

## Kas yra CNF failas?

CNF failas (taip pat žinomas kaip konfigūracijos failas) MySQL naudojamas MySQL serverio konfigūracijos parametrams saugoti. CNF failo vieta gali skirtis priklausomai nuo operacinės sistemos ir naudojamo diegimo metodo. Konfigūracija paprastai apima įvairius nustatymus, pvz., numatytąją simbolių kodavimą, skirtąjį laiką, talpyklos ir buferio konfigūracijas, kurias galima koreguoti, kad būtų optimizuotas duomenų bazės našumas, atsižvelgiant į naudojimą.

## CNF failo formatas – daugiau informacijos

Galite sukurti CNF naudodami šiuos veiksmus MySQL:

1. Atidarykite teksto rengyklę, pvz., Notepad, ir sukurkite naują failą.
2. Pridėkite norimas konfigūracijos parinktis prie failo, po vieną eilutėje. Štai pavyzdys:

```
[mysqld]
datadir=/var/lib/mysql
socket=/var/lib/mysql/mysql.sock
user=mysql
symbolic-links=0

[client]
user=root
password=password123
```

3. Išsaugokite failą su .cnf plėtiniu, pavyzdžiui, mysql.cnf.
4. Perkelkite failą į atitinkamą katalogą. Pavyzdžiui, Linux sistemose katalogas gali būti /etc/mysql/conf.d/ arba /etc/mysql/.
5. Iš naujo paleiskite MySQL serverį, kad įsigaliotų nauji konfigūracijos nustatymai.

Būtinai patikrinkite visus CNF failo pakeitimus, atliktus ne gamybinėje aplinkoje, prieš įdiegdami juos gamybinėje aplinkoje.

## Kaip atidaryti CNF failą?

CNF failas yra tekstinis failas, kurį galima lengvai atidaryti naudojant bet kurį teksto rengyklę, pvz., Notepad. Taip pat galite jį atidaryti dešiniuoju pelės mygtuku spustelėdami ir meniu pasirinkę Atidaryti naudojant. Kai failas bus atidarytas, galite redaguoti konfigūracijos nustatymus, jei reikia. CNF yra įvairių nustatymų, susijusių su MySQL serveriu, pvz., prievado numerį, registravimo parinktis ir buferio dydžius. Pataisę nustatymus, išsaugokite pakeitimus ir uždarykite teksto rengyklę. Galiausiai iš naujo paleiskite MySQL serverį, kad pakeitimai įsigaliotų.

Atkreipkite dėmesį, kad svarbu būti atsargiems redaguojant MySQL konfigūracijos failą, nes dėl neteisingų nustatymų serveris gali elgtis nenuspėjamai arba iš viso nepasileisti. Prieš atliekant bet kokius pakeitimus rekomenduojama pasidaryti originalaus failo atsarginę kopiją, kad prireikus galėtumėte ją atkurti.

## Nuorodos
* [MySQL](https://en.wikipedia.org/wiki/MySQL)


