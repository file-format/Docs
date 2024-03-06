{
  "date": "2021-05-25",
  "keywords": [
"DML",
"DML fails",
"DML faila formāts",
"DML faila tips",
"failu",
"veids",
"kas ir DML fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DML — DynaScript HTML fails",
  "description": "Uzziniet par DML faila formātu un API, kas var izveidot un atvērt DML failus.",
  "linktitle": "DML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-dm-lvl"
}
},
  "lastmod": "2021-05-25"
}

## Kas ir DML fails?

Fails ar paplašinājumu .dml ir tīmekļa skripta lapas koda fails, kas izveidots ar DyanScript. DynaScript ir dinamiska [HTML](/web/html/) skriptu valoda, kas ir saderīga ar ECMAScript un nodrošina lielāko daļu to pašu funkciju kā citas skriptu valodas. Tas ir līdzīgs ColdFusion kodam un Microsoft Active Server Pages (ASP) kodam. DML failus var atvērt un skatīt standarta tīmekļa pārlūkprogrammās, kas ir līdzīgas citām HTML lapām.

## DML faila formāts

DML faili tiek izveidoti vienkārša teksta faila formātā, un tos var atvērt ar teksta redaktoru, lai skatītu kodu. Koda rakstīšanu, izmantojot DML skriptu valodu, var izmantot, lai dinamiski ģenerētu HTML servera pusē mitinātajās DML lapās. DynaScripts ir veidoti no šādiem valodas elementiem:


 * SCRIPT tags — tie ir iegulti dokumentos kā HTML komentāri. HTML komentārs ir atzīmēts ar \
 * Literāļi — tās ir fiksētas vērtības DynaScript failos. To piemēri ir veseli skaitļi, piemēram, s 123 , 0x3F , 0123, peldošā komata skaitļi, piemēram, 456.789 , 3.2e-8, Būla skaitļi, piemēram, patiess vai nepatiess, un virkne, piemēram, Lietus Spānijā.
 * Mainīgie — DynaScript mainīgie nav jādefinē vai jāpiešķir fiksētam datu tipam. Mainīgajam ir jābūt vērtībai, pirms to izmantojat izteiksmē; pretējā gadījumā tiek ģenerēts izpildlaika brīdinājums.
 * Izteiksmes — tās ir mainīgo, burtisko vērtību, operatoru un citu izteiksmju kombinācijas. Piešķiršanas paziņojuma labā puse ir izteiksme.
 * Operatori — tie darbojas ar vienu vai vairākām izteiksmēm, ko sauc par operandiem. Tie var būt trīskārši, bināri vai unāri: trīskāršie operatori darbojas pēc trim izteiksmēm, binārie operatori darbojas ar divām izteiksmēm, un vienkāršā operatori darbojas ar vienu.
 * Paziņojumi — tie kontrolē skriptu plūsmu, manipulē ar objektiem un vispārīgo programmēšanu. Parasti šie paziņojumi atbilst standarta C un Java sintaksei. Piemēri ir if-else, do-while cilpas, pārslēgšana, pārtraukums, turpināšana utt., tāpat kā jebkura cita skriptu valoda.
* Funkcijas — Funkcijas, tāpat kā jebkura cita skriptu valoda, ļauj vienu reizi dokumentā kā funkciju iekapsulēt instrukciju kopu, pēc tam to vairākas reizes izmantot visā dokumentā (izsaucot funkciju). DynaScript atbalsta arī funkcijas.

* Objekti — DynaScript ir orientēts uz objektiem un atbalsta “objektus” un pamatjēdzienus, kas orientēti uz objektiem: iekapsulēšana, polimorfisms un mantošana.


