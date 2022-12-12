{
  "date" : "2021-03-10",
  "keywords" :[ "ACSM", "Adobe Content Server Message", "extensie", "format", "eBook", "fișier", "Adobe Digital Editions"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier ACSM de la Adobe și API-urile care pot crea și deschide fișiere ACSM.",
  "title" :"ACSM - Adobe Content Server Message File Format",
  "linktitle" : "ACSM",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## Ce este un fișier ACSM?

Fișierele cu extensia .acsm se numesc fișiere Adobe Content Server Message. Aceste fișiere sunt folosite de **Adobe Digital Editions** pentru a activa și descărca conținut protejat Adobe DRM. De fapt, un fișier ACSM nu este un fișier eBook; nu poate fi deschis și citit ca și alte cărți electronice (ex. PDF); Conține doar datele pentru activarea și descărcarea unei cărți electronice. Înseamnă că un fișier ACSM constă numai din informațiile care comunică cu serverele Adobe. Utilizatorii Digital Editions pot vedea fișierul ACSM dacă vor descărca o carte electronică, dar descărcarea s-ar fi oprit din orice motiv. Utilizatorii pot relua descărcarea făcând dublu clic pe fișierul .acsm.

## Cum funcționează un fișier ACSM?

Deoarece Adobe Content Server este responsabil să protejeze cărțile electronice și alte materiale digitale. După cumpărare, conținutul este conectat automat la ID-ul Adobe al cumpărătorului. ID-ul este privat și nu poate fi transferat altora. Un utilizator trebuie să îl configureze înainte de a cumpăra orice document cu protecție Adobe împotriva copierii. Clienții nu pot avea acces la documentele lor protejate împotriva copierii fără a-și transmite ID-ul Adobe aplicației de server Adobe care rulează în fundal.

Când clienții își fac achiziția, ACSM este singurul fișier pe care îl pot descărca la început. Clientul trebuie să fi instalat software-ul Adobe Digital Editions pe sistemul său și să l-a conectat la Adobe ID-ul pentru a deschide fișierul ACSM. Adobe Digital Editions va verifica ID-ul pentru autorizarea de a converti fișierul ACSM. Dacă este autentificat, utilizatorul își poate descărca cartea electronică în format [EPUB](/ro/ebook/epub/) sau [PDF](/ro/pdf/). Adobe Digital Editions folosește, de asemenea, fișierul ACSM pentru a recunoaște directorul de descărcare.

## Referințe

* [Adobe Content Server - Prin Wikipedia](https://en.wikipedia.org/wiki/Adobe_Content_Server)


