{
"date":"2023-07-20",
   "keywords":[
"BIN",
"BIN-bestand",
"bestand",
"BIN bestandsextensie",
"verlenging",
"bestand"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title":"BIN-bestandsindeling - Unix-uitvoerbaar bestand",
   "description":"Leer meer over het BIN-formaat en API's waarmee BIN-bestanden kunnen worden gemaakt en geopend.",
"linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin",
"parent" : "executable"
}
},
"lastmod":"2023-07-20"
}

## Wat is een BIN-bestand?

Een BIN-bestand is een uitvoerbaar bestand op Unix-gebaseerde besturingssystemen zoals Linux of FreeBSD. Het bevat een gecompileerd programma dat is samengesteld uit binaire code die is afgeleid van de broncode, waardoor het compatibel is met de onderliggende systeemarchitectuur. Unix uitvoerbare BIN-bestanden kunnen worden vergeleken met Windows .EXE-bestanden en macOS .APP-bestanden in termen van hun rol als uitvoerbare formaten.

Op het gebied van softwareontwikkeling voor Unix-systemen worden BIN-bestanden vaak door ontwikkelaars gebruikt om programma's te verpakken en te distribueren. Ze bieden een handige manier om software aan gebruikers te leveren, waardoor een eenvoudige installatie en uitvoering mogelijk is. Naast BIN-bestanden bestaan er nog andere soorten uitvoerbare Unix-bestanden, waaronder [.ELF](/nl/executable/elf/), .X86, [.RUN](/nl/executable/run/) en .X86_64, elk afgestemd op specifieke hardware of systeem vereisten.

Als het gaat om de interne structuur van een BIN-bestand, bestaat het uit gecodeerde gegevens die het Unix-besturingssysteem gebruikt om het bijgevoegde programma te identificeren, lezen en uit te voeren. Het systeem vertrouwt op specifieke bestandshandtekeningen of headers om het BIN-bestand als uitvoerbaar bestand te herkennen, gevolgd door de interpretatie en uitvoering van de binaire instructies die het bevat.

BIN-bestanden worden vaak geleverd met een bijbehorend **INSTALL.TXT**-bestand, dat gedetailleerde instructies biedt over hoe u het programma correct kunt installeren en instellen. Deze documentatie zorgt ervoor dat gebruikers met succes door het installatieproces kunnen navigeren en de software zonder complicaties kunnen gaan gebruiken.

## Hoe open je een BIN-bestand?

BIN-bestanden zijn niet ontworpen om rechtstreeks te worden geopend en bekeken. U kunt de programma's echter wel uitvoeren of de gegevens die ze bevatten extraheren. Om toegang te krijgen tot de inhoud van een BIN-bestand, volgt u deze stappen op de opdrachtregel, ervan uitgaande dat de naam van het BIN-bestand "sample.bin" is:

1. **Zorg voor uitvoerbare machtigingen:**

Voordat u het BIN-bestand uitvoert, moet u ervoor zorgen dat het over de benodigde machtigingen beschikt om als uitvoerbaar bestand te worden uitgevoerd. Gebruik het commando:

```
$ chmod +x sample.bin
```

Deze opdracht verleent het bestand uitvoerbare rechten.

2. **Voer het BIN-bestand uit:**

Nadat u de uitvoerbare machtigingen hebt ingesteld, kunt u het BIN-bestand uitvoeren door de volgende opdracht in te voeren:

```
$ ./sample.bin
```

**Waarschuwing**

_Wees voorzichtig bij het omgaan met gedownloade of per e-mail verzonden BIN-bestanden, aangezien deze mogelijk door cybercriminelen kunnen worden gebruikt om malware te verspreiden. Voer alleen BIN-bestanden uit van vertrouwde bronnen om het risico op kwaadaardige uitvoerbare aanvallen te beperken._

## Andere BIN-bestanden

Hier volgen andere bestandstypen die de bestandsextensie **.bin** gebruiken.

- [BIN - MacBinary gecodeerd bestand] (/nl/compression/bin/)
- [BIN - Binair schijfimagebestand](/nl/disc-and-media/bin/)
- [BIN - BlackBerry IT-beleidsbestand](/nl/settings/bin/)
- [BIN - Sega Genesis Game-ROM](/nl/game/bin/)
- [BIN - PSX PlayStation BIOS-afbeelding](/nl/game/bin-pcsx/)

## Referenties

* [Hoe binaire bestanden uit te voeren in Linux](https://linuxhint.com/execute-binary-files-in-linux/)


