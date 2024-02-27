{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Shell script - Sådan kører du det på Ubuntu og Linux",
  "description":"Lær om, hvad der er Shell Script, og hvordan du kører det på Ubuntu og Linux",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-da",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## Hvad er Shell Script?

Shell scripting involverer at skrive en række kommandoer i en almindelig tekstfil, ofte omtalt som et **Shell Script**. Disse scripts udføres af en shell, som er en kommandolinjefortolker. De mest almindelige skaller omfatter

1. Bash (Bourne Again SHell)
2. Zsh (Z Shell)
3. Fisk.

Shell-scripts kan variere fra simple one-liners til komplekse programmer, og de bruges til at udføre en lang række opgaver, såsom filmanipulation, systemadministration og automatisering af gentagne opgaver.

## Fordele ved Shell Scripting:

1.  **Automation:** Shell-scripts giver brugerne mulighed for at automatisere gentagne opgaver, hvilket sparer tid og reducerer risikoen for menneskelige fejl.
    
2.  **Tilpasning:** Brugere kan oprette scripts, der er skræddersyet til deres specifikke behov, hvilket giver en høj grad af tilpasning.
    
3.  **Batchbehandling:** Shell-scripts er fremragende til at håndtere batchbehandlingsopgaver, hvor flere kommandoer skal udføres i rækkefølge.
    
4.  **Systemadministration:** Shell-scripts bruges almindeligvis til systemadministrationsopgaver, såsom sikkerhedskopier, logrotation og softwareinstallation.

## Sådan skriver du et simpelt Shell-script:

Lad os oprette et grundlæggende shell-script, der udskriver en hilsen. Åbn en teksteditor og opret en fil med navnet `greeting.sh`. Tilføj følgende linjer:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Gem filen og gør den eksekverbar ved at køre følgende kommando i terminalen:

```
chmod +x greeting.sh
```

Nu kan du udføre scriptet:

```
./greeting.sh
```

Output skal være:

```
Hello, welcome to the world of shell scripting!
```

## Kørsel af Shell-scripts på Ubuntu og Linux:

Nu vil vi diskutere **hvordan man kører en .sh-fil i Ubuntu og Linux**.

1.  **Gør scriptet eksekverbart:** Før du kører et shell-script, skal du sikre dig, at det er eksekverbart. Brug `chmod`-kommandoen som vist tidligere.
    
2.  **Naviger til scriptkataloget:** Åbn en terminal og brug `cd`-kommandoen til at navigere til den mappe, der indeholder dit shell-script.
    
3.  **Kør scriptet:** Udfør scriptet ved at skrive `./scriptname.sh` i terminalen, og erstatte scriptnavn med det faktiske navn på dit script.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Brug af Bash-kommandoen:** Hvis dit script begynder med `#!/bin/bash` (kendt som en **shebang**), kan du også køre det ved at bruge `bash`-kommandoen.

```
bash greeting.sh
```

## Hvad betyder $@ i Shell Script?

I shell-script repræsenterer `$@` alle de kommandolinjeargumenter, der sendes til scriptet. Det bruges ofte til at henvise til listen over argumenter som separate enheder. Når det bruges inden for dobbelte anførselstegn, som `$@`, bevarer det individuelle argumenter, der tager højde for mellemrum og specialtegn.

Her er en kort forklaring:

- `$@`: Repræsenterer alle positionelle parametre (argumenter) sendt til script eller funktion. Hvert argument behandles som et separat ord.
    
- `$@`: Når der anføres dobbelte anførselstegn, bevares adskillelse af argumenter, der tillader mellemrum eller specialtegn i individuelle argumenter.
    

Her er et simpelt eksempel til illustration:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Når du kører dette script med argumenter, for eksempel:

```
bash example.sh arg1 "argument 2" arg3
```

Det ville udsende:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Som du kan se, repræsenterer `$@` alle argumenter, og `$@` bevarer de individuelle argumenter, selvom de indeholder mellemrum.

