{
  "date" : "2023-01-31",
  "keywords" : ["run file", "what is a run file", "file", "how to open run file", "run file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Lær om RUN-filformat og API'er, der kan oprette og åbne RUN-filer.",
  "title" : "KØR filformat - Linux eksekverbar fil",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run-da",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## Hvad er en RUN fil?

.run-filformatet bruges almindeligvis til at distribuere software- eller applikationsinstallationsprogrammer i Linux-miljøet. For at installere softwaren skal du gøre filen eksekverbar, hvilket kan gøres ved hjælp af følgende kommando:

```bash
chmod +x file_name.run 
```

Derefter kan du køre filen ved at bruge følgende kommando:

```bash
./file_name.run 
```

Installationsprocessen kan variere afhængigt af den specifikke fil og det program, du forsøger at installere.

.run-filformatet er en type shell-script, der bruges til at distribuere software- eller applikationsinstallationsprogrammer i Linux-miljøet. Det er en selvstændig pakke, der inkluderer alt det nødvendige for at installere softwaren, inklusive binære filer, biblioteker og konfigurationsfiler.

Det er vigtigt at bemærke, at .run-filer også kan indeholde ondsindet kode, så det er altid en god idé at verificere kilden til filen og scanne den for virus, før du kører den.

Derudover kan nogle .run-filer kræve root-rettigheder for at køre og installere, så du skal muligvis bruge kommandoen sudo til at køre filen med forhøjede tilladelser:

```bash
sudo ./filename.run
```

## Hvordan åbner jeg filen RUN?

For at åbne en .run-fil skal du gøre den eksekverbar, hvilket kan gøres med kommandoen chmod:

```bash
chmod +x filename.run 
```

Når filen er gjort eksekverbar, kan du køre den ved at skrive:

```bash
./filename.run
```

At køre en .run-fil er ikke det samme som at åbne den i en teksteditor. Kørsel af en .run fil vil udføre dens instruktioner, som kan være alt fra installation af et program til at køre et script. For at se indholdet af en .run-fil skal du åbne den i en teksteditor, såsom nano eller vim:

```
nano filename.run
```
eller
```
vim filename.run
```

## Referencer
* [Sådan udføres .bin- og .run-filer i Ubuntu](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)



