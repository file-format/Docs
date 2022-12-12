{
  "date" : "2019-10-11",
  "keywords" :[ "asp","fișier asp", "format fișier asp", "tip fișier asp", "fișier", "tip", "ce este un fișier asp" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASP – Active Server Pages File Format",
  "description" :"Aflați despre ce este un fișier ASP și API-urile care le pot crea și deschide.",
  "linktitle" : "ASP",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier ASP?

ASP înseamnă Active Server Pages, care este un cadru de dezvoltare pentru crearea de pagini web. Permite executarea codului computerului de către un server intern pentru a servi cererile web. Când este generată o solicitare pentru un fișier ASP de către browser web, serverul citește fișierul și execută orice cod/script din interiorul acestuia pentru a genera rezultatul **[HTML](/ro/web/html/)** care este returnat la browser pentru afișare.

Spre deosebire de paginile HTML, care sunt pagini statice servite de server, fișierele ASP generează conținut dinamic în timpul execuției, care poate implica solicitări de date dintr-o bază de date. Paginile ASP folosesc de obicei extensia .asp mai degrabă decât .html. Deoarece codul/scriptul din interiorul unui fișier ASP este executat pe partea serverului, browserul solicitant nu poate vedea codul folosit pentru a construi pagina difuzată. Toate browserele moderne sunt capabile să afișeze pagini generate ca rezultat. Fiind construite pe tehnologia Microsoft, paginile create cu ASP sunt găzduite pe serverele Microsoft Internet Information Services (IIS).

## Scurt istoric al formatului de fișier ASP
ASP a trecut prin doar câteva revizuiri, dar a fost înlocuit de ASP.NET, care este o modalitate mai modernă și mai eficientă de dezvoltare și gestionare a paginilor de pe server. Suportul pentru ASP este inclus în mod implicit împreună cu Internet Information Services (IIS). ASP a fost publicat în trei versiuni diferite, cu îmbunătățiri în fiecare.

* ASP 1.0 a fost lansat în decembrie 1996 ca parte a IIS 3.0
* ASP 2.0 a fost lansat în septembrie 1997 ca parte a IIS 4.0
* ASP 3.0 a fost lansat în noiembrie 2000 ca parte a IIS 5.0

## Obiecte funcționale ASP

Fișierele ASP folosesc obiecte din partea serverului pentru a procesa cererile utilizatorilor și pentru a genera pagini de ieșire pentru a fi servite utilizatorilor. Fiecare obiect are un set de colecții, proprietăți și metode pentru procesarea cererilor și răspunsurilor. Aceste obiecte includ:

### Solicitare obiect

Când un browser solicită o pagină de la un server, se numește cerere. Obiectul Request este folosit pentru a obține informații de la un vizitator.

### Obiect de răspuns

Obiectul ASP Response este folosit pentru a trimite ieșire utilizatorului de pe server.

### Obiect server

Obiectul ASP Server este utilizat pentru a accesa proprietăți și metode de pe server. Permite conexiuni la baze de date (ADO), sistemul de fișiere și utilizarea componentelor instalate pe server.

### Obiect de sesiune

Un obiect de sesiune este ca o legătură între browserul utilizatorului care solicită o pagină de la server și serverul însuși. Acest lucru se realizează printr-un cookie creat de ASP și trimis pe computerul utilizatorului. Obiectul Sesiune stochează informații despre, sau modifică setările pentru o sesiune de utilizator. Informațiile sunt stocate într-un obiect Session sunt partajate în toate paginile unei aplicații. Informațiile comune stocate în variabilele de sesiune sunt numele, id-ul și preferințele. Serverul creează un nou obiect Session pentru fiecare utilizator nou și distruge obiectul Session atunci când sesiunea expiră.

### Obiect de aplicație

Obiectul Aplicație conține informații care vor fi utilizate de multe pagini din aplicație (cum ar fi informațiile de conectare la baza de date). Informațiile pot fi accesate de pe orice pagină. Informațiile pot fi modificate și într-un singur loc, iar modificările se vor reflecta automat pe toate paginile. Obiectul Application este folosit pentru a stoca și accesa variabile din orice pagină, la fel ca obiectul Session.

### Obiect ASPError

Obiectul ASPError a fost implementat în ASP 3.0 și este disponibil în IIS5 și mai târziu. Obiectul ASPError este folosit pentru a afișa informații detaliate despre orice eroare care apare în scripturi dintr-o pagină ASP.

**Notă:** Obiectul ASPError este creat atunci când este apelat Server.GetLastError, astfel încât informațiile despre eroare pot fi accesate numai folosind metoda Server.GetLastError.

## Referințe

* [ASP - Prin W3C](https://www.w3schools.com/asp/default.asp)
* [Crearea de pagini ASP simple](https://docs.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))

