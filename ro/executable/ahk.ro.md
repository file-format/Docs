{
  "date" : "2022-04-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier AHK și despre API-urile care pot crea și deschide fișiere AHK.",
  "title" :"Format fișier AHK- Fișier script AutoHotkey",
  "linktitle" : "AHK",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-04-25"
}

## Ce este un fișier AHK?

Un fișier AHK este un fișier script generat cu aplicația software AutoHotkey care este utilizat pentru automatizarea sarcinilor în Microsoft Windows. Conține instrucțiuni pentru automatizarea sarcinilor folosind taste de comandă rapidă care pot fi folosite pentru a efectua acțiuni instantanee. Fișierul este executat de AutoHotkey și toate acțiunile sunt efectuate secvenţial. Fișierele AHK sunt suficient de puternice pentru a efectua sarcini complexe folosind tastele rapide definite folosind tastele rapide. Fișierele AHK pot fi deschise cu editori de text, cum ar fi Microsoft Notepad și Notepad++.

## Format de fișier AHK

Fișierele AHK sunt salvate pe disc ca fișiere text simplu și conțin linii de cod care pot fi executate de AutoHotkey. AutoHotkey este un limbaj de scripting gratuit, open-source și permite utilizatorilor să creeze scripturi simple până la complexe pentru a efectua acțiuni precum completarea formularelor, clicurile automate, executarea macrocomenzilor etc. Un fișier AHK poate efectua cel puțin o singură acțiune și apoi ieși .

Există instrumente disponibile care pot fi folosite pentru a converti fișierele AHK în [Exe](/ro/executable/exe/).

### AHK Exemplu

Următorul exemplu folosește tasta Win+Z pentru a rula Microsoft Notepad sau pentru a-l aduce în față dacă rulează deja.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## Cum creez un fișier AHK?

Următorii pași pot fi utilizați pentru a crea un fișier AHK. Acestea presupun că AutoHotkey este deja instalată pe mașină.

* Faceți clic dreapta pe desktop.
* Găsiți „Nou” în meniu.
* Faceți clic pe „Script AutoHotkey” în meniul „Nou”.
* Dați scriptului un nume nou.
* Găsiți fișierul nou creat pe desktop și faceți clic dreapta pe el.
* Faceți clic pe „Editare script”.
* Ar fi trebuit să apară o fereastră, probabil Notepad.
* Salvați fișierul.

## Referințe

* [AutoHotkey](https://www.autohotkey.com/)
* [Fișier lot - de la Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

