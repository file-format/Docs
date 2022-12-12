{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Lock File Format - Ce este un fișier Lock?",
  "description":"Aflați despre formatul de fișier LOCK și despre .",
  "linktitle" : "LOCK",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Ce este un fișier LOCK?

Un fișier **LOCK** este un fișier redenumit care este utilizat de aplicații și sisteme de operare pentru a marca un fișier sau un dispozitiv ca blocat. Acest lucru le spune altor aplicații să nu folosească fișierul decât dacă este liber din aplicația care îl folosește. În majoritatea cazurilor, aceste fișiere de blocare sunt goale, dar în alte cazuri, ele pot conține informații legate de blocare, cum ar fi proprietăți și setări.

Uneori, fișierul .lock este utilizat de Microsoft .NET Framework pentru a crea copii **lockeed** ale unui fișier de bază de date. Într-un astfel de caz, o copie a fișierului bazei de date se va deschide cu extensia .lock. Acest lucru nu permite utilizatorului să facă modificări în fișierul în timp ce acesta este utilizat de un alt utilizator.

## LOCK Format fișier - Mai multe informații

Un fișier LOCK este creat de fiecare aplicație, iar formatul acestuia este specific aplicației. Aceste fișiere de blocare pot fi salvate atât în format text, cât și în format de fișier binar.

Prezența fișierelor de blocare împiedică accesul simultan al unei resurse la mai multe fișiere care încearcă să acceseze resursa respectivă. O copie a fișierului original este creată cu extensia .lock sufixată la numele său. Acest lucru le spune altor aplicații să aibă acces numai în citire la fișier. De exemplu, resource.dat va deveni resource.data.lock.

Pentru limbajul de programare Ruby, puteți întâlni fișierul **gemfile.lock**. Aici Bundler ține evidența versiunilor exacte care au fost instalate. Astfel, atunci când un proiect/bibliotecă este mutat pe o altă mașină, pachetul care rulează se va uita la Gemfile pentru versiunea relevantă exactă.

## Blocați fișierul în Linux

Linux acceptă două tipuri de blocări de fișiere: blocări consultative și blocări obligatorii.

* **Blocare consultativă**: tip de blocare care nu este aplicată. În acest caz, procesele participante cooperează între ele, dobândind în mod explicit blocări. Dacă acest lucru nu este posibil, blocările de avertizare sunt ignorate.

* **Blocari obligatorii**: În cazul blocării obligatorii, sistemul de operare impune blocarea fișierului, împiedicând alte procese să citească sau să scrie fișierul. Acest lucru nu necesită nicio cooperare între procese.

blocarea obligatorie nu necesită nicio cooperare între procesele participante. Odată ce o blocare obligatorie este activată pe un fișier, sistemul de operare împiedică alte procese să citească sau să scrie fișierul.

## Referințe

* [GemFile și Gemfile.lock în Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)
* [Blocare în Linux](https://www.baeldung.com/linux/file-locking#:~:text=File%20locking%20is%20a%20mechanism,very%20dangerous%20command%20in%20Linux.)

