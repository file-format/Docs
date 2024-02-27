{
  "date": "2023-03-07",
  "keywords": [
"reg fil",
"hvad er en reg fil",
"fil",
"reg filtypenavn",
"udvidelse"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "REG-filformat - Windows-registreringsfil",
  "description": "Lær om REG-format og API'er, der kan oprette og åbne REG-filer.",
  "linktitle": "REG",
  "menu": {
    "docs": {
      "identifier": "system-reg-da",
      "parent": "system"
}
},
  "lastmod": "2023-03-07"
}

## Hvad er REG fil?

En REG-fil er et filformat, der bruges til at importere eller eksportere Windows-registreringsdatabasedata. Windows-registreringsdatabasen er en hierarkisk database, der gemmer konfigurationsindstillinger og muligheder for Windows-operativsystemet og installerede applikationer. Registret indeholder oplysninger såsom brugerpræferencer, applikationsindstillinger, hardware- og softwarekonfigurationsdata og mere.

En REG-fil har typisk en .reg filtypenavn og er en almindelig tekstfil, der indeholder en række registreringsposter og værdier i et bestemt format. Formatet består af en overskriftssektion, der identificerer filen som en registreringsfil, efterfulgt af en række nøgle- og værdipar, der repræsenterer registreringsposter.

## REG-filformat - flere oplysninger

Her er et eksempel på et reg filformat:

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

Den første linje i filen angiver versionen af registreringseditoren. De følgende linjer indeholder registreringsdatabasen i formatet af en nøglesti efterfulgt af et værdinavn og værdidata. I dette eksempel indeholder reg-filen to poster: en, der tilføjer et program kaldet Example.exe til Windows-startlisten, og en anden, der indstiller Skjult-værdien i Windows Stifinders avancerede indstillinger til true.

Reg-filer kan oprettes og redigeres ved hjælp af en teksteditor, såsom Notesblok. De bruges ofte til sikkerhedskopiering og gendannelse, såvel som til at konfigurere flere computere med de samme indstillinger i registreringsdatabasen.

## Importer eller eksporter Windows-registreringsdatabasen

En REG-fil er en filtype, der bruges til at importere eller eksportere data fra Windows-registreringsdatabasen. Windows-registreringsdatabasen er en hierarkisk database, der gemmer konfigurationsindstillinger og muligheder for Windows-operativsystemet og installerede applikationer. Registret indeholder oplysninger såsom brugerpræferencer, applikationsindstillinger, hardware- og softwarekonfigurationsdata og mere.

Reg-filer kan bruges til at oprette eller ændre registreringsposter, og de bruges ofte til sikkerhedskopiering og gendannelsesformål samt til at konfigurere flere computere med de samme registreringsindstillinger. Sådan bruger du en reg-fil til at tilføje en ny post i registreringsdatabasen til Windows-registreringsdatabasen:

1. Opret en ny tekstfil ved hjælp af en teksteditor, såsom Notesblok.
2. Indtast registreringsdatabasen i det korrekte format. Formatet består af en overskriftssektion, der identificerer filen som en registreringsfil, efterfulgt af en række nøgle- og værdipar, der repræsenterer registreringsposter. Her er et eksempel:

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

Dette opretter en ny nøgle kaldet Eksempel under Software-nøglen i den aktuelle brugers registreringsdatabase og sætter værdien Setting1 til Value1.

3. Gem filen med filtypenavnet .reg.
4. Dobbeltklik på .reg-filen for at tilføje den nye post i registreringsdatabasen til Windows-registreringsdatabasen.

Du vil blive bedt om at bekræfte, at du vil tilføje posten til registreringsdatabasen. Når du har bekræftet, vil den nye post blive tilføjet til registreringsdatabasen, og du kan bekræfte den ved hjælp af værktøjet Registreringseditor.

## Referencer
* [Windows Registry](https://en.wikipedia.org/wiki/Windows_Registry)


