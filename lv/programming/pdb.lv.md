{
  "date": "2019-10-11",
  "keywords": [
"pdb failu",
"pdb",
"pagarinājumu",
"formātā",
"Kas ir pdb fails",
"pdb faila formātā",
"PBP metadati"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PBP faila formāts — programmas datu bāzes fails",
  "description": "Uzziniet par PBP faila formātu un API, kas var izveidot un atvērt PDB failus.",
  "linktitle": "PDB",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-pd-lvb"
}
},
  "lastmod": "2020-09-10"
}

## Kas ir PBP fails?

Fails ar paplašinājumu .pdb ir programmas datu bāzes fails, kurā ir apkopota izpildāmā faila (EXE/DLL) atkļūdošanas informācija. PBP failus ģenerē Microsoft kompilatori, kad lietojumprogramma tiek kompilēta atkļūdošanas režīmā. PDB faila klātbūtne var palīdzēt izpildāmā faila apgrieztā inženierijā, jo tas satur nozīmīgu informāciju par visiem moduļu simboliem. Šī iemesla dēļ šie faili tiek turēti atsevišķi no galīgā izpildāmā faila. Microsoft [DgbHelp API](https://learn.microsoft.com/en-us/windows/win32/debug/dbghelp-functions) var atvērt PBP failu, lai iegūtu informāciju, piemēram, publiskošanu un eksportēšanu, globālos simbolus, vietējos simbolus, tipa datus, avota failus un rindu numurus.

## PBP faila formāts

PDB ir Microsoft patentēts faila formāts, un tas vēl nekur nav oficiāli dokumentēts. Tomēr sākuma dokumentācija ir pieejama [here](https://github.com/Microsoft/microsoft-pdb) un uz to var atsaukties.

### PBP straumes

PBP faili sastāv no vairākām straumēm, kur katra straume darbojas kā virtuāls atsevišķs fails un satur informāciju. PDB failu rakstītāji var rakstīt šajos failos, un fails tiek pabeigts tikai pēc skaidras saistības izdošanas. Kompilators var turpināt rakstīt PDB failā, bet veikt darbību tikai tad, ja viss lietotāja kods ir veiksmīgi kompilēts. PBP fails sastāv no šādām straumēm:

|Straumes Nr. |Saturs |Īss apraksts|
---|---|---|
|1| Pdb (galvene) |Informācija par versiju un informācija, lai šo PBP savienotu ar EXE|
|2| Tpi (tipu pārvaldnieks) |Visi izpildāmajā failā izmantotie veidi.|
|3| Dbi (Atkļūdošanas informācija) |Satur sadaļas ieguldījumus un 'Modifikācijas' sarakstu|
|4| NameMap| Uztur jauktu virkņu tabulu|
|4-(n+4)| n Mod's (Moduļa informācija)| Katrā Mod straumē ir simboli un rindu numuri vienai kompilandei|
|n+4| Globālais simbols hash| Indekss, kas ļauj meklēt globālos simbolos pēc nosaukuma|
|n+5| Publisks simbols hash| Indekss, kas ļauj meklēt publiskos simbolos pēc adresēm|
|n+6| Simbolu ieraksti| Faktiskie globālo un publisko simbolu simbolu ieraksti|
|n+7| Ierakstiet hash| TPI straumē izmantotais jaukums.|

Katra straume PBP failā sastāv no vairākām lappusēm, kuras ne vienmēr ir secīgi numurētas.

### PBP virsraksts

PBP failam ir galvene, kas sastāv no paraksta konkrētā formāta identificēšanai un apstiprināšanai. Paraksta garums ir atkarīgs no PBP formāta. Galvene var būt garāka par vienu lapu.

### PBP metadati
The PDB metadata is responsible to recognize all of the component streams, giving the length, and sequence of pages for each stream. Orders are given to streams consecutively; starting with 0. Ir arī nesakārtota saknes straume, kurā ir daži metadati.

## Atsauces
 * [PBP — Wikipedia](https://en.wikipedia.org/wiki/Program_database)
 * [Microsoft PDB](https://github.com/Microsoft/microsoft-pdb)

