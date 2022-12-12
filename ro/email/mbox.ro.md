{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MBOX – Fișier cutie poștală de e-mail",
  "description":"Aflați despre formatul de fișier MBOX și despre API-urile care pot crea și deschide fișiere MBOX.",
  "linktitle" : "MBOX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier MBOX?

Formatul de fișier MBox este un termen generic care reprezintă un container pentru colectarea mesajelor de poștă electronică. Mesajele sunt stocate în interiorul containerului împreună cu atașamentele lor. Mesajele dintr-un folder întreg sunt salvate într-un singur fișier de bază de date și mesajele noi sunt atașate la sfârșitul fișierului. Numeroase aplicații și API oferă suport pentru formatul de fișier MBox, cum ar fi Apple Mail și Mozilla Thunderbird.

## Format de fișier MBOX ##

Formatul de fișier MBox a rămas nestandardizat destul de mult timp până în 2005, când aplicația/mbox a fost standardizată ca [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Mesaje, în format RFC 2822 , sunt concatenate în formatul de fișier MBox unul după altul. Fiecare mesaj începe cu o linie de separare care identifică expeditorul mesajului și, de asemenea, identifică data și ora la care mesajul a fost primit de către destinatarul final (fie sistemul ultimului salt din calea de transfer, fie sistemul care servește ca destinatarului). mailstore). Fiecare mesaj este terminat de obicei printr-o linie goală. Sfârșitul bazei de date este de obicei recunoscut fie prin absența oricăror date suplimentare, fie prin prezența unui marcator explicit de sfârșit de fișier.

## Citirea unui mesaj din fișierul MBox ##

Un cititor scanează printr-un fișier mbox căutând De_ linii. Orice linie From_ marchează începutul unui mesaj. Cititorul nu ar trebui să încerce să profite de faptul că fiecare linie From_ (dincolo de începutul fișierului) linie goală. Odată ce cititorul găsește un mesaj, extrage un expeditor de plic (posibil corupt) și data de livrare din linia From_. Apoi citește până la următoarea linie From_ sau la sfârșitul fișierului, oricare dintre acestea survine primul. Îndepărtează linia goală finală și șterge ghilimele >From_ lines și >>From_ lines și așa mai departe. Rezultatul este un mesaj RFC 822.

## Considerații privind codificarea ##

Conținutul unui fișier MBox poate deveni amestecat ireversibil atunci când un e-mail primit conține un fișier Mbox ca atașament și este salvat într-un alt fișier Mbox. Pentru a evita acest lucru, sistemele de mesagerie trebuie să codifice o bază de date mbox cu codare de transfer netransparentă (cum ar fi BASE64 sau Quoted-Printable) ori de câte ori un astfel de obiect este transferat prin protocoale de mesagerie. Implementatorii ar trebui, de asemenea, să fie pregătiți să codifice datele mbox la nivel local dacă sunt primite date neconforme.

## Referințe ##

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)
* [Mbox - Wikipedia](https://en.wikipedia.org/wiki/Mbox)

