{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AWK faila formāts — AWK skripta fails",
  "description":"Uzziniet par AWK faila formātu un API, kas var izveidot un atvērt AWK failus.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk-lv",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Kas ir AWK fails?

AWK fails ir skripta fails, kas izveidots teksta apstrādes lietojumprogrammai **AWK**, kas ir komplektā ar Unix un Linux operētājsistēmām. Tajā ir loģiski norādījumi, kā veikt darbības ar tekstu vai faila saturu, piemēram, teksta saskaņošanu, aizstāšanu un drukāšanu. Tas palīdz ģenerēt atskaites un formatētu tekstu no ievades faila. Utilīta awk parasti atrodas mapē /usr/bin/awk lielākajā daļā Linux/unix izplatījumu.

## Kā izveidot AWK skriptu?

AWK failu var izveidot vai atvērt jebkurā teksta redaktorā operētājsistēmā Linux/Unix OS. Jaunu AWK skripta failu var izveidot šādi.

```
$ vi script.awk
```

Tas atvērs AWK failu teksta redaktorā. Ievadiet dažus paziņojumus teksta redaktorā, kā norādīts tālāk.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
Šī teksta satura pirmā rindiņa ir izskaidrota šādi.

 * \#! – saukts par Shebang, kas norāda skripta instrukciju tulku
 * /usr/bin/awk – ir tulks
 * -f – tulka opcija, ko izmanto programmas faila lasīšanai

## Kā izpildīt AWK skriptu?

Saglabājiet failu un padariet skriptu izpildāmu, izdodot tālāk norādīto komandu:
```
$ chmod +x script.awk
```

Pēc tam skriptu var palaist šādi.

```
$ ./script.awk
```

kā rezultātā tiek iegūta šāda izvade.

```
Writing my first Awk executable script!
```

## Atsauce Nr.

* [Skriptu rakstīšana, izmantojot Awk programmēšanas valodu](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)


