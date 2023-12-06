{
"data": "2023-03-07",
  "keywords": [
"fișier reg",
"ce este un fișier reg",
"fişier",
"extensia fișierului reg",
"extensie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format de fișier REG - fișierul de registru Windows",
  "description":"Aflați despre formatul REG și despre API-urile care pot crea și deschide fișiere REG.",
"linktitle": "REG",
  "menu": {
    "docs": {
      "identifier": "system-reg",
      "parent": "system"
}
},
"lastmod": "2023-03-07"
}

## Ce este un fișier REG?

Un fișier REG este un format de fișier utilizat pentru a importa sau exporta date din Registrul Windows. Registrul Windows este o bază de date ierarhică care stochează setările de configurare și opțiunile pentru sistemul de operare Windows și aplicațiile instalate. Registrul conține informații precum preferințele utilizatorului, setările aplicației, datele de configurare hardware și software și multe altele.

Un fișier REG are de obicei o extensie de fișier ".reg" și este un fișier text simplu care conține o serie de intrări și valori de registry într-un format specific. Formatul constă dintr-o secțiune antet care identifică fișierul ca fișier de registry, urmată de o serie de perechi cheie și valoare care reprezintă intrări de registry.

## Format fișier REG - Mai multe informații

Iată un exemplu de format de fișier reg:

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

Prima linie a fișierului specifică versiunea editorului de registry. Următoarele rânduri conțin intrările de registry în formatul unei căi de cheie urmată de un nume de valoare și date de valoare. În acest exemplu, fișierul reg conține două intrări: una care adaugă un program numit "Example.exe" la lista de pornire Windows și alta care setează valoarea "Hidden" din setările avansate Windows Explorer la "adevărat".

Fișierele reg pot fi create și editate folosind un editor de text, cum ar fi Notepad. Ele sunt adesea folosite pentru backup și restaurare, precum și pentru configurarea mai multor computere cu aceleași setări de registry.

## Importați sau exportați registrul Windows

Un fișier REG este un tip de fișier utilizat pentru a importa sau exporta date din Registrul Windows. Registrul Windows este o bază de date ierarhică care stochează setările de configurare și opțiunile pentru sistemul de operare Windows și aplicațiile instalate. Registrul conține informații precum preferințele utilizatorului, setările aplicației, datele de configurare hardware și software și multe altele.

Fișierele de regulă pot fi folosite pentru a crea sau modifica intrările de registry și sunt adesea folosite în scopuri de backup și restaurare, precum și pentru configurarea mai multor computere cu aceleași setări de registry. Iată cum să utilizați un fișier reg pentru a adăuga o nouă intrare în registry la Windows Registry:

1. Creați un fișier text nou utilizând un editor de text, cum ar fi Notepad.
2. Introduceți intrarea din registry în formatul corect. Formatul constă dintr-o secțiune antet care identifică fișierul ca fișier de registry, urmată de o serie de perechi cheie și valoare care reprezintă intrări de registry. Iată un exemplu:

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

Aceasta creează o nouă cheie numită "Exemplu" sub cheia "Software" din registrul utilizatorului curent și setează valoarea "Setting1" la "Value1".

3. Salvați fișierul cu extensia de fișier .reg.
4. Faceți dublu clic pe fișierul .reg pentru a adăuga noua intrare din registry la Registrul Windows.

Vi se va solicita să confirmați că doriți să adăugați intrarea în registry. Odată ce confirmați, noua intrare va fi adăugată la registry și o puteți verifica folosind instrumentul Editor de registru.

## Referințe
* [Registrul Windows](https://en.wikipedia.org/wiki/Windows_Registry)

