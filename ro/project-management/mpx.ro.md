{
  "date" : "2019-10-11",
  "keywords" :[ "fișier mpx", "format fișier mpx", "ce este un fișier mpx", "fișier", "exemplu mpx", "extensie fișier mpx", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPX - Format de fișier Microsoft Project Exchange",
  "description":"Aflați despre formatul de fișier MPX și despre API-urile care pot crea și deschide fișiere MPX.",
  "linktitle" : "MPX",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## Ce este un fișier MPX? ##

Un fișier cu extensia .mpx este un format de fișier Microsoft Exchange. Un format de fișier MPX a fost dezvoltat de Microsoft Project (MSP) pentru a facilita schimbul de informații despre proiect între MSP și alte aplicații care acceptă formatul de fișier MPX, inclusiv Primavera Project Planner, Sciforma și Timerline Precision Estimating. Folosind fișierele MPX, puteți transfera tot felul de informații dintr-un proiect într-un sistem diferit, cum ar fi informații detaliate despre atribuirea resurselor, informații despre calendar sau informații din caseta de dialog Informații despre proiect.

Microsoft Project 4.0 a introdus suport pentru crearea și citirea formatelor de fișiere MPX care au continuat să fie utilizate prin Microsoft Project 98. Cu toate acestea, suportul pentru crearea fișierelor MPX a întrerupt lansarea Microsoft Project 2000, iar versiunile până la Microsoft Project 2010 acceptă doar citirea MPX. Formatul de fișier MPX nu este acceptat în versiunile ulterioare MSP 2010.

## Format fișier MPX ##

O prezentare generală a specificațiilor fișierului MPX este oferită în această secțiune. Specificațiile complete pot fi găsite în această [Bază de cunoștințe](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) articol și poate fi consultat pentru detalii.

### Înregistrări ###

O înregistrare a fișierului MPX constă în informații pentru proiect. Există diferite tipuri de înregistrări în care fiecare înregistrare are propria sa ordine. Fiecare tip de înregistrare este identificat prin numărul său de înregistrare. Pentru un fișier MPX, este necesar să conțină tipul de înregistrare File Creation. Alte tipuri de înregistrări nu sunt obligatorii. Următorul tabel prezintă toate tipurile de înregistrări, numerele lor de înregistrare și numărul de înregistrări pe care fiecare tip le poate conține în fișierul MPX. Includerea înregistrărilor în fișierul MPX trebuie să urmeze ordinea tabelului, cu comentarii introduse oriunde.

|Nume înregistrare|Număr înregistrare|Număr maxim de înregistrări
---|---|---|
|Crearea fișierului (obligatoriu)|niciunul|1
|Setări valutare|10|1
|Setări implicite|11|1
|Setări de dată și oră|12|1
|Definiție calendar de bază|20|250
|Ore calendaristice de bază|25| 7 pe înregistrarea definiției calendarului de bază
|Excepția calendarului de bază|26| 250 per înregistrarea definiției calendarului de bază
|Antetul proiectului|30|1
|Text Resource Table Definition|140|1- (Sau puteți utiliza înregistrarea Numeric Resource Table Definition)
|Definiția tabelului de resurse numerice|41|1
|Resursa|50|9.999
|Note de resurse|51| 1 per înregistrare de resurse
|Definiția calendarului resurselor|55| 1 per înregistrare de resurse
|Resurse Calendar Ore|56| 7 pe calendar de resurse
|Excepția calendarului de resurse| 57|250 pe calendar de resurse
|Text Task Table Definition|60|1 (Sau puteți utiliza înregistrarea Numeric Task Table Definition)
|Definiția tabelului de sarcini numerice|61|1
|Sarcina|70|9
|Note sarcini|71| 1 pe înregistrarea sarcinii
|Sarcina recurentă|72| 1 pe înregistrarea sarcinii
|Alocarea resurselor|75| 100 pe înregistrarea sarcinii
|Câmpuri Grup de lucru de atribuire|76| 1 per fișă de sarcină
|Nume proiecte|80|500
|Legături client DDE și OLE|81|500
|Comentarii|0|nelimitat

### Structura fișierului ###

Un fișier MPX constă din înregistrările menționate mai sus care sunt aranjate într-o manieră prestabilită în interiorul fișierului. Detaliile despre aceste tipuri de înregistrări sunt discutate după cum urmează:

**File Creation Record (FCR):** Aceasta este o înregistrare obligatorie al cărei scop este de a identifica:

* Format de fișier (MPX)
* Caracterul separator de listă utilizat în fișier
* Numărul programului și al versiunii utilizate pentru a crea fișierul
* Numărul versiunii formatului de fișier MPX utilizat în fișier
* Pagina de cod folosită pentru a crea fișierul

Aceasta trebuie să fie prima înregistrare din fișier. Când exportați din Microsoft Project, caracterul de separare a listei este specificat în elementul Setări regionale din Panoul de control Windows. O înregistrare FCR include următoarele câmpuri:

* MPX urmat imediat de caracterul separator de listă
* Numele/identificatorul programului
* Numărul versiunii fișierului
* Pagina de cod (850, 437, MAC, ANSI)

De exemplu, înregistrarea poate conține informații **MPX, Microsoft Project, 3.0**, care specifică faptul că o virgulă este utilizată ca caracter separator de listă în acest fișier MPX. Versiunea formatului MPX utilizată în fișier este exportată din Microsoft Project versiunea 3.0.

**Setări valutar** Această înregistrare, având numărul de înregistrare 10, specifică setările pentru opțiunile valutare din caseta de dialog Opțiuni. Dacă această înregistrare nu este inclusă, se utilizează setările curente din caseta de dialog Opțiuni. Separatorii de mii și zecimale sunt specificați în elementul Setări regionale din Panoul de control Windows.
Câmpurile incluse în această înregistrare sunt:

* Simbol Valută
* Poziția simbolului (0 # după, 1 # înainte, 2 # după cu un spațiu, 3 # înainte cu un spațiu)
* Cifre valutare (0,1,2)
* Separator de mii
* Separator zecimal

**Exemplu:** 10,$,1,2,",",.
Acest exemplu specifică faptul că valorile valutare includ un semn dolar ($) înaintea lor, că două cifre sunt incluse după virgulă zecimală, că o virgulă este folosită pentru a separa miile și că o punct este folosită ca virgulă zecimală. Deoarece caracterul separator de listă este inclus în câmpul Separator de mii, câmpul este înconjurat de ghilimele.

**Setări implicite:** Această înregistrare, având numărul de înregistrare 11, specifică setările pentru opțiunile implicite din caseta de dialog Opțiuni. Dacă nu este specificată o durată, unitatea de durată implicită trebuie setată pentru calculele corecte ale unității de durată. Dacă această înregistrare nu este inclusă, se utilizează setările curente din caseta de dialog Opțiuni.
Câmpurile incluse în această înregistrare sunt:

* Unități de durată implicite (0 # minute, 1 # ore, 2 # zile, 3 # săptămâni)
* Tip de durată implicit (0 # nu este fix, 1 # fix)
* Unități de lucru implicite (0 # minute, 1 # ore, 2 # zile, 3 # săptămâni)
* Ore/zi implicite
* Ore/Săptămână implicite
* Tarif standard implicit
* Rata implicită pentru orele suplimentare
* Actualizarea stării sarcinii Actualizează starea resurselor (0 # nu, 1 # da)
* Împărțiți sarcini în curs (0 # nu, 1 # da)

**Setări de dată și oră:** Această înregistrare, având numărul de înregistrare 12, specifică setările pentru opțiunile de dată și oră din caseta de dialog Opțiuni și opțiunea Format data text bară din caseta de dialog Aspect. Dacă această înregistrare nu este inclusă, se utilizează setările curente din caseta de dialog Opțiuni.
\\Câmpurile incluse în această înregistrare sunt:

* Data comenzii (0 # lună/zi/an, 1 # zi/lună/an, 2 # an/lună/zi)
* Format oră (0 # 12 ore, 1 # 24 ore)
* Ora implicită (număr de minute după miezul nopții)
* Separator de date
* Separator de timp
* 0:00 - 11:59 Text
* 12:00 - 23:59 Text
* Format data (0 -14)*
* Format de dată text bară (0 -194)*

**Definiția calendarului de bază:** Aceste înregistrări, având numărul de înregistrare 20, definesc calendarele de bază și zilele lor lucrătoare și nelucrătoare ale săptămânii. Setările implicite sunt utilizate dacă nu există nicio intrare pentru o zi. Setările implicite sunt de luni până vineri pentru zilele lucrătoare și sâmbătă și duminică pentru zilele nelucrătoare. În această înregistrare, câmpul Nume este obligatoriu. Pentru fiecare dintre zile, o intrare de 0 indică faptul că ziua este o zi nelucrătoare, iar o intrare de 1 indică faptul că ziua este o zi lucrătoare.
Câmpurile incluse în această înregistrare sunt:

* Nume
* Duminică
* Luni
* Marți
* Miercuri
* Joi
* Vineri
* Sambata

**Ore calendaristice de bază:** Aceste înregistrări, având numărul de înregistrare 25, specifică orele de lucru pentru zilele săptămânii dacă diferă de setările implicite. Orele de lucru implicite sunt 8:00 AM până la 12:00 PM și 1:00 PM până la 5:00 PM Fiecare înregistrare de ore de bază calendaristice se referă la înregistrarea anterioară de definire a calendarului de bază. Până la șapte dintre aceste înregistrări pot urma fiecare înregistrare a definiției calendarului de bază.

* Ziua săptămânii (1 - 7, unde 1 # duminică și 7 # sâmbătă)
* Din timpul 1
* La ora 1
* Din Timpul 2
* La ora 2
* Din Timpul 3
* La ora 3

**Excepție calendaristică de bază:** Aceste înregistrări, având numărul de înregistrare 26, definesc excepțiile de la zilele și orele specificate în cele două tipuri de înregistrări anterioare. Până la 250 dintre aceste înregistrări pot urma fiecare înregistrare a definiției calendarului de bază. Aceste înregistrări trebuie listate în ordine cronologică. Dacă o excepție este de o zi, puteți lăsa câmpul Până la data gol. Dacă nu sunt indicate ore, se utilizează orele implicite de 8:00 AM până la 12:00 PM și 1:00 PM până la 5:00 PM.
Câmpurile incluse în această înregistrare sunt:

* Din data
* Până în prezent
* Nefuncționează/funcționează (0 # nefuncționează, 1 # lucrează)
* Din timpul 1
* La ora 1
* Din Timpul 2
* La ora 2
* Din Timpul 3
* La ora 3

** Antet proiect: ** Această înregistrare, având valoarea de înregistrare 30, setează câmpuri globale ale proiectului, cum ar fi data de începere a proiectului și data de încheiere a proiectului. Câmpurile din această înregistrare corespund informațiilor din casetele de dialog Informații despre proiect și Statistici.
Câmpurile și filele incluse în această înregistrare sunt:

* Fila Proiect
* Companie
* Administrator
* Calendar (utilizat standard dacă nu există nicio intrare)
* Data de începere (fie acest câmp, fie următorul câmp este calculat pentru un fișier importat, în funcție de setarea Programare de la)
* Data de încheiere
* Program de la (0 # începere, 1 # terminare)
* Data curenta*
* Comentarii
* Cost
* Costul de referință
* Costul actual
* Muncă
* Lucrări de bază
* Munca reală
* Muncă
* Durată*
* Durata de referință*
* Durata reală
* Procent completat
* Început de bază
* Finisare de bază
* Început real
* Finisare reală
* Start Variance
* Varianta de finisare
* Subiect
* Autor
* Cuvinte cheie

**Text Resource Table Definition**: Această înregistrare listează câmpurile de resurse, în ordine, care sunt importate sau exportate. Pentru fișierele importate, numele trebuie să se potrivească cu numele câmpurilor utilizate în Microsoft Project. Pentru fișierele exportate, această înregistrare provine din tabelul Export de resurse. Trebuie utilizată fie această înregistrare, fie înregistrarea Numeric Resource Table Definition. La exportul din Microsoft Project, ambele înregistrări sunt incluse.

**Definiția tabelului de resurse numerice:** Folosind numere mai degrabă decât nume, această înregistrare listează câmpurile de resurse, în ordine, care sunt importate sau exportate. Aceasta este o metodă alternativă pentru identificarea câmpurilor de resurse incluse în fiecare înregistrare de resurse și este utilă atunci când definiți un fișier MPX creat de un produs în limbă străină.

**Resursa:** Aceste înregistrări conțin informații pentru fiecare resursă importată sau exportată. Fiecare înregistrare de resursă descrie o resursă. Când importați informații, câmpurile care sunt incluse sunt definite de înregistrarea Definiție tabel de resurse text sau de înregistrarea Definiție de tabel de resurse numerice. Când exportați informații, câmpurile care sunt incluse sunt cele enumerate în tabelul Export resursă.

**Note de resurse:** Aceste înregistrări conțin note despre înregistrarea de resurse imediat anterioară. Pentru o nouă linie din notă, este folosit caracterul ASCII 127. Dacă nota include caracterul separator de listă, includeți nota între ghilimele.

**Definiția calendarului resurselor:** Aceste înregistrări definesc zilele lucrătoare pentru resursa specificată în înregistrarea resursă imediat anterioară. Pentru fișierele importate, dacă nu există nicio intrare pentru câmpul Nume calendar de bază, se utilizează Standard. Nicio intrare pentru ziua respectivă indică faptul că ziua este setată la valoarea implicită (2). Dacă nu există înregistrări de definiție a calendarului resurselor, Standard este utilizat ca calendar de bază pentru resursă, implicit utilizat pentru zile. Pentru fiecare dintre zile, o intrare de 0 indică faptul că ziua este o zi nelucrătoare, 1 indică faptul că ziua este o zi lucrătoare, iar 2 specifică că este utilizată implicit.

**Ore calendaristice resurse:** Aceste înregistrări definesc orele de lucru pentru resursă care diferă de calendarul de bază utilizat de resursă. Aceste înregistrări se aplică înregistrării Definiție calendar de resurse imediat anterioară acestei înregistrări. Până la șapte dintre aceste înregistrări pot urma fiecare înregistrare de definiție a calendarului de resurse.

**Excepția calendarului de resurse:** Aceste înregistrări definesc excepțiile de la zilele și orele specificate în cele două tipuri de înregistrări anterioare. Până la 250 dintre aceste înregistrări pot urma fiecare înregistrare de definiție a calendarului de resurse. Aceste înregistrări trebuie listate în ordine cronologică. Dacă excepția este de numai o zi, puteți lăsa câmpul Până la data gol. Dacă nu sunt indicate ore, se utilizează orele implicite de 8:00 AM până la 12:00 PM și 1:00 PM până la 5:00 PM.

**Text Task Table Definition:** Această înregistrare listează câmpurile de activitate, în ordine, care sunt importate sau exportate. Pentru fișierele importate, numele trebuie să se potrivească cu numele câmpurilor utilizate în Microsoft Project. Dacă fișierul este în curs de export, această înregistrare provine din tabelul de activitate Export. La exportul din Microsoft Project, ambele înregistrări sunt incluse. Câmpurile care sunt calculate de Microsoft Project, cum ar fi Început programat și Sfârșit programat, sunt ignorate dacă sunt importate. Dacă aveți date de începere sau de încheiere a activității care sunt fixe, utilizați câmpurile Tip de constrângere și Data de constrângere.

**Definiția tabelului de sarcini numerice:** Folosind numere mai degrabă decât nume, această înregistrare listează câmpurile de activitate, în ordine, care sunt importate sau exportate. Aceasta este o metodă alternativă pentru identificarea câmpurilor de activitate incluse în fiecare înregistrare de sarcină și este utilă atunci când definiți un fișier MPX creat de un produs în limbă străină.

**Sarcina:** Aceste înregistrări conțin informații pentru fiecare sarcină importată sau exportată. Fiecare înregistrare de sarcină descrie o sarcină. Când importați informații, câmpurile care sunt incluse sunt definite de înregistrarea Definiție tabel de sarcini text sau de înregistrarea Definiție tabel de sarcini numerice. Când exportați informații, câmpurile care sunt incluse sunt cele enumerate în tabelul Export de activități.

**Note de activitate:** Aceste înregistrări conțin note despre înregistrarea de activitate imediat anterioară. Utilizați caracterul ASCII 127 pentru a indica o nouă linie în notă. Dacă nota include caracterul separator de listă, includeți nota între ghilimele.

**Alocarea resurselor**: Aceste înregistrări listează informații despre resursele atribuite sarcinii care a fost definită în înregistrarea Sarcină anterioară. Dacă îmbinați fișiere și doriți să păstrați informațiile privind atribuirea resurselor, trebuie să includeți informațiile în fișierul MPX. Dacă îmbinați, toate sarcinile existente pentru sarcinile îmbinate vor fi șterse. Dacă îmbinați fișiere pe baza ID-urilor unice, resursele sunt alocate folosind ID-urile unice de resurse, mai degrabă decât ID-urile.

**Câmpuri pentru grupul de lucru al atribuirii resurselor:** Aceste înregistrări listează informațiile care sunt stocate cu fiecare atribuire pentru caracteristicile grupului de lucru ale Microsoft Project 4.0 și 4.1. Dacă utilizați funcțiile Grupului de lucru, trebuie să includeți această înregistrare pentru a vă asigura că nicio informație nu se pierde.

**Nume proiecte:** Aceste înregistrări listează toate numele de linkuri DDE stocate în proiect.

**Legături client DDE și OLE:** Aceste înregistrări listează legăturile DDE în proiect.

**Comentarii:** Aceste înregistrări pot fi folosite pentru a adăuga comentarii la fișier și pot apărea în orice poziție din fișier. Fiecare înregistrare de comentarii trebuie să înceapă cu un „0”.

## Probleme la deschiderea unui fișier MPX ##

Iată lista unor probleme comune care pot apărea și pot cauza funcționarea defectuoasă a formatului MPX:

* Absența software-ului suport
* Fișier corupt
* Fișier infectat din cauza virusului
* Nu există drept de acces în sistem pentru a deschide fișierele
* Unitate învechită în sistemul dumneavoastră
* Extensia fișierului este redenumită

## Referințe ##

* [MPX - Microsoft Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)

