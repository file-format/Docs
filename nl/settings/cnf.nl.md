{
"datum": "22-03-2023",
  "keywords": [
"cnf-bestand",
"wat is een cnf-bestand",
"hoe cnf-bestand te openen",
"bestand",
"cnf bestandsextensie",
"verlenging"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"CNF-bestandsindeling - MySQL-configuratiebestand",
  "description":"Leer meer over het CNF-formaat en API's die CNF-bestanden kunnen maken en openen.",
"linktitle":"CNF",
  "menu": {
    "docs": {
      "identifier": "settings-cnf",
"parent" : "settings"
}
},
"laatste mod": "22-03-2023"
}

## Wat is een CNF-bestand?

Een CNF-bestand (ook wel configuratiebestand genoemd) in MySQL wordt gebruikt om configuratie-instellingen voor de MySQL-server op te slaan. De locatie van het CNF-bestand kan variëren, afhankelijk van het besturingssysteem en de gebruikte installatiemethode. De configuratie omvat doorgaans verschillende instellingen, zoals standaard tekencodering, time-outs, cache- en bufferconfiguraties, die kunnen worden aangepast om de databaseprestaties te optimaliseren op basis van gebruik.

## CNF-bestandsformaat – Meer informatie

U kunt CNF maken met behulp van de volgende stappen in MySQL:

1. Open een teksteditor, bijvoorbeeld Kladblok, en maak een nieuw bestand.
2. Voeg de gewenste configuratieopties toe aan het bestand, één per regel. Hier is een voorbeeld:

```
[mysqld]
datadir=/var/lib/mysql
socket=/var/lib/mysql/mysql.sock
user=mysql
symbolic-links=0

[client]
user=root
password=password123
```

3. Sla het bestand op met de extensie .cnf, bijvoorbeeld "mysql.cnf".
4. Verplaats het bestand naar de juiste map. Op Linux-systemen kan de map bijvoorbeeld /etc/mysql/conf.d/ of /etc/mysql/ zijn.
5. Start de MySQL-server opnieuw op zodat de nieuwe configuratie-instellingen van kracht worden.

Zorg ervoor dat u eventuele wijzigingen in het CNF-bestand test in een niet-productieomgeving voordat u deze in een productieomgeving implementeert.

## Hoe open je een CNF-bestand?

CNF-bestand is een tekstbestand en kan eenvoudig worden geopend met elke teksteditor zoals Kladblok. U kunt het ook openen door met de rechtermuisknop te klikken en 'Openen met' in het menu te selecteren. Zodra het bestand geopend is, kunt u de configuratie-instellingen indien nodig bewerken. CNF bevat verschillende instellingen gerelateerd aan de MySQL-server, bijvoorbeeld poortnummer, logopties en buffergroottes. Nadat u de instellingen heeft bewerkt, slaat u de wijzigingen op en sluit u de teksteditor. Start ten slotte de MySQL-server opnieuw op om de wijzigingen door te voeren.

Houd er rekening mee dat het belangrijk is om voorzichtig te zijn bij het bewerken van het MySQL-configuratiebestand, omdat onjuiste instellingen ervoor kunnen zorgen dat de server zich onvoorspelbaar gedraagt of helemaal niet opstart. Het wordt aanbevolen om een back-up te maken van het originele bestand voordat u wijzigingen aanbrengt, zodat u dit indien nodig kunt herstellen.

## Referenties
* [MySQL](https://en.wikipedia.org/wiki/MySQL)

