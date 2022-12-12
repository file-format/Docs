{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICS - Format de fișier iCalendar",
  "description":"Aflați despre formatul de fișier ICS și despre API-urile care pot crea și deschide fișiere ICS.",
  "linktitle" : "ICS",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier ICS?

Specificația principală a obiectelor pentru calendarul și programarea pe Internet (iCalendar) este un standard de internet (RFC 2445) pentru schimbul și implementarea evenimentelor de calendar și programare. Formatul iCalendar este interoperabil, asigurând astfel schimbul de informații din calendar între utilizatorii care au diferite aplicații de e-mail. iCalendar formatează datele de intrare ca extensii de poștă Internet multifuncțională (MIME) și facilitează schimbul de obiecte prin diferite protocoale de transport. Aceste protocoale de transport pot fi SMTP, HTTP, comunicare asincronă punct-la-punct și transport de rețea bazat pe medii fizice.

iCalendar permite utilizatorilor să partajeze evenimente, sarcini dependente de dată/ora și informații despre liber/ocupat prin e-mailuri către alți utilizatori care pot răspunde. Fișierele iCalendar sunt stocate folosind sufixe „.ics” „.iCalendar” sau „.ifb” cu un tip MIME „text/calendar”. iCalendar este menținut să fie autonom, fără nicio dependență de protocolul de transport. Serverele web (cu protocol HTTP) pot transporta informații iCalendar, iar paginile web pot conține date iCalendar în formă încorporată folosind iCalendar.

## Scurt istoric al formatului de fișier ICS

În 1998, Internet Engineering Task Force (IETF) a definit iCalendar ca standard (RFC 2445). Standardul a fost documentat de Frank Dawson (Lotus Notes Corporation) și Derik Stenerson (Microsoft). În 2009, standardul a fost din nou rafinat de Bernard Desruisseaux (Oracle) ca RFC 5545. De data aceasta au fost adăugate unele caracteristici noi, iar unele caracteristici învechite au fost depreciate. În 2016, RFC 7986 a fost lansat și mărit la originalul iCalendar RFC. RFC 7986 a adăugat noi caracteristici obiectului principal VCALENDAR și au fost introduse și noi caracteristici de sprijin pentru sistemele de conferințe.

## Format de fișier ICS ##

Tipul MIME utilizat de datele din iCalendar este „text/calendar”. Setul de caractere implicit pentru iCalendar este UTF-8, cu toate acestea, prin furnizarea de parametri în MIME, poate fi utilizat un set de caractere diferit. Un fișier iCalendar conține secțiuni, printre aceste secțiuni „VCALENDAR”, este secțiunea globală care încapsulează toate celelalte secțiuni. Secțiunea VEVENT definește evenimente, VTODO listează toate elementele de făcut, VJOURNAL conține intrări în jurnal și VTIMEZONE specifică informații despre fusul orar. sunt permise mai multe secțiuni de categorie similară. Pentru numeroase evenimente, mai multe secțiuni VEVENT pot fi prezente într-un fișier iCalendar.

### Rânduri de conținut ###

Obiectele iCalendar sunt aranjate în linii distincte de text „linii de conținut”. În acest format de fișier, secvența CRLF termină o linie, în timp ce lungimea liniei este limitată la 75 de octeți, excluzând întreruperea de linie. Un articol de date lung poate fi extins pe mai multe rânduri.

### Separatoare de liste și câmpuri ###

Proprietățile și parametrii specifică o listă de valori care sunt separate printr-un caracter virgulă. Șirurile între ghilimele sunt folosite pentru valorile parametrilor bazate pe URI. Lista parametrilor poate fi construită după valoarea proprietății. Fiecare parametru de proprietate din această listă trebuie despărțit printr-un punct și virgulă.

Într-o listă de valori, un SEMICOLON izolează parametrii de proprietate și o virgulă separă valorile proprietăților. Un exemplu este dat mai jos:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Valori multiple

Unele proprietăți pot avea mai multe valori. Pur și simplu generarea unei noi linii de conținut cu numele proprietății este regula de bază pentru proprietățile cu valori multiple. Cu toate acestea, pentru o singură valoare cu mai multe variante de limbă nu trebuie să utilizați proprietăți cu mai multe valori.

### Conținut binar

În cadrul unui obiect iCalendar, valoarea proprietății poate face referire la date de conținut binar plasate într-o entitate MIME externă folosind un URI. Conținutul binar în linie poate fi utilizat în situații speciale cu parametrul „CODIFICARE”, în care aplicația trebuie să exprime un obiect iCalendar ca entitate unică. Următorul exemplu explică o proprietate „ATTACH” cu o referință URI:

ATAșați: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Set de caractere

Deși schema implicită de set de caractere pentru un iCalendar este UTF-8, nu este specificat niciun parametru de proprietate pentru a defini setul de caractere al unei valori de proprietate. în transferurile MIME, parametrul „charset” TREBUIE utilizat pentru setul de caractere existent.

## Referințe

* [Specificația obiectului principal pentru calendarul și programarea internetului](https://www.ietf.org/rfc/rfc5545.txt)
* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)
* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)

