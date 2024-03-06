{
  "date": "2022-05-08",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GDB faila formāts — ESRI faila ģeo datu bāzes fails",
  "description": "Uzziniet par GDB failu formātu un API, kas var izveidot un atvērt GDB failus.",
  "linktitle": "GDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-gd-lvb"
}
},
  "lastmod": "2022-05-08"
}

## Kas ir GDB fails?

ESRI faila ģeodatu bāze (FileGDB) ir failu kolekcija diska mapē, kurā ir saistīti ģeotelpiskie dati, piemēram, objektu datu kopas, objektu klases un saistītās tabulas. Lai tas darbotos, kopā ar .gdb failu ir jāglabā tajā pašā direktorijā. Vaicājumus var izpildīt .gdb failā, lai pārvaldītu telpiskos un netelpiskos datus.

## GDB faila formāts — vairāk informācijas

Failu ģeodatu bāzes sastāv no septiņām sistēmas tabulām un lietotāju datiem. Lietotāja datus var glabāt šāda veida datu kopās:

* Funkciju klase

* Funkciju datu kopa

* Mozaīkas datu kopa

* Rastra katalogs

* Rastra datu kopa

* Shematiska datu kopa

* Tabula (netelpiska)

* Rīku kastes


Līdzekļu datu kopās var būt iezīmju klases, kā arī šāda veida datu kopas:

* Pielikumi

* Ar funkciju saistīta anotācija

* Ģeometriskie tīkli

* Tīkla datu kopas

* Paku audumi

* Attiecību nodarbības

* Apvidus

* Topoloģijas


Noklusējuma maksimālais datu kopu lielums failu ģeodatu bāzēs ir 1 TB. Maksimālo lielumu var palielināt līdz 256 TB lielām datu kopām (parasti rastra). To kontrolē konfigurācijas atslēgvārds. Papildinformāciju skatiet sadaļā Failu ģeodatu bāzu konfigurācijas atslēgvārdi.

Failu ģeodatu bāzēs var būt arī apakštipi un domēni, un tās var piedalīties izrakstīšanās/reģistrēšanās replikācijā un vienvirziena replikās.

Failu ģeodatu bāzei vienlaikus var piekļūt vairāki lietotāji. Ja lietotāji rediģē, viņiem ir jārediģē dažādas datu kopas.

## GDB faila formāta specifikācijas ##

Fails GDB ir ESRI patentēts formāts, un tā specifikācijas nav pieejamas publiski. Šī iemesla dēļ faila GDB faila formāta informāciju nevarēja dokumentēt nekur citur, izņemot dažus avotus, kuri to ir izdarījuši [partially](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec), izmantojot reverso inženieriju.

## Atsauces Nr.

* [FGDB specifikācijas](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec)


