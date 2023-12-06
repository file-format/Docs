{
"data": "2023-06-12",
  "keywords": [
"bak",
"fișier bak",
"Marcaje BAK Chromium",
"Ce este un fișier bak",
"cum se deschide fișierul bak",
"fişier",
"extensie de fișier bak",
"extensie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "fals",
"toc": true,
"title": "Format fișier BAK - Backup pentru marcaje Chromium",
  "description":"Aflați despre formatul BAK Chromium Bookmarks și despre API-urile care pot crea și deschide fișiere BAK.",
"linktitle": "Marcaje BAK Chromium",
  "menu": {
    "docs": {
      "identifier": "misc-bak-chromium",
      "parent": "misc"
}
},
"lastmod": "2023-06-12"
}

## Ce este un fișier BAK?

Un fișier .bak în contextul browserelor web bazate pe Chromium, cum ar fi Google Chrome și Microsoft Edge, este în esență un fișier de rezervă al marcajelor dvs. Aceste marcaje sunt salvate ca o listă de text simplu, iar formatul de fișier utilizat este JSON. Scopul acestor fișiere .bak este de a vă proteja marcajele, oferind o copie de rezervă care poate fi restaurată în caz de ștergere sau pierdere accidentală.

Browserele bazate pe Chromium, inclusiv Google Chrome, creează în mod obișnuit aceste fișiere de rezervă și de obicei le dau numele "Bookmarks.bak". Ele sunt în esență un instantaneu al marcajelor dvs. într-un anumit moment în timp.

## Cum să utilizați un fișier .bak pentru a vă restaura marcajele

1. **Găsiți fișierul de rezervă:** se află de obicei într-un folder specific asociat cu profilul dvs. Chromium. Locația exactă poate varia în funcție de sistemul dvs. de operare.

Pe Windows: căutați în `C:\Users\<YourUsername> \AppData\Local\Chromium\User Data\Default\Bookmarks.bak`.

Pe macOS: Căutați în `~/Library/Application Support/Chromium/Default/Bookmarks.bak`.

Pe Linux: verificați `~/.config/chromium/Default/Bookmarks.bak`.

3. Asigurați-vă că browserul dvs. Chromium este închis.
4. Redenumiți fișierul "Bookmarks.bak" eliminând extensia ".bak", așa că se numește pur și simplu "Bookmarks".
5. Porniți Chromium.

Prin redenumirea fișierului .bak în "Marcaje", Chromium îl va folosi ca fișier de marcaje curent, iar marcajele dvs. anterioare ar trebui restaurate.

## Backup pentru marcaje Chromium

Copierea de rezervă a marcajelor dvs. Chromium este o măsură de precauție înțeleaptă pentru a vă asigura că nu vă pierdeți paginile web și adresele URL importante salvate. Chromium este un browser open-source care servește drept bază pentru alte browsere precum Google Chrome și Microsoft Edge. Pentru a face backup marcajelor dvs. Chromium, urmați acești pași:

## Metoda 1: Backup manual

1. **Deschideți Chromium**: Lansați browserul Chromium pe computer.

2. **Acces la Marcaje**: dați clic pe cele trei puncte verticale (pictograma meniului) din colțul din dreapta sus al ferestrei browserului. Din meniul drop-down, plasați cursorul peste "Marcaje" pentru a afișa submeniul de marcaje.

3. **Exportați marcaje**: în submeniul de marcaje, faceți clic pe "Manager de marcaje". Aceasta va deschide o filă nouă care va afișa marcajele dvs.

4. **Exportați marcaje**: în fila Manager de marcaje, faceți clic din nou pe cele trei puncte verticale (de obicei în colțul din dreapta sus) pentru a deschide meniul Manager de marcaje. Din acest meniu, selectați "Exportați marcaje".

5. **Alegeți locația**: alegeți unde doriți să salvați fișierul de marcaje exportat pe computer. Numele implicit de fișier este "bookmarks.html", dar îl puteți schimba dacă preferați. Salvați-l într-o locație de care vă veți aminti.

6. **Salvați**: faceți clic pe butonul "Salvați" sau "Exportați" pentru a salva marcajele ca fișier HTML.

Marcajele dvs. au fost acum salvate ca fișier HTML. Puteți copia acest fișier pe o unitate externă sau pe o stocare în cloud pentru păstrare.

## Metoda 2: sincronizați cu Contul Google (dacă este cazul)

Dacă sunteți conectat la un cont Google în Chromium, puteți utiliza și funcția de sincronizare încorporată pentru a vă păstra marcajele în siguranță și sincronizate pe toate dispozitivele. În acest fel, marcajele dvs. vor fi salvate automat în contul dvs. Google.

1. **Deschideți Chromium**: Lansați browserul Chromium și asigurați-vă că sunteți conectat la contul dvs. Google.

2. **Activați sincronizarea**: faceți clic pe cele trei puncte verticale (pictograma meniului) din colțul din dreapta sus al ferestrei browserului și accesați "Setări".

3. **Servicii de sincronizare și Google**: în fila Setări, faceți clic pe "Servicii de sincronizare și Google" din bara laterală din stânga.

4. **Sincronizați-vă datele**: sub "Sincronizare", asigurați-vă că "Marcaje" este activat. Aceasta vă va sincroniza marcajele cu contul dvs. Google.

Marcajele dvs. vor fi acum salvate automat și sincronizate cu contul dvs. Google. Le puteți accesa conectându-vă la contul dvs. Google de pe orice dispozitiv cu Chromium sau alt browser care acceptă sincronizarea Google.

Nu uitați să faceți periodic copii de siguranță ale marcajelor și manual, mai ales dacă doriți o copie locală care nu se bazează exclusiv pe sincronizarea contului dvs. Google.

## Cum se deschide un fișier BAK

Dacă doriți să explorați datele brute ale copiei de rezervă a marcajelor, puteți deschide fișierul "Bookmarks.bak" cu diverse editoare de text, cum ar fi Microsoft Visual Studio Code (disponibil pe mai multe platforme), Microsoft Notepad (pentru utilizatorii Windows), Apple TextEdit (pentru utilizatorii de Mac) sau orice alt editor de text la alegere. Acest lucru vă va permite să vizualizați marcajele și metadatele conținute în fișier.

Puteți deschide fișierul "Bookmarks.bak" și puteți vizualiza conținutul acestuia utilizând diverse programe de editare a textului și editori de cod. Iată câteva opțiuni frecvent utilizate:

1. Cod Visual Studio (Codul VS)
2. Notepad (Windows)
3. TextEdit (Mac)
4. Text sublim
5. Notepad++
6. Atom
7. nano și Vim (Linux)
8. WordPad (Windows)

## Alte fișiere BAK

Iată și alte tipuri de fișiere care folosesc extensia de fișier **.bak**.

**Bază de date**
- [BAK - Fișier de copiere a bazei de date](/ro/database/bak/)
- [BAK - Swiftpage Act! Backup baze de date](/ro/database/bak-act/)
- [BAK - Backup baze de date Microsoft SQL Server](/ro/database/bak-sqlserver/)

**Joc**
- [BAK - Terraria World sau Player Backup](/ro/game/bak-terraria/)

**Diverse**
- [BAK - Fișier de rezervă](/ro/misc/bak-backup/)
- [BAK - Backup scor final 2012](/ro/misc/bak-finale/)
- [BAK - Backup MobileTrans](/ro/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Backup](/ro/misc/bak-vegas/)

**Setari**
- [BAK - Backup Holo Launcher](/ro/settings/bak-holo/)

## Referințe
* [Chromium Bookmarks](https://www.chromium.org/user-experience/bookmarks/)
