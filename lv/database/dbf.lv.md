{
  "date": "2021-06-15",
  "keywords": [
"DBF",
"pagarinājumu",
"dbf failu",
"dbf faila formātā",
"Datu bāzes faila tips",
"Datu bāzes faila formāts",
"kas ir dbf fails",
"dBASE"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par DBF faila formātu un API, kas var izveidot un atvērt DBF failus.",
  "title": "DBF — dBase datu bāzes fails",
  "linktitle": "DBF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-db-lvf"
}
},
  "lastmod": "2021-06-15"
}

## Kas ir DBF fails?
The file with .dbf extension is a database file used by a database management system application called **dBASE**. Inititally, the dBASE database was named as Project Vulcan; started by **Wayne Ratliff** in 1978. DBF faila tips tika ieviests ar dBASE II 1983. gadā. Tas sakārto vairākus datu ierakstus ar masīva tipa laukiem. **xBase** datu bāzes programmatūra, kas ir populāra, jo tā ir saderīga ar plašu failu formātu klāstu; atbalsta arī DBF failus.

## DBF faila formāts
DBF faila formāts pieder dBASE datu bāzes pārvaldības sistēmai, taču tas var būt saderīgs ar xBase vai citu DBVS programmatūru. Sākotnējā dbf faila versija sastāvēja no vienkāršas tabulas, kurai varēja pievienot, modificēt, dzēst vai izdrukāt datus, izmantojot ASCII rakstzīmju kopu. Laika gaitā .dbf tika uzlabots, un tika pievienoti papildu faili, lai palielinātu datu bāzes sistēmas funkcijas un iespējas.

Mūsdienu dBASE DBF fails sastāv no galvenes, datu ierakstiem un EOF (faila beigu) marķiera.

- galvenē ir informācija par failu, piemēram, ierakstu skaits un ierakstos izmantoto lauku veidu skaits.
- Ieraksti satur faktiskos datus.
- Faila beigas ir atzīmētas ar vienu baitu ar vērtību 0x1A.

### Faila galvene
Faila galvenes izkārtojums dBase ir parādīts šajā tabulā:

| baits | Saturs | Nozīme |
---|---|---|
| 0 | 1 baits | Derīgs dBASE DOS failam; biti 0–2 norāda versijas numuru, 3. bits norāda dBASE DOS piezīmes failam, 4.–6. biti norāda SQL tabulas esamību, 7. bits norāda jebkura piezīmes faila esamību (vai nu dBASE m PLUS, vai dBASE DOS) |
| 1–3 | 3 baiti | Pēdējās atjaunināšanas datums; formatēts kā GGMMDD |
| 4–7 | 32 bitu numurs | Ierakstu skaits datu bāzes failā |
| 8–9 | 16 bitu numurs | Baitu skaits galvenē |
| 10–11 | 16 bitu numurs | Ieraksta baitu skaits |
| 12–13 | 2 baiti | Rezervēts; aizpildīt ar 0 |
| 14 | 1 baits | Karogs, kas norāda uz nepabeigtu darījumu[1. piezīme] |
| 15 | 1 baits | Šifrēšanas karodziņš[2. piezīme] |
| 16–27 | 12 baiti | Rezervēts dBASE for DOS vairāku lietotāju vidē |
| 28 | 1 baits | Ražošanas .mdx faila karodziņš; 1, ja ir ražošanas .mdx fails, 0, ja nav |
| 29 | 1 baits | Valodas draivera ID |
| 30–31 | 2 baiti | Rezervēts; aizpildīt ar 0 |
| 32–n [3. piezīme][4. piezīme] | 32 baiti katrs | lauku deskriptoru masīvs (skatīt deskriptoru izkārtojumu tālāk) |
| n + 1 | 1 baits | 0x0D kā lauka deskriptora masīva terminators |

- Funkcija ISMARKEDO pārbauda šo karogu (DARĪJUMA SĀKŠANA iestata to uz 1, END TRANSACTION un ROLLBACK atiestata uz 0).
- Ja šis karodziņš ir iestatīts uz 1, tiek parādīts ziņojums Datu bāze šifrēta.
- Maksimālais lauku skaits ir 255.
- n ir pēdējais baits lauka deskriptora masīvā.

### Lauka deskriptora masīvs
Lauku deskriptoru izkārtojums dBASE:

| baits | Saturs | Nozīme |
---|---|---|
| 0–10 | 11 baiti | Lauka nosaukums ASCII formātā (ar nulli aizpildīts) |
| 11 | 1 baits | Lauka veids. Atļautās vērtības: C, D, F, L, M vai N (nozīmes skatiet nākamajā tabulā) |
| 12–15 | 4 baiti | Rezervēts |
| 16 | 1 baits | Lauka garums binārā formātā (maksimums 254 (0xFE)). |
| 17 | 1 baits | Lauku decimāldaļu skaits binārā |
| 18–19 | 2 baiti | Darba zonas ID |
| 20 | 1 baits | Piemērs |
| 21–30 | 10 baiti | Rezervēts |
| 31 | 1 baits | Ražošanas MDX lauka karogs; 1, ja laukam ir indeksa tags ražošanas MDX failā, 0, ja nav |

### Datu bāzes ieraksti
Katrs ieraksts sākas ar dzēšanas karodziņu (1 baits). Lauki tiek ietīti ierakstos bez lauku atdalītājiem. Visi lauka dati ir ASCII. Atkarībā no lauka veida lietojumprogramma uzliek papildu ierobežojumus. Šeit ir dBase lauku veidi:

| Lauka veids | Mnemoniska | Ko tā pieņem |
-------|-----|----|
| C | Raksturs | Jebkurš ASCII teksts (pildīts ar atstarpēm līdz lauka garumam) |
| D | Datums | Cipari un rakstzīme, lai atdalītu mēnesi, dienu un gadu (iekšēji saglabāti kā 8 cipari GGGGMMDD formātā) |
| F | Peldošais punkts | -, ., 0–9 (pa labi taisnots, polsterēts ar atstarpēm) |
| L | Loģiski | Y, y, N, n, T, t, F, f vai ? (kad nav inicializēts) |
| M | Piezīme | Jebkurš ASCII teksts (iekšēji saglabāts kā 10 cipari, kas apzīmē .dbt bloka numuru, taisnots pa labi, polsterēts ar atstarpēm) |
| N | Skaitlis | -, ., 0–9 (pa labi taisnots, polsterēts ar atstarpēm) |









## Atsauces Nr.

* [.dbf — Wikipedia](https://en.wikipedia.org/wiki/.dbf)


