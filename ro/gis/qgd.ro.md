{
  "date" : "2021-03-18",
  "author" : {
    "display_name" : "Muhammad Umar",
	"keywords" :[ "QGD", "Bază de date Sqlite a proiectului QGIS", "extensie", "format", "QGIS", "Bază de date auxiliară", "Ce este un fișier QGD"]
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGD - Baza de date Sqlite a proiectului QGIS",
  "description":"Aflați despre QGD, care este o bază de date sqlite a proiectului QGIS și API-uri care pot crea și deschide fișiere QGD.",
  "linktitle" : "QGD",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Ce este un fișier QGD?

Fișierul cu extensia .QGD este de fapt baza de date sqlite asociată proiectului **QGIS** care găzduiește datele auxiliare pentru proiect. Fișierul QGD va rămâne gol, dacă nu vor exista date auxiliare pentru proiect.

## Detalii despre formatul fișierului QGD

În modul clasic, baza de date auxiliară este salvată ca fișier cu extensia .qgd de-a lungul fișierului xml. Sistemul **Bază de date auxiliară** permite citirea și scrierea datelor în sistem ca o modalitate alternativă. Când se creează QGZ, care este un container arhivat, fișierul .qgd este inclus în .qgz.

## Ce este baza de date auxiliară?
Baza de date auxiliară este de fapt un sistem db de așteptare care este creat ca răspuns la duplicarea bazei de date țintă. Baza de date auxiliară este de fapt un caz de bază de date duplicat ar fi baza de date pe care o duplicați. De exemplu, dacă configurați o bază de date de așteptare folosind o bază de date duplicată, baza de date sursă va fi țintă, iar baza de date de așteptare va fi cunoscută ca auxiliară.


## Referințe

* [QGZ – Un nou format implicit de fișier de proiect pentru QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [Formate de fișiere QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

