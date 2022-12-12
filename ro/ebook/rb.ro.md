{
  "date" : "2021-03-08",
  "keywords" :[ "RB", "Dispozitivul Nuvo Media Rocket eBook", "fișier", "extensie", "format", "eBook" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier RB pentru dispozitivul Rocket eBook al Nuvo Media și API-urile care pot crea și deschide fișiere RB.",
  "title" :"RB - Fișier eBook Rocket",
  "linktitle" : "RB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## Ce este un fișier RB?

Fișierul cu extensia .rb deține conținutul cărții electronice Rocket. Cartea electronică Rocket este de fapt un dispozitiv realizat de Nuvo Media; au lansat acest dispozitiv în 1998. Deși Rocket eBook este capabil să afișeze imagini, dar numai în afișaj alb-negru. Are un ecran de 106 dpi sau 480 x 320 pixeli pe un ecran tactil de 4,5 x 3 inci. Cartea electronică Rocket se conectează la un computer printr-o conexiune de port serial pentru a descărca cărți electronice în format de fișier RB. Fișierele RB sunt capabile să utilizeze DRM, dar această tehnologie nu este utilizată în cărțile electronice moderne. Fișierul RB conține în mod convențional un fișier HTML cu imagini și un fișier pseudo-OPF cu toate metadatele (.info).

## Specificația tehnică a formatului fișierului RB ##

Un număr magic (în hex) apare în primii 4 octeți ai fișierului: B0 0C B0 0C.

Se pare că următorii doi octeți sunt un număr de versiune, cum ar fi „02 00”, care reprezintă versiunea majoră 2 și versiunea minoră 0.

Următorii patru octeți conțin textul „NUVO”, urmat de 4 octeți de 00h.

Următorul 4 octeți este data la care a fost creată cartea, codificată ca int16. Acest lucru ne pune la offset 0Eh. Versiunea veche a ORocketLibrary a codificat valoarea totală a anului (adică, 1999 a fost „CF 07”, 2000 a fost „D0 07”). În versiunea recentă, tm_year este stocat textual, adică 100 pentru anul 2000 ("64 00"). După an vine un int8 reprezentând numărul relativ de 1 lună și un int8 reprezentând ziua lunii.

Următorii 6 octeți sunt 00h. Pentru setarea orei, acestea pot fi rezervate.

Offset-ul absolut al „Cuprinsului” este conținut într-un int32 la offset 18h.

După aceasta este un int32 care conține lungimea fișierului .rb. Acesta este folosit pentru a determina dacă fișierele sunt complete sau nu.

Toată această bucată de octeți (20h până la 128h) pare să fie nevoie doar de un titlu care este criptat. În titlurile necriptate, acestea sunt întotdeauna zero.

În cele mai multe cazuri, urmează cuprinsul (la offset 128). Începe cu o contorizare int32 a numărului de intrări „pagină” (secțiuni .rb-file) din ToC. Fiecare intrare constă dintr-un nume (zero-padded la 32 de octeți), urmat de 3 int32s: lungimea segmentului de date, poziția în fișierul .rb și un steag pentru această intrare. Începând de astăzi, valorile cunoscute sunt: 1 (criptat), 2 (pagina de informații) și 8 (dezumflat). Numele sunt toate personalizate, după cum este necesar, pentru a se asigura că sunt toate unice.

## Referințe

* [E-Reader - de MobileRead](https://en.wikipedia.org/wiki/E-reader)

