{
  "date" : "2023-01-31",
  "keywords" :["run-bestand", "wat is een run-bestand", "bestand", "hoe run-bestand te openen", "bestandsextensie uitvoeren", "extensie"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Leer meer over de RUN-bestandsindeling en API's die RUN-bestanden kunnen maken en openen.",
  "title" :"RUN-bestandsindeling - uitvoerbaar Linux-bestand",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## Wat is een RUN-bestand?

Het .run-bestandsformaat wordt vaak gebruikt voor het distribueren van software- of applicatie-installatieprogramma's in de Linux-omgeving. Om de software te installeren, moet u het bestand uitvoerbaar maken. Dit kunt u doen met de volgende opdracht:

```bash
chmod +x file_name.run 
```

Vervolgens kunt u het bestand uitvoeren met de volgende opdracht:

```bash
./file_name.run 
```

Het installatieproces kan variëren, afhankelijk van het specifieke bestand en programma dat u probeert te installeren.

Het .run-bestandsformaat is een type shellscript dat wordt gebruikt om software- of applicatie-installatieprogramma's in de Linux-omgeving te distribueren. Het is een op zichzelf staand pakket dat alles bevat wat nodig is om de software te installeren, inclusief binaire bestanden, bibliotheken en configuratiebestanden.

Het is belangrijk op te merken dat .run-bestanden ook schadelijke code kunnen bevatten. Het is dus altijd een goed idee om de bron van het bestand te verifiëren en het op virussen te scannen voordat u het uitvoert.

Bovendien hebben sommige .run-bestanden mogelijk rootrechten nodig om te kunnen worden uitgevoerd en geïnstalleerd, dus u moet mogelijk de opdracht "sudo" gebruiken om het bestand met verhoogde machtigingen uit te voeren:

```bash
sudo ./filename.run
```

## Hoe open je een RUN-bestand?

Om een .run-bestand te openen, moet u het uitvoerbaar maken, wat gedaan kan worden met de opdracht "chmod":

```bash
chmod +x filename.run 
```

Zodra het bestand uitvoerbaar is gemaakt, kunt u het uitvoeren door het volgende te typen:

```bash
./filename.run
```

Het uitvoeren van een .run-bestand is niet hetzelfde als het openen in een teksteditor. Als u een .run-bestand uitvoert, worden de instructies uitgevoerd, die van alles kunnen zijn, van het installeren van een programma tot het uitvoeren van een script. Om de inhoud van een .run-bestand te bekijken, moet je het openen in een teksteditor, zoals nano of vim:

```
nano filename.run
```
of
```
vim filename.run
```

## Referenties
* [Hoe .bin- en .run-bestanden uit te voeren in Ubuntu](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)


