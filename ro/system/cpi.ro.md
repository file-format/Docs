{
"data":"2023-10-18",
   "keywords":[
"cpi",
"fișier cpi",
"fișier cu informații despre pagina de coduri CPI",
"cum se deschide un fișier cpi",
"fişier",
"extensie fișier cpi",
"extensie",
"fişier"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Format fișier CPI - Fișier cu informații despre pagina de cod",
   "description":"Aflați despre formatul de fișier CPI Codepage Information și despre API-urile care pot crea și deschide fișiere CPI.",
"linktitle":"CPI",
   "menu":{
      "docs":{
         "identifier":"system-cpi",
         "parent":"system"
}
},
"lastmod":"2023-10-18"
}

## Ce este un fișier CPI?

Un fișier `.cpi`, în contextul sistemelor de operare Microsoft Windows și DOS, este de obicei **"Fișier de informații privind pagina de coduri."** Aceste fișiere conțin informații despre paginile de cod utilizate pentru codificarea textului și maparea setului de caractere. Paginile de cod sunt esențiale pentru afișarea și procesarea textului în diferite limbi și seturi de caractere.

În contextul Windows și DOS, paginile de cod sunt folosite pentru a defini modul în care caracterele sunt reprezentate și codificate în diferite limbi și regiuni. Aceste pagini de coduri determină modul în care caracterele sunt stocate în memorie și afișate pe ecran. Fiecare pagină de coduri are un identificator unic și fișierele `.cpi` stochează informații despre aceste pagini de coduri, inclusiv detalii precum maparea caracterelor și informații despre fonturi.

Fișierele `.cpi` se găsesc în mod obișnuit în directoarele de sistem Windows sau DOS și joacă un rol crucial în a permite sistemului de operare să afișeze corect textul pentru diferite locații și seturi de caractere. Ele ajută sistemul să înțeleagă cum să interpreteze și să redea caractere din diferite limbi și codificări.

## Fișiere de informații din pagina de cod

Să aruncăm o privire mai atentă la fișierele de informații ale paginii de cod (.cpi) și la modul în care acestea funcționează în cadrul MS-DOS și al iterațiilor anterioare ale Microsoft Windows:

1. **Codificarea caracterelor și paginile de coduri**: paginile de coduri sunt o componentă critică a modului în care textul este codificat și afișat pe computer. Ele definesc codificarea caracterelor pentru un anumit limbaj sau set de caractere. Fiecare pagină de coduri atribuie valori numerice (puncte de cod) caracterelor, permițând computerului să le reprezinte și să le afișeze. De exemplu, pagina de coduri 437 este folosită în mod obișnuit în Statele Unite și Europa de Vest, în timp ce pagina de coduri 850 este folosită pentru codificarea Latin-1.
    







2. **Inițializarea sistemului**: În timpul inițializării sistemului (când pornește computerul), MS-DOS și versiunile mai vechi de Windows vor citi fișierele `.cpi` pentru a determina ce pagini de cod să accepte. Aceste informații au fost esențiale pentru redarea textului, introducerea de la tastatură și conversiile setului de caractere.
    







3. **Suport pentru afișaj și tastatură**: Aceste fișiere oferă informații despre modul în care caracterele ar trebui să fie afișate pe ecran și care seturi de caractere sau pagini de cod ar trebui să fie acceptate pentru introducerea tastaturii. Paginile de cod diferite definesc seturi de caractere diferite, astfel încât aceste fișiere ajută sistemul de operare să știe cum să gestioneze introducerea utilizatorului și să afișeze textul corect.
    







4. **Localizare**: fișierele `.cpi` sunt esențiale pentru localizarea sistemului de operare. Acestea permit sistemului să se adapteze la diferite limbi, regiuni și seturi de caractere, făcând posibil ca utilizatorii din întreaga lume să folosească MS-DOS sau Windows în limbile lor preferate.
    







5. **Mai multe fișiere `.cpi`**: pe computerul cu suport multilingv, este posibil să găsiți mai multe fișiere `.cpi` care corespund unor pagini de cod diferite. De exemplu, sistemul poate avea `437.cpi` pentru Statele Unite, `850.cpi` pentru Latin-1, `852.cpi` pentru Europa Centrală și așa mai departe. Fișierul corespunzător este încărcat pe baza localizării utilizatorului sau a paginii de cod selectate.
    







6. **Informații despre font**: Pe lângă mapările de caractere, aceste fișiere pot conține informații despre fonturi, specificând ce fonturi să folosească pentru fiecare pagină de cod. Acest lucru este important pentru redarea textului în stil și dimensiune corespunzătoare.
    







7. **Sisteme moștenite**: fișierele `.cpi` erau mai frecvente în versiunile mai vechi de MS-DOS și Windows. Versiunile moderne de Windows (cum ar fi Windows 10 și versiuni ulterioare) folosesc de obicei Unicode pentru codificarea textului, care acceptă o gamă largă de caractere și limbi. Unicode simplifică procesarea textului pentru medii multilingve și este standard pentru software-ul modern.

## Cum se deschide fișierul CPI?

Deschiderea fișierului .CPI (Code Page Information) nu este o acțiune tipică a utilizatorului și, în general, aceste fișiere nu sunt menite să fie deschise manual. Ele sunt utilizate de sistemul de operare pentru a gestiona codificarea textului și seturile de caractere, iar conținutul lor este accesat și utilizat automat de către sistem.

Cu toate acestea, dacă sunteți interesat să vizualizați conținutul fișierului .CPI în scopuri informative, puteți încerca să îl deschideți cu un editor de text sau un vizualizator hexazecimal. Iată cum puteți încerca să deschideți fișierul .CPI:

1. **Editor de text**: Puteți utiliza un editor de text precum Notepad (pe Windows) sau orice editor de text simplu pe alte sisteme de operare pentru a deschide și vizualiza fișierul .CPI. Rețineți că conținutul fișierelor .CPI nu este menit să fie citit de om și este posibil să vedeți serii de caractere greu de interpretat.
    







2. **Vizualizator hexazecimal**: Un vizualizator hexazecimal sau un editor hexazecimal poate fi folosit pentru a deschide și inspecta conținutul fișierului .CPI în forma sa binară brută. Editorii hexadecimale oferă o vizualizare mai detaliată a datelor fișierului, care poate fi utilă dacă încercați să înțelegeți structura acestuia. Exemple de astfel de software includ HxD, Hex Fiend (pentru macOS) și 010 Editor.

## Alte fișiere CPI

Iată și alte tipuri de fișiere care folosesc extensia de fișier **.cpi**.

**Video și sistem**
- [CPI - Informații despre videoclipul AVCHD](/ro/video/cpi/)
- [CPI - Fișier cu informații despre pagina de cod](/ro/system/cpi/)

## Referințe
* [Pagină de cod](https://en.wikipedia.org/wiki/Code_page)

