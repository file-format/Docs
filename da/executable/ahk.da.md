{
  "date": "2022-04-25",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om AHK-filformat og API'er, der kan oprette og åbne AHK-filer.",
  "title": "AHK-filformat - AutoHotkey-scriptfil",
  "linktitle": "AHK",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ah-dak"
}
},
  "lastmod": "2022-04-25"
}

## Hvad er AHK fil?

En AHK-fil er en scriptfil, der er genereret med AutoHotkey-softwareapplikation, der bruges til automatisering af opgaver i Microsoft Windows. Den indeholder instruktioner til automatisering af opgaver ved hjælp af genvejstaster, der kan bruges til at udføre øjeblikkelige handlinger. Filen udføres af AutoHotkey, og alle handlinger udføres sekventielt. AHK-filer er kraftige nok til at udføre komplekse opgaver ved hjælp af genvejstaster, der er defineret ved hjælp af genvejstaster. AHK-filer kan åbnes med teksteditorer som Microsoft Notepad og Notepad++.

## AHK filformat

AHK-filer gemmes på disken som almindelige tekstfiler og indeholder kodelinjer, der kan udføres af AutoHotkey. AutoHotkey er et gratis open source scriptsprog og giver brugerne mulighed for at skabe enkle til komplekse scripts for at udføre handlinger såsom formularudfyldere, auto-klik, eksekvering af makroer osv. En AHK-fil kan som minimum udføre en enkelt handling og derefter afslutte .

Der er tilgængelige værktøjer, som kan bruges til at konvertere AHK til [Exe](/executable/exe/) filer.

### AHK Eksempel

Følgende eksempel bruger Win+Z-tasten til at køre Microsoft Notesblok eller bringe den foran, hvis den allerede kører.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## Hvordan opretter jeg en AHK-fil?

De følgende trin kan bruges til at oprette en AHK-fil. Disse antager, at AutoHotkey allerede er installeret på maskinen.

* Højreklik på dit skrivebord.

* Find "Ny" i menuen.

* Klik på "AutoHotkey Script" i menuen "Ny".

* Giv scriptet et nyt navn.

* Find den nyoprettede fil på dit skrivebord, og højreklik på den.

* Klik på "Rediger script".

* Et vindue skulle være dukket op, sandsynligvis Notesblok.

* Gem filen.


## Referencer

* [AutoHotkey](https://www.autohotkey.com/)

* [Batch-fil - af Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)


