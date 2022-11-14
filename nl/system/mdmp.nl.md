{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MDMP-bestand - Windows Minidump-bestandsindeling",
  "description":"Meer informatie over MDMP-bestandsindelingen en API's die MDMP-bestanden kunnen maken en openen.",
  "linktitle" : "MDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Wat is een MDMP-bestand?

Een MDMP-bestand is een geheugendump van een toepassing op Microsoft Windows die wordt gemaakt wanneer de toepassing abnormaal wordt afgesloten of crasht. Het bevat informatie en gegevensdumps die kunnen worden gebruikt om de oorzaak van de crash op te sporen. MDMP-bestanden zijn van toepassing op toepassingen die door elk platform zijn gemaakt, zoals Java, C++, .NET en andere. Naast MDMP,

Toepassingen die MDMP-bestanden kunnen openen, zijn onder meer Microsoft Visual Studio Debugger.

## MDMP-bestandsindeling

MDMP-bestanden worden als binaire bestanden op schijf opgeslagen en kunnen worden geopend met Microsoft Visual Studio-foutopsporing. Het bevat de volgende informatie om de reden voor de crash te helpen identificeren.

* Details van het stopbericht, de parameters en andere gegevens
* Lijst met geladen stuurprogramma's
* Processorcontext (PRCB) voor de processor die niet meer werkt
* Procesinformatie en kernelcontext (EPROCESS) voor het proces dat is gestopt
* Procesinformatie en kernelcontext (ETHREAD) voor de thread die is gestopt
* Aanroepstack in kernelmodus voor de thread die is gestopt

Deze informatie helpt om erachter te komen wat er is gebeurd, het probleem op te lossen en te voorkomen dat het opnieuw gebeurt.

### Analyseer Minidump

Windows vereist een wisselbestand op het opstartvolume om een geheugendumpbestand te maken. Het wisselbestand wordt gemaakt op het opstartvolume en moet minimaal 2 megabyte (MB) groot zijn. Het dumpbestand wordt gemaakt wanneer een toepassing crasht. In het geval van een tweede probleem wordt een tweede klein geheugendumpbestand aangemaakt terwijl het vorige behouden blijft. De naam van het dumpbestand is anders om overschrijven te voorkomen.

Windows houdt een lijst bij van alle geheugendumpbestanden in de map %SystemRoot%\Minidump. U kunt MDMP-bestanden analyseren door ze in Visual Studio Debugger uit te voeren, zoals vermeld in de onderstaande stappen.

## Hoe open ik een MDMP-bestand in Visual Studio?

De volgende stappen kunnen worden gebruikt om een MDMP-bestand te openen in Visual Studio.

* Kies in Visual Studio in het menu Bestand de optie Openen | Crashdump.
* Navigeer naar het dumpbestand dat u wilt openen.
* Selecteer Openen.

## Referentie

* [Het kleine geheugendumpbestand lezen dat door Windows is gemaakt als er een crash optreedt](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -het dossier)

