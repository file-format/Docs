{
"data": "2023-06-08",
  "keywords": [
"fișier crx",
"Ce este un fișier crx",
"cum se instalează fișierul crx în google chrome",
"cum se deschide fișierul crx",
"ce conține fișierul crx",
"care este formatul fișierului crx",
"fişier",
"extensie fișier crx",
"extensie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format fișier CRX - Extensie Google Chrome",
  "description":"Aflați despre formatul CRX și despre API-urile care pot crea și deschide fișiere CRX.",
  "linktitle": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx",
      "parent": "misc"
}
},
"lastmod": "2023-06-08"
}

## Ce este un fișier CRX?

Formatul de fișier CRX este asociat cu extensiile browserului Google Chrome. Un fișier CRX este în esență un pachet comprimat care conține fișierele și metadatele necesare pentru ca o extensie să fie instalată și rulată în Google Chrome. Îmbunătățește funcționalitatea sau aspectul unui browser web oferind o funcție sau o temă suplimentară.

Când un fișier CRX este descărcat și instalat în Google Chrome, browserul verifică integritatea extensiei folosind cheia publică și semnătura. Dacă verificarea are succes, Chrome extrage conținutul fișierului CRX și instalează extensia, făcându-l disponibil pentru utilizare. Utilizatorii își pot gestiona extensiile prin intermediul paginii Extensii Chrome, care permite activarea, dezactivarea sau eliminarea extensiilor instalate.

## Cum se instalează fișierul CRX în Google Chrome?

Pentru a instala un fișier CRX în Google Chrome, puteți urma acești pași:

1. Deschideți browserul Chrome.
2. Tastați `chrome://extensions` în bara de adrese și apăsați Enter.
3. Activați comutatorul de comutare "Mod dezvoltator" situat în colțul din dreapta sus al paginii Extensii.
4. Faceți clic pe butonul "Încărcați despachetat".
5. Localizați și selectați folderul care conține conținutul extras al fișierului CRX (sau pur și simplu selectați fișierul CRX însuși).
6. Faceți clic pe "Deschidere" pentru a instala extensia.

## Ce conține fișierul CRX?

Un fișier CRX conține fișierele și metadatele necesare pentru extensia Google Chrome. Iată o detaliere a conținutului tipic găsit într-un fișier CRX:

- **Fișier manifest (manifest.json):** Acest fișier este un fișier formatat JSON care include informații despre extensia, cum ar fi numele, versiunea, descrierea, permisiunile și scripturile de fundal. Acesta definește structura și comportamentul extensiei.
- **Fișiere JavaScript:** Aceste fișiere conțin codul care definește funcționalitatea extensiei. Acestea pot include scripturi pentru gestionarea evenimentelor, modificarea paginilor web sau interacțiunea cu API-urile Chrome.
- **Fișiere HTML, CSS și imagine:** Extensiile includ adesea elemente de interfață cu utilizatorul, cum ar fi ferestre pop-up sau pagini cu opțiuni. Fișierele HTML definesc structura acestor interfețe, în timp ce fișierele CSS le controlează aspectul. Fișierele imagine sunt folosite pentru pictograme sau alte elemente grafice.
- **Fișiere cu resurse opționale:** Extensiile pot include resurse suplimentare, cum ar fi fișierele de localizare pentru acceptarea mai multor limbi. Aceste fișiere conțin traduceri ale textului utilizat în interfața de utilizator a extensiei.
- **Scripturi de fundal:** Dacă o extensie are procese de fundal sau scripturi care rulează independent de pagina web activă, aceste scripturi vor fi incluse în fișierul CRX.
- **Scripturi de conținut:** Scripturile de conținut sunt scripturi care pot fi injectate în paginile web pentru a le modifica comportamentul sau a interacționa cu conținutul lor. Dacă extensia folosește scripturi de conținut, fișierele necesare pentru acele scripturi vor fi prezente în fișierul CRX.
- **Alte active:** În funcție de cerințele specifice de extensie, pot fi incluse fișiere suplimentare, cum ar fi fișiere audio sau video, fonturi sau fișiere de date.

Formatul de fișier CRX este în esență un pachet comprimat care conține toate aceste fișiere și foldere într-o manieră structurată. Când fișierul CRX este instalat în Google Chrome, browserul extrage conținutul și îl plasează în locații adecvate, permițând încărcarea și rularea extensiei în browser.

## Care este formatul fișierului CRX?

Formatul de fișier CRX este un format specific pentru ambalarea și distribuirea extensiilor Google Chrome. Este, în esență, o arhivă ZIP comprimată cu extensii de fișiere diferite. Structura de bază a fișierului CRX este următoarea:

- **Semnătura fișierului:** primii 4 octeți ai fișierului conțin numărul magic "Cr24" (hexazecimal: 43 72 32 34) care servește ca semnătură pentru a identifica fișierul ca fișier CRX.
- **Numărul versiunii:** Următorii 4 octeți reprezintă numărul versiunii formatului CRX.
- **Lungimea cheii publice:** Următorii 4 octeți indică lungimea cheii publice codificate utilizate pentru verificarea semnăturii extensiei.
- **Lungimea semnăturii:** Cei 4 octeți următori specifică lungimea semnăturii extensiei.
- **Cheie publică:** Această secțiune conține cheia publică codificată utilizată pentru verificarea integrității extensiei.
- **Semnătura:** Această secțiune conține semnătura extensiei, care este generată prin semnarea conținutului extensiei folosind o cheie privată corespunzătoare cheii publice menționate mai sus.
- **Arhivă ZIP:** Octeții rămași ai fișierului CRX cuprind o arhivă ZIP comprimată. Această arhivă conține toate fișierele și folderele de extensie necesare, inclusiv fișierul manifest, fișierele JavaScript, fișierele HTML, fișierele CSS, imaginile și orice alte resurse.

## Referințe
* [Specificație format CRX](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)

