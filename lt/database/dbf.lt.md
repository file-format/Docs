{
  "date": "2021-06-15",
  "keywords": [
"DBF",
"pratęsimas",
"dbf failą",
"dbf failo formatas",
"Duomenų bazės failo tipas",
"Duomenų bazės failo formatas",
"kas yra dbf failas",
"dBASE"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie DBF failo formatą ir API, kurios gali kurti ir atidaryti DBF failus.",
  "title": "DBF – dBase duomenų bazės failas",
  "linktitle": "DBF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-db-ltf"
}
},
  "lastmod": "2021-06-15"
}

## Kas yra DBF failas?
The file with .dbf extension is a database file used by a database management system application called **dBASE**. Inititally, the dBASE database was named as Project Vulcan; started by **Wayne Ratliff** in 1978. DBF failo tipas buvo pristatytas su dBASE II 1983 m. Jis sutvarko kelis duomenų įrašus su masyvo tipo laukais. **xBase** duomenų bazės programinė įranga, kuri yra populiari dėl suderinamumo su daugybe failų formatų; taip pat palaiko DBF failus.

## DBF failo formatas
DBF failo formatas priklauso dBASE duomenų bazių valdymo sistemai, tačiau jis gali būti suderinamas su xBase ar kita DBVS programine įranga. Pradinė dbf failo versija buvo sudaryta iš paprastos lentelės, kurioje duomenys galėjo būti pridėti, modifikuoti, ištrinti arba atspausdinti naudojant ASCII simbolių rinkinį. Laikui bėgant .dbf buvo patobulintas ir buvo pridėta papildomų failų, siekiant padidinti duomenų bazių sistemos funkcijas ir galimybes.

Šiuolaikinėje dBASE DBF failą sudaro antraštė, duomenų įrašai ir EOF (failo pabaigos) žymeklis.

- Antraštėje pateikiama informacija apie failą, pvz., įrašų skaičius ir įrašuose naudojamų laukų tipų skaičius.
- Įrašuose yra faktiniai duomenys.
- Failo pabaiga pažymėta vienu baitu, kurio reikšmė yra 0x1A.

### Failo antraštė
Failo antraštės išdėstymas dBase pateiktas šioje lentelėje:

| Baitas | Turinys | Reikšmė |
---|---|---|
| 0 | 1 baitas | Galiojantis dBASE DOS failui; bitai 0–2 nurodo versijos numerį, 3 bitai rodo, kad yra DOS atmintinės failo dBASE, 4–6 bitai nurodo SQL lentelės buvimą, 7 bitai nurodo bet kokio atmintinės failo buvimą (arba dBASE m PLUS, arba dBASE DOS) |
| 1–3 | 3 baitai | Paskutinio atnaujinimo data; suformatuotas kaip YYMMDD |
| 4–7 | 32 bitų numeris | Įrašų skaičius duomenų bazės faile |
| 8–9 | 16 bitų numeris | Baitų skaičius antraštėje |
| 10–11 | 16 bitų numeris | Įrašo baitų skaičius |
| 12–13 | 2 baitai | Rezervuota; užpildyti 0 |
| 14 | 1 baitas | Žyma, nurodanti nebaigtą operaciją[1 pastaba] |
| 15 | 1 baitas | Šifravimo žyma[2 pastaba] |
| 16–27 | 12 baitų | Rezervuota dBASE, skirta DOS kelių vartotojų aplinkoje |
| 28 | 1 baitas | Gamybos .mdx failo vėliavėlė; 1, jei yra gamybos .mdx failas, 0, jei nėra |
| 29 | 1 baitas | Kalbos vairuotojo ID |
| 30–31 | 2 baitai | Rezervuota; užpildyti 0 |
| 32–n [3 pastaba][4 pastaba] | po 32 baitus | lauko deskriptorių masyvas (dėl deskriptorių išdėstymo žr. toliau) |
| n + 1 | 1 baitas | 0x0D kaip lauko deskriptoriaus masyvo terminatorius |

- Funkcija ISMARKEDO patikrina šią žymą (OPERACIJOS PRADĖJIMAS nustato ją į 1, END TRANSACTION ir ROLLBACK nustato 0).
- Jei ši vėliavėlė nustatyta į 1, pasirodo pranešimas Duomenų bazė užšifruota.
- Maksimalus laukelių skaičius yra 255.
- n reiškia paskutinį lauko deskriptorių masyvo baitą.

### Lauko deskriptorių masyvas
Lauko aprašų išdėstymas dBASE:

| Baitas | Turinys | Reikšmė |
---|---|---|
| 0–10 | 11 baitų | Lauko pavadinimas ASCII formatu (užpildytas nulis) |
| 11 | 1 baitas | Lauko tipas. Leidžiamos reikšmės: C, D, F, L, M arba N (reikšmes rasite kitoje lentelėje) |
| 12–15 | 4 baitai | Rezervuota |
| 16 | 1 baitas | Lauko ilgis dvejetainiu formatu (maksimalus 254 (0xFE)). |
| 17 | 1 baitas | Laukų dešimtainis skaičius dvejetainiais |
| 18–19 | 2 baitai | Darbo zonos ID |
| 20 | 1 baitas | Pavyzdys |
| 21–30 | 10 baitų | Rezervuota |
| 31 | 1 baitas | Gamybos MDX lauko vėliavėlė; 1, jei lauke yra indekso žyma gamybos MDX faile, 0, jei ne |

### Duomenų bazės įrašai
Kiekvienas įrašas prasideda trynimo (1 baito) vėliavėle. Laukai suvyniojami į įrašus be laukų skyriklių. Visi lauko duomenys yra ASCII. Priklausomai nuo lauko tipo, programa nustato papildomų apribojimų. Štai dBase laukų tipai:

| Lauko tipas | Mnemoninis | Ką ji priima |
-------|-----|----|
| C | Charakteris | Bet koks ASCII tekstas (papildytas tarpais iki lauko ilgio) |
| D | Data | Skaičiai ir simbolis, atskiriantys mėnesį, dieną ir metus (viduje saugomi kaip 8 skaitmenys MMMMMMDD formatu) |
| F | Slankusis kablelis | -, ., 0–9 (išlygintas dešinėje, užpildytas tarpais) |
| L | Logiška | Y, y, N, n, T, t, F, f arba ? (kai neinicijuota) |
| M | Atmintinė | Bet koks ASCII tekstas (viduje saugomas kaip 10 skaitmenų, nurodančių .dbt bloko numerį, išlygintas dešinėje, užpildytas tarpais) |
| N | Skaitinis | -, ., 0–9 (išlygintas dešinėje, užpildytas tarpais) |









## Nuorodos Nr.

* [.dbf – Vikipedija](https://en.wikipedia.org/wiki/.dbf)


