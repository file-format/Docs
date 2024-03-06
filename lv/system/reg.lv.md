{
  "date": "2023-03-07",
  "keywords": [
"reg fails",
"kas ir reg fails",
"failu",
"reg faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "REG faila formāts — Windows reģistra fails",
  "description": "Uzziniet par REG formātu un API, kas var izveidot un atvērt REG failus.",
  "linktitle": "REG",
  "menu": {
    "docs": {
      "identifier": "system-reg-lv",
      "parent": "system"
}
},
  "lastmod": "2023-03-07"
}

## Kas ir REG fails?

REG fails ir faila formāts, ko izmanto Windows reģistra datu importēšanai vai eksportēšanai. Windows reģistrs ir hierarhiska datu bāze, kurā tiek glabāti Windows operētājsistēmas un instalēto lietojumprogrammu konfigurācijas iestatījumi un opcijas. Reģistrā ir informācija, piemēram, lietotāja preferences, lietojumprogrammu iestatījumi, aparatūras un programmatūras konfigurācijas dati un daudz kas cits.

REG failam parasti ir .reg” faila paplašinājums, un tas ir vienkārša teksta fails, kas satur virkni reģistra ierakstu un vērtību noteiktā formātā. Formāts sastāv no galvenes sadaļas, kas identificē failu kā reģistra failu, kam seko virkne atslēgu un vērtību pāru, kas attēlo reģistra ierakstus.

## REG faila formāts — vairāk informācijas

Šeit ir reg faila formāta piemērs:

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

Faila pirmajā rindā ir norādīta reģistra redaktora versija. Nākamajās rindās ir reģistra ieraksti atslēgas ceļa formātā, kam seko vērtības nosaukums un vērtības dati. Šajā piemērā reg failā ir divi ieraksti: viens, kas pievieno programmu Example.exe Windows startēšanas sarakstam, un otrs, kas iestata Hidden vērtību Windows Explorer papildu iestatījumos uz true.

Reg failus var izveidot un rediģēt, izmantojot teksta redaktoru, piemēram, Notepad. Tos bieži izmanto dublēšanai un atjaunošanai, kā arī vairāku datoru konfigurēšanai ar vienādiem reģistra iestatījumiem.

## Importējiet vai eksportējiet Windows reģistru

REG fails ir faila veids, ko izmanto datu importēšanai vai eksportēšanai no Windows reģistra. Windows reģistrs ir hierarhiska datu bāze, kurā tiek glabāti Windows operētājsistēmas un instalēto lietojumprogrammu konfigurācijas iestatījumi un opcijas. Reģistrā ir informācija, piemēram, lietotāja preferences, lietojumprogrammu iestatījumi, aparatūras un programmatūras konfigurācijas dati un daudz kas cits.

Reg failus var izmantot, lai izveidotu vai modificētu reģistra ierakstus, un tos bieži izmanto dublēšanai un atjaunošanai, kā arī vairāku datoru konfigurēšanai ar vienādiem reģistra iestatījumiem. Lūk, kā izmantot reg failu, lai pievienotu jaunu reģistra ierakstu Windows reģistram:

1. Izveidojiet jaunu teksta failu, izmantojot teksta redaktoru, piemēram, Notepad.
2. Ievadiet reģistra ierakstu pareizajā formātā. Formāts sastāv no galvenes sadaļas, kas identificē failu kā reģistra failu, kam seko virkne atslēgu un vērtību pāru, kas attēlo reģistra ierakstus. Šeit ir piemērs:

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

Tādējādi pašreizējā lietotāja reģistra stropā zem atslēgas Programmatūra tiek izveidota jauna atslēga ar nosaukumu Piemērs un Setting1 vērtība tiek iestatīta uz Vērtība1.

3. Saglabājiet failu ar .reg faila paplašinājumu.
4. Veiciet dubultklikšķi uz .reg faila, lai pievienotu jauno reģistra ierakstu Windows reģistram.

Jums tiks piedāvāts apstiprināt, ka vēlaties pievienot ierakstu reģistrā. Pēc apstiprināšanas jaunais ieraksts tiks pievienots reģistram, un jūs varat to pārbaudīt, izmantojot reģistra redaktora rīku.

## Atsauces
* [Windows reģistrs](https://en.wikipedia.org/wiki/Windows_Registry)


