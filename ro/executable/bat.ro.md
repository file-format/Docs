{
  "date" : "2021-06-24",
  "keywords" :[ "fișier bat", "ce este un fișier bat", "fișier", "exemplu de fișier bat", "extensie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier BAT și despre API-urile care pot crea și deschide fișiere BAT.",
  "title" :"BAT - Format de fișier lot",
  "linktitle" : "BAT",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-24"
}

## Ce este un fișier BAT?
Un fișier BAT este cunoscut ca fișier batch care rulează cu DOS și toate versiunile de Windows, sub cmd.exe. Acesta constă dintr-o serie de comenzi de linie în text simplu, care urmează să fie executate de interpretul de linie de comandă pentru a efectua diferite sarcini, cum ar fi rularea utilităților de întreținere în Windows sau pornirea programelor tipice. Un fișier batch poate include orice comandă care poate fi acceptată de interpret în mod interactiv și poate utiliza structura de cod care permite ramificarea condiționată și bucla așa cum este scrisă în fișierul batch.
## Format de fișier BAT
Un format de fișier BAT este pur și simplu un script încorporat pentru a automatiza secvențele de comenzi care sunt de natură repetitivă. Termenul „batch” este folosit pentru procesarea în lot, poate fi considerat „execuție non-interactivă”. Prin urmare, un fișier batch nu poate procesa un lot de date multiple. În vechiul sistem de operare pe disc (DOS), fișierul batch a fost rulat sub interfața liniei de comandă tastând numele fișierului și extensia .bat. Sistemul de operare anterior bazat pe interfața grafică Microsoft, cum ar fi Microsoft Windows, era dependent de DOS. Utilizatorii au trebuit să folosească DOS pentru a efectua operațiuni tipice precum repararea, optimizarea sau reinstalarea Windows. Mai târziu, Microsoft a introdus Windows NT, care nu depindea de sistemul de operare DOS. Prin urmare, fișierele batch pot fi rulate utilizând Command Prompt sau **cmd.exe** în sistemele de operare Microsoft moderne.
### Parametrii fișierului batch
Linia de comandă acceptă o serie de variabile speciale, cum ar fi **%0, %1 până la %9**, pentru a se referi la numele și calea jobului batch și la cei nouă parametri de apelare din cadrul jobului batch. Parametrii inexistenți sunt înlocuiți cu un șir de lungime zero. Deși, ele pot fi folosite similar cu variabilele de mediu, dar nu sunt salvate în mediu. Microsoft și IBM se referă la aceste variabile ca fiind parametri de înlocuire, în timp ce Novell, Digital Research și Caldera au introdus termenul de variabile de înlocuire pentru ele.

Iată câteva comenzi utile pentru fișiere Batch:
| Comanda | Descriere |
------|------------|
| VER | Această comandă de lot arată versiunea de MS-DOS pe care o utilizați. |
|ASSOC| Aceasta este o comandă de lot care asociază o extensie cu un tip de fișier (FTYPE), afișează asocierile existente sau șterge o asociere. |
|CD| Această comandă de lot vă ajută să faceți modificări într-un director diferit sau afișează directorul curent. |
|CLS| Această comandă de lot șterge ecranul. |
|COPIE| Această comandă batch este utilizată pentru a copia fișiere dintr-o locație în alta. |
|DEL| Această comandă batch șterge fișiere și nu directoare. |
|DIR| Această comandă batch listează conținutul unui director. |
|DATA| Această comandă de lot vă ajută să găsiți data sistemului. |
|ECHO| Această comandă de lot afișează mesaje sau activează sau dezactivează ecoul comenzii. |
|EXIT| Această comandă batch iese din consola DOS. |
|MD| Această comandă batch creează un director nou în locația curentă. |
|MUTA| Această comandă batch mută fișiere sau directoare între directoare. |
|CALEA| Această comandă batch afișează sau setează variabila cale. |
|PAUZĂ| Această comandă batch solicită utilizatorului și așteaptă introducerea unei linii de intrare. |
|PROMPT| Această comandă batch poate fi utilizată pentru a modifica sau reseta promptul cmd.exe. |
|RD| Această comandă batch elimină directoare, dar directoarele trebuie să fie goale înainte de a putea fi eliminate. |
|REN| Redenumește fișierele și directoarele |
|REM| Această comandă batch este utilizată pentru observațiile din fișierele batch, împiedicând executarea conținutului remarcii. |
|START| Această comandă batch pornește un program într-o fereastră nouă sau deschide un document. |
|TIMP| Această comandă lot setează sau afișează ora. |
|TIP| Această comandă lot imprimă conținutul unui fișier sau fișiere la ieșire. |
|VOL| Această comandă de lot afișează etichetele de volum. |
|ATTRIB| Afișează sau setează atributele fișierelor din directorul curent |
|CHKDSK| Această comandă lot verifică discul pentru orice problemă. |
|ALEGEREA| Această comandă lot oferă utilizatorului o listă de opțiuni. |
|CMD| Această comandă lot invocă o altă instanță de prompt de comandă. |
|COMP| Această comandă lot compară 2 fișiere în funcție de dimensiunea fișierului. |
|CONVERT| Această comandă batch convertește un volum din sistemul de fișiere FAT16 sau FAT32 în sistemul de fișiere NTFS. |
|DRIVERQUERY| Această comandă de lot arată toate driverele de dispozitiv instalate și proprietățile acestora. |
|EXPANDE| Această comandă batch extrage fișiere din fișierele cabinet .cab comprimate. |
|GĂSĂ| Această comandă batch caută un șir în fișiere sau intrări, producând linii care se potrivesc. |
|FORMAT| Această comandă batch formatează un disc pentru a utiliza sistemul de fișiere acceptat de Windows, cum ar fi FAT, FAT32 sau NTFS, suprascriind astfel conținutul anterior al discului. |
|AJUTOR| Această comandă lot arată lista comenzilor furnizate de Windows. |
|IPCONFIG| Această comandă batch afișează Windows IP Configuration. Afișează configurația după conexiune și numele acelei conexiuni. |
|LABEL| Această comandă de lot adaugă, setează sau elimină o etichetă de disc. |
|MAI MULT| Această comandă batch afișează conținutul unui fișier sau fișiere, câte un ecran. |
|NET| Oferă diverse servicii de rețea, în funcție de comanda utilizată. |
|PING| Această comandă batch trimite pachete „ecou” ICMP/IP prin rețea la adresa desemnată. |
|OPRIRE| Această comandă în lot oprește un computer sau deconectează utilizatorul curent. |
|SORTARE| Această comandă batch preia intrarea dintr-un fișier sursă și sortează conținutul acestuia în ordine alfabetică, de la A la Z sau de la Z la A. Tipărește rezultatul pe consolă. |
|SUBST| Această comandă lot atribuie o literă de unitate unui folder local, afișează atribuirile curente sau elimină o atribuire. |
|SYSTEMINFO| Această comandă de lot arată configurația unui computer și a sistemului său de operare. |
|TASKKILL| Această comandă batch încheie una sau mai multe sarcini. |
|LISTA DE SARCINI| Această comandă lot listează sarcini, inclusiv numele sarcinii și ID-ul procesului (PID). |
|XCOPIE| Această comandă batch copiază fișierele și directoarele într-un mod mai avansat. |
|COPAC| Această comandă batch afișează un arbore al tuturor subdirectoarelor din directorul curent la orice nivel de recursivitate sau profunzime. |
|FC |Această comandă batch listează diferențele reale dintre două fișiere. |
|DISKPART |Această comandă batch arată și configurează proprietățile partițiilor de disc. |
|TITLE |Această comandă lot setează titlul afișat în fereastra consolei. |
|SET | Afișează lista de variabile de mediu din sistemul curent. |

## Exemplu de fișier BAT
Scripturile batch sunt de obicei salvate ca fișiere text simple; care conțin comenzi care sunt executate într-o secvență. Aceste fișiere sunt salvate cu extensia .bat; recunoscut și executat prin utilizarea software-ului **Command Interpreter**. Acest software este disponibil nativ în Microsoft Windows cu numele **cmd.exe**.

Iată un exemplu de Script Batch care șterge toate fișierele din directorul curent:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## Referințe

* [Batch Script - Ghid rapid](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)
* [Fișier lot - de la Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

