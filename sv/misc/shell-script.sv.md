{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Shell script - Hur man kör det på Ubuntu och Linux",
  "description":"Lär dig om vad som är Shell Script och hur du kör det på Ubuntu och Linux",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-sv",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## Vad är Shell Script?

Shell scripting innebär att skriva en serie kommandon i en vanlig textfil, ofta kallad **Shell Script**. Dessa skript exekveras av ett skal, som är en kommandoradstolk. De vanligaste skalen inkluderar

1. Bash (Bourne Again SHell)
2. Zsh (Z Shell)
3. Fisk.

Skalskript kan sträcka sig från enkla one-liners till komplexa program, och de används för att utföra en mängd olika uppgifter, såsom filmanipulation, systemadministration och automatisering av repetitiva uppgifter.

## Fördelar med Shell Scripting:

1.  **Automation:** Shell-skript tillåter användare att automatisera repetitiva uppgifter, vilket sparar tid och minskar risken för mänskliga fel.
    
2.  **Anpassning:** Användare kan skapa skript som är skräddarsydda för deras specifika behov, vilket ger en hög grad av anpassning.
    
3.  **Satsbearbetning:** Skalskript är utmärkta för att hantera satsvis bearbetningsuppgifter, där flera kommandon måste köras i följd.
    
4.  **Systemadministration:** Shell-skript används ofta för systemadministrationsuppgifter, såsom säkerhetskopiering, loggrotation och programvaruinstallation.

## Att skriva ett enkelt skalskript:

Låt oss skapa ett grundläggande skalskript som skriver ut ett hälsningsmeddelande. Öppna en textredigerare och skapa en fil med namnet `greeting.sh`. Lägg till följande rader:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Spara filen och gör den körbar genom att köra följande kommando i terminalen:

```
chmod +x greeting.sh
```

Nu kan du köra skriptet:

```
./greeting.sh
```

Utgången bör vara:

```
Hello, welcome to the world of shell scripting!
```

## Köra Shell-skript på Ubuntu och Linux:

Nu kommer vi att diskutera **hur man kör en .sh-fil i Ubuntu och Linux**.

1.  **Gör skriptet körbart:** Innan du kör ett skalskript, se till att det är körbart. Använd kommandot `chmod` som visats tidigare.
    
2.  **Navigera till skriptkatalogen:** Öppna en terminal och använd kommandot `cd` för att navigera till katalogen som innehåller ditt skalskript.
    
3.  **Kör skriptet:** Kör skriptet genom att skriva `./scriptname.sh` i terminalen, ersätt scriptname med det faktiska namnet på ditt skript.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Använda kommandot Bash:** Om ditt skript börjar med `#!/bin/bash` (känd som en **shebang**), kan du också köra det med kommandot `bash`.

```
bash greeting.sh
```

## Vad betyder $@ i Shell Script?

I skalskriptet representerar `$@` alla kommandoradsargument som skickas till skriptet. Det används ofta för att referera till en lista med argument som separata enheter. När den används inom dubbla citattecken, som `$@`, bevarar den individuella argument och tar hänsyn till mellanslag och specialtecken.

Här är en kort förklaring:

- `$@`: Representerar alla positionsparametrar (argument) som skickas till skript eller funktion. Varje argument behandlas som ett separat ord.
    
- `$@`: När det är dubbla citattecken bevaras separationen av argument, vilket tillåter mellanslag eller specialtecken i enskilda argument.
    

Här är ett enkelt exempel för att illustrera:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

När du kör det här skriptet med argument, till exempel:

```
bash example.sh arg1 "argument 2" arg3
```

Det skulle mata ut:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Som du kan se representerar `$@` alla argument, och `$@` bevarar de individuella argumenten, även om de innehåller mellanslag.

