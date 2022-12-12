{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier OSR și despre API-urile care pot crea și deschide fișiere OSR.",
  "title" :"Fișier OSR - osu! Replay File Format",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Ce este un fișier OSR?

Un fișier OSR este un fișier de reluare a jocului creat de [osu! joc](https://osu.ppy.sh/home). Osu! este un joc de ritm în care utilizatorii potrivesc clicurile mouse-ului cu muzica. Cântecul redat de utilizator, succesele și ratarile, ora și data cântecului redat și clasamentul general sunt înregistrate în fișierul OSR. Acest fișier OSR poate fi apoi partajat altora în scopul reluării. Fișierul OSR necesită ca fișierul beatmap să fie prezent în folderul „Cântece”.

**Tipul MIME de format de fișier OSR:** x-osu-replay

## Format de fișier OSR

Fișierele OSR sunt salvate ca fișiere binare cu câmpuri de date cu lungime fixă și variabilă.

|Tipul de date| Format|
---|---|
|Byte |Modul de joc al reluării (0 = osu! Standard, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mania)|
|Număr întreg |Versiunea jocului când a fost creată reluarea (ex. 20131216)|
|String |osu! beatmap MD5 hash|
|Șnur| Nume jucător|
|Șnur| osu! reluare hash MD5 (include anumite proprietăți ale reluării)|
|Scurt| Număr de 300 de sec|
|Scurt| Număr de 100 în standard, 150 în Taiko, 100 în CTB, 100 în mania|
|Scurt| Număr de 50 de ani în standard, fructe mici în CTB, 50 de ani în mania|
|Scurt| Număr de Gekis în standard, Max 300s în mania|
|Scurt| Numărul de Katus în standard, 200s în mania|
|Scurt| Numărul de rateuri|
|Număr întreg| Scorul total afișat în raportul de scor|
|Scurt| Cea mai bună combinație afișată în raportul de scor|
|Oct| Combo perfect/complet (1 = fără rateuri și fără întreruperi de glisare și fără glisoare terminate devreme)|
|Număr întreg| Moduri folosite. Vezi mai jos lista de valori ale modului.|
|Șnur| Grafic cu bare de viață: perechi separate prin virgulă u/v, unde u este timpul în milisecunde în melodie și v este o valoare în virgulă mobilă de la 0 - 1 care reprezintă cantitatea de viață pe care o aveți la momentul dat (0 = bara de viață este gol, 1= bara de viață este plină)|
|Lung| Marca temporală (bifări Windows)|
|Număr întreg| Lungimea în octeți a datelor de redare comprimate|
|Oct |Matrice Date de redare comprimate|
|Lung| Scor online ID|
|dublu| Informații suplimentare despre mod. Prezent numai dacă este activată Practica țintă.|

## Referințe

* [OSU! Joc de ritm](https://osu.ppy.sh/home)
* [Format fișier OSR](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)

