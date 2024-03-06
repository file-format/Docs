{
  "date": "2019-10-11",
  "keywords": [
"sh failu",
".sh failu",
"pagarinājumu",
"formātā",
"sh faila piemērs",
"sh faila formātā",
"kā palaist sh failu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SH — Bash Shell skripta fails",
  "description": "Uzziniet par SH faila formātu un API, kas var izveidot un atvērt SH failus.",
  "linktitle": "SH",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-s-lvh"
}
},
  "lastmod": "2021-05-21"
}

## Kas ir SH fails?

Fails ar paplašinājumu .sh ir skriptu valodas komandu fails, kurā ir datorprogramma, kas jāpalaiž Unix apvalkā. Tajā var būt vairākas komandas, kas tiek izpildītas secīgi, lai veiktu tādas darbības kā failu apstrāde, programmu izpilde un citi līdzīgi uzdevumi. Lietotājs tos izpilda no komandrindas saskarnes vai pakešu, lai vienlaikus veiktu vairākas darbības. Skriptu failus var atvērt teksta redaktoros, piemēram, Notepad, Notepad++, Vim, Apple Terminal un citās līdzīgās lietojumprogrammās operētājsistēmās Windows, MacOS un Linux OS.

## SH faila formāts

SH faili ir rakstīti vienkāršā tekstā, ievērojot definēto sintakse. Šie skriptu faili atbalsta:

 * `Komentāri` — komentāri sākas ar #, un apvalks tos ignorē.
 * Īsceļi — tos var izmantot, lai pārdēvētu komandu īsai un vienkāršai izpildei.
 * `Pakešu darbi` — var tikt automātiski izpildītas vairākas komandas, kuras pretējā gadījumā būtu jāievada manuāli. Tas novērš nepieciešamību gaidīt, līdz lietotājs aktivizēs katru secības posmu.
 * `Ģeneralizācija` - izmantojot vienkāršas cilpas, tiek panākts daudz vairāk vispārinājums tādām darbībām kā attēlu pārveidošana no viena no diska uz citu.

## SH faila piemērs

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## Kā palaist SH failu?
SH faili parasti darbojas operētājsistēmā Linux, pat operētājsistēmā Windows jums ir nepieciešams izveidot savienojumu ar Linux termināli, izmantojot programmatūru, piemēram, Putty, lai palaistu sh failus. Tālāk ir norādītas darbības, lai palaistu SH failu Linux terminālī.

1. Atveriet Linux termināli un dodieties uz direktoriju, kurā atrodas SH fails.
2. Izmantojot komandu chmod, iestatiet skripta izpildes atļauju (ja tā vēl nav iestatīta).
3. Palaidiet skriptu, izmantojot vienu no tālāk norādītajām darbībām
	1. `./faila nosaukums.sh`
	2.  `sh faila nosaukums.sh`
	3.  `bash script-name-here.sh`

## Atsauces

* [Bashscripting for Beginners](https://help.ubuntu.com/community/Beginners/BashScripting)

* [Shellscript](https://www.shellscript.sh/)


