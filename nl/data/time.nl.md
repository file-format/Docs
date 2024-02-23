{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TIME-bestand - Wat is een .time-bestand? Tijdstip waarop het bestand is gemaakt in Linux",
  "description" : "Leer meer over het TIME-bestand en ontdek de tijd waarop het bestand is gemaakt in Linux",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-nl",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Wat is een TIME-bestand?

Het TIME-bestandsformaat werd gebruikt door een websysteem genaamd LIGHT, waarmee gebruikers hun leven konden opnemen, organiseren en delen. In wezen bewaarde het een verzameling berichten en vertegenwoordigde het een map op de levenspagina van de gebruiker binnen het systeem.

## Hoe u erachter kunt komen wanneer een bestand is gemaakt in Linux

In Linux kun je het commando `stat` gebruiken om erachter te komen wanneer een bestand is gemaakt. Hier ziet u hoe u het kunt doen:

Open een terminal en typ het volgende commando:

```
stat <file_path>
```

Vervang '<file_path> ` met het pad naar het bestand waarin u geïnteresseerd bent. Bijvoorbeeld:

```
stat /path/to/your/file.txt
```

Met deze opdracht wordt verschillende informatie over het bestand weergegeven, inclusief de aanmaaktijd ervan. Zoek naar de regel die begint met 'Geboorte' of 'Bestand:'. De Geboorte-tijd geeft aan wanneer het bestand op het bestandssysteem is aangemaakt.

Hier is een voorbeeld van hoe de uitvoer eruit zou kunnen zien:

```
  File: /path/to/your/file.txt
  Size: 1024       	Blocks: 8          IO Block: 4096   regular file
Device: 801h/2049d	Inode: 1643318     Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/   user)   Gid: ( 1000/   user)
Access: 2024-01-31 12:34:56.789012345 +0000
Modify: 2024-01-31 12:34:56.789012345 +0000
Change: 2024-01-31 12:34:56.789012345 +0000
 Birth: 2024-01-31 12:34:56.789012345 +0000
```

In dit voorbeeld geeft de Geboorte-tijd aan wanneer het bestand is aangemaakt.

