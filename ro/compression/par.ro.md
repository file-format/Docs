{
"data":"2023-07-18",
   "keywords":[
"PAR",
"Fișier PAR",
"cum se deschide un fișier par",
"fişier",
"Extensie fișier PAR",
"extensie",
"fişier"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Format fișier PAR - Fișier index Parchive",
   "description":"Aflați despre formatul PAR și despre API-urile care pot crea și deschide fișiere PAR.",
"linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par",
         "parent":"compression"
}
},
"lastmod":"2023-07-18"
}

## Ce este un fișier PAR?

În arhivele Parchive (PAR), un fișier .par se referă la un fișier index care conține un grup de volume de paritate sau blocuri de paritate. Acest fișier index este utilizat pentru detectarea erorilor și în scopuri de recuperare atunci când unul sau mai multe fișiere din arhivă sunt pierdute sau deteriorate.

O arhivă Parchive constă de obicei atât din fișierele de date originale, cât și din volumele de paritate corespunzătoare. Volumele de paritate sunt create folosind algoritmi de corectare a erorilor Reed-Solomon. Aceste volume de paritate conțin informații redundante care pot fi folosite pentru a recupera fișierele de date originale.

Fișierul .par, cunoscut și ca un set de volume de paritate, conține informații despre structura și locația volumelor de paritate din arhivă. Acesta servește ca index sau hartă pentru procesul de recuperare. Folosind fișierul .par, software-ul PAR specializat poate determina ce volume de paritate sunt necesare și cum ar trebui utilizate pentru a reconstrui fișierele lipsă sau deteriorate.

Când unul sau mai multe fișiere din arhiva Parchive devin inaccesibile sau corupte, fișierul .par poate fi utilizat împreună cu volumele de paritate disponibile pentru a recupera datele pierdute. Software-ul PAR citește fișierul .par, identifică fișierele lipsă sau deteriorate și utilizează volumele de paritate pentru a le reconstrui.

## Cum se deschide un fișier PAR?

Pentru a deschide și utiliza fișiere .par, veți avea nevoie de software PAR specializat. Iată câteva opțiuni software populare care pot gestiona fișierele .par:

- **QuickPar:** QuickPar este un software PAR utilizat pe scară largă pentru Windows. Vă permite să creați, să verificați și să reparați fișiere PAR. Puteți deschide un fișier .par în QuickPar pentru a verifica integritatea acestuia sau îl puteți utiliza pentru a repara fișierele deteriorate sau lipsă dintr-o arhivă Parchive.

- **MultiPar:** MultiPar este un alt software PAR popular disponibil pentru Windows. Acceptă atât formatele de fișiere PAR, cât și PAR2 și oferă caracteristici avansate pentru crearea, verificarea și repararea arhivelor. MultiPar poate deschide fișiere .par și poate efectua operațiuni de detectare și recuperare a erorilor pe baza volumelor de paritate furnizate.

- **MacPAR deLuxe:** MacPAR deLuxe este un software PAR conceput special pentru macOS. Acceptă formatele de fișiere PAR și PAR2 și oferă funcționalități similare cu QuickPar și MultiPar. MacPAR deLuxe poate deschide fișiere .par și poate ajuta la verificarea arhivelor și la recuperarea fișierelor deteriorate sau lipsă.

## Format de fișier PAR - Mai multe informații

Formatul de fișier PAR, denumit în mod obișnuit Parchive, este un format de fișier specific utilizat pentru crearea datelor de paritate și efectuarea de detectare și recuperare a erorilor în arhivele de fișiere. Formatul de fișier PAR constă de obicei din trei tipuri: PAR, PAR2 și PAR3.

- **PAR:** Formatul original de fișier PAR, cunoscut și ca PAR1, a fost dezvoltat de proiectul Parchive. Include datele de paritate generate din fișierele de date originale. Fișierele PAR oferă un nivel de bază de detectare și recuperare a erorilor, dar au limitări în ceea ce privește capabilitățile de corectare a erorilor.

- **PAR2:** PAR2 este o versiune îmbunătățită a formatului de fișier PAR. Oferă capabilități mai avansate de corectare a erorilor și funcții de recuperare îmbunătățite. Fișierele PAR2 sunt utilizate de obicei pentru a crea date de paritate care pot recupera fișierele pierdute sau deteriorate dintr-o arhivă. Fișierele PAR2 oferă o protecție mai bună împotriva coruperii datelor și sunt utilizate pe scară largă în scopuri de arhivare a fișierelor.

- **PAR3:** PAR3 este cea mai recentă versiune a formatului de fișier PAR și oferă îmbunătățiri suplimentare în corectarea și recuperarea erorilor. Oferă niveluri și mai mari de redundanță și capabilități de corectare a erorilor în comparație cu PAR2. Fișierele PAR3 sunt concepute pentru a oferi opțiuni de protecție și recuperare mai robuste pentru datele stocate în arhive.

Ambele formate de fișiere PAR2 și PAR3 sunt acceptate pe scară largă de software-ul PAR și oferă posibilitatea de a verifica integritatea fișierelor dintr-o arhivă și de a recupera datele pierdute sau deteriorate. Fișierele PAR și PAR2 sunt încă utilizate în mod obișnuit, în timp ce fișierele PAR3 câștigă treptat adoptarea datorită capacităților lor îmbunătățite de corectare a erorilor.

## Referințe
* [Arhivă](https://en.wikipedia.org/wiki/Parchive)

