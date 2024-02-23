{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Shell-script - Hoe het uit te voeren op Ubuntu en Linux",
  "description":"Lees meer over wat Shell Script is en hoe u het op Ubuntu en Linux kunt uitvoeren",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-nl",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## Wat is Shell-script?

Shell-scripting omvat het schrijven van een reeks opdrachten in een tekstbestand, vaak een **Shell-script** genoemd. Deze scripts worden uitgevoerd door een shell, een opdrachtregelinterpreter. De meest voorkomende schelpen zijn onder meer

1. Bash (Bourne opnieuw SHell)
2. Zsh (Z-schaal)
3. Vis.

Shell-scripts kunnen variëren van eenvoudige oneliners tot complexe programma's, en worden gebruikt om een breed scala aan taken uit te voeren, zoals bestandsmanipulatie, systeembeheer en automatisering van repetitieve taken.

## Voordelen van Shell-scripting:

1.  **Automatisering:** Shell-scripts stellen gebruikers in staat repetitieve taken te automatiseren, waardoor tijd wordt bespaard en de kans op menselijke fouten wordt verkleind.
    
2.  **Aanpassing:** Gebruikers kunnen scripts maken die zijn afgestemd op hun specifieke behoeften, waardoor een hoge mate van aanpassing mogelijk is.
    
3.  **Batchverwerking:** Shell-scripts zijn uitstekend geschikt voor het verwerken van batchverwerkingstaken, waarbij meerdere opdrachten achter elkaar moeten worden uitgevoerd.
    
4.  **Systeembeheer:** Shell-scripts worden vaak gebruikt voor systeembeheertaken, zoals back-ups, logboekrotatie en software-installatie.

## Een eenvoudig shellscript schrijven:

Laten we een eenvoudig shellscript maken dat een begroetingsbericht afdrukt. Open een teksteditor en maak een bestand met de naam `greeting.sh`. Voeg de volgende regels toe:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Sla het bestand op en maak het uitvoerbaar door de volgende opdracht in de terminal uit te voeren:

```
chmod +x greeting.sh
```

Nu kunt u het script uitvoeren:

```
./greeting.sh
```

De uitvoer zou moeten zijn:

```
Hello, welcome to the world of shell scripting!
```

## Shell-scripts uitvoeren op Ubuntu en Linux:

Nu bespreken we **hoe je een .sh-bestand uitvoert in Ubuntu en Linux**.

1.  **Maak het script uitvoerbaar:** Voordat u een shellscript uitvoert, moet u ervoor zorgen dat het uitvoerbaar is. Gebruik het `chmod` commando zoals eerder getoond.
    
2.  **Navigeer naar de scriptdirectory:** Open een terminal en gebruik het `cd`-commando om naar de directory te navigeren die uw shellscript bevat.
    
3.  **Voer het script uit:** Voer het script uit door `./scriptnaam.sh` in de terminal te typen, waarbij u scriptnaam vervangt door de daadwerkelijke naam van uw script.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Het Bash-commando gebruiken:** Als uw script begint met `#!/bin/bash` (bekend als een **shebang**), kunt u het ook uitvoeren met het `bash`-commando.

```
bash greeting.sh
```

## Wat betekent $@ in Shell-script?

In shellscript vertegenwoordigt `$@` alle opdrachtregelargumenten die aan het script worden doorgegeven. Het wordt vaak gebruikt om naar een lijst met argumenten te verwijzen als afzonderlijke entiteiten. Bij gebruik tussen dubbele aanhalingstekens, zoals `$@`, blijven individuele argumenten behouden, waarbij rekening wordt gehouden met spaties en speciale tekens.

Hier is een korte uitleg:

- `$@`: Vertegenwoordigt alle positionele parameters (argumenten) die aan het script of de functie worden doorgegeven. Elk argument wordt behandeld als een afzonderlijk woord.
    
- `$@`: Bij dubbele aanhalingstekens blijft de scheiding van argumenten behouden, waarbij spaties of speciale tekens binnen individuele argumenten mogelijk zijn.
    

Hier is een eenvoudig voorbeeld ter illustratie:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Wanneer u dit script uitvoert met argumenten, bijvoorbeeld:

```
bash example.sh arg1 "argument 2" arg3
```

Het zou het volgende opleveren:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Zoals u kunt zien vertegenwoordigt `$@` alle argumenten, en behoudt `$@` de individuele argumenten, zelfs als deze spaties bevatten.

