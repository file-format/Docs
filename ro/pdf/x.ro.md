{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier PDF/X",
  "description":"Aflați despre formatul de fișier PDF/X și despre API-urile care pot crea și deschide fișiere PDF/X.",
  "linktitle" : "PDF/X",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Ce este fișierul PDF/X? #

PDF/X este un standard ISO 15930 publicat în 2001 cu un subset de funcționalități PDF. Standardul a fost stabilit și publicat pe baza cerințelor specifice ale industriilor tipografice și editoriale. Cerințele pentru acest standard au fost toate concepute în funcție de nevoile diverse ale industriilor tipărite și editoriale. PDF/X necesită ca fișierele conforme să fie complete, adică autonome. Acest lucru necesită ca elemente precum fonturile utilizate în pagină să facă parte din document. Conținutul precum 3D sau video nu poate face parte din documentul PDF/X. Informațiile conținute în documentul PDF/X necesită ca acestea să fie corecte.

## Standarde și revizuiri PDF/X ##

Familia de standarde PDF/X cuprinde mai multe versiuni, fiecare proiectată pentru un rezultat specializat. Dezvoltarea acestor standarde a fost menită să răspundă nevoilor diverse ale industriilor tipărite și editoriale.

* `PDF/X-1a` - Cunoscut și ca primul standard al familiei PDF/X, PDF/X-1a necesită ca întregul conținut să facă parte din documentul PDF pentru a putea fi tipărit. Elementele de document precum fonturile, formularele, protecția prin parolă și adnotările vizibile nu sunt permise. PDF/X-1a are propriile cerințe specifice, precum și cele referitoare la transparență și straturile sunt permise. Acestea necesită, de asemenea, ca elementele de imprimare să utilizeze numai culori CMYK, tonuri de gri sau spot, rezultând în nicio utilizare a spațiilor de culoare RGB sau independente de dispozitiv. este pentru schimburi în care toate fișierele vor fi livrate în CMYK (și/sau culori spot), fără date RGB sau gestionate de culoare. PDF/X-1a este, de asemenea, denumit Schimb complet datorită caracterului complet al informațiilor solicitate de
* `PDF/X-3` - a fost introdus în 2002 și a ridicat multe restricții ale PDF/X-1a. Acest lucru a permis graficelor dintr-un PDF/X-3 să utilizeze spații de culoare CMYK, grescale, RGB, Lab și ICC. De fapt, se bazează pe standardele PDF 1.3 cu [profil ICC](https://en.wikipedia.org/wiki/ICC_Profile). Se mai numește Color Management datorită flexibilității și regulilor pe care le introduce legate de culorile incluse într-un document PDF.
* `PDF/X-4` - acceptă transparențe, astfel încât PDF-X/4 conține toate datele necesare pentru ieșire fără aplatizare.
* `PDF/X-5` - se bazează pe PDF/X-4, adăugând suport pentru grafică externă prin intermediul XObjects de referință, precum și profiluri externe n-coloranți pentru redarea intenției. Utilizați-l pentru schimbul parțial de date de tipărire folosind versiunea PDF 1.6

## Referințe ##

* [PDF/X - După Wikipedia](https://en.wikipedia.org/wiki/PDF/X)

