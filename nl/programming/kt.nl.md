---
date: 2019-10-11
keywords: kt, .kt, kotlin-bestandsindeling, hoe kotlin-bestanden te openen, hoe kotlin-bestanden uit te voeren, .kt-bestandsindeling, kt-bestand, kotlin-bestandsextensie, .kt-extensie, kotlin vs java
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: KT-bestandsindeling
linktitle: KT
description: "Lees meer over KT-bestandsindelingen en API's die KT-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## Wat is een KT-bestand? ##

Een broncode geschreven in Kotlin wordt opgeslagen met de extensie .kt die algemeen bekend staat als **Kotlin-bestandsextensie**. De Kotlin is een universele programmeertaal voor meerdere platforms, ontwikkeld door JetBrains om volledig interoperabel te zijn met [Java](/nl/programming/java/). Het Kotlin-handelsmerk wordt beschermd door de Kotlin Foundation.

Kotlin werd op 7 mei 2019 door Google aangekondigd als de favoriete programmeertaal voor de ontwikkeling van Android-apps. Android Studio 3.0 begon in oktober 2017 met het ondersteunen van Kotlin als alternatief voor de ontwikkeling van Android-apps.

## Korte geschiedenis van Kotlin KT-bestandsindeling ##

Kotlin werd in juli 2011 door JetBrains onthuld als een nieuwe programmeertaal voor JVM. De leider van JetBrains Dmitry Jemerov zei dat de meeste talen functies misten waarnaar ze op zoek waren, behalve Scala, maar de trage compilatie van Scala was een nadeel. Een van de belangrijkste doelen van Kotlin was om even snel te compileren als Java. Het Kotlin-project was in februari 2012 open source onder de Apache 2-licentie.

Versie 1.0 van Kotlin werd uitgebracht op 15 februari 2015. Android kondigde eersteklas ondersteuning voor Kotlin op Android aan op Google I/O 2017. Kotlin 1.2 werd uitgebracht op 28 november 2017 met de mogelijkheid om code te delen tussen JVM- en JavaScript-platforms. Kotlin 1.3 werd uitgebracht op 29 oktober 2018 met de ondersteuning voor asynchrone programmering. Google heeft op 7 mei 2019 aangekondigd dat Kotlin de favoriete programmeertaal is voor de ontwikkeling van Android-apps. Kotlin 1.4 werd in augustus 2020 uitgebracht met enkele kleine wijzigingen om de interoperabiliteit met Swift/Objective-C te ondersteunen.

## Kotlin-syntaxis ##

Kotlin is ontworpen om beter te zijn dan Java, maar toch interoperabel te zijn met Java-code om een geleidelijke migratie van Java naar Kotlin mogelijk te maken.

* Puntkomma's zijn optioneel in Kotlin. Een nieuwe regel is voldoende om het einde van de verklaring aan te geven.
* Kotlin ondersteunt twee soorten variabelen, alleen-lezen, gedefinieerd door het sleutelwoord *val*, en veranderlijk, gedefinieerd door het sleutelwoord *var*.
* Lessen zijn standaard privé en definitief. Om van een klasse af te leiden, moet de basisklasse worden gedeclareerd met het sleutelwoord *open*.
* Kotlin ondersteunt ook procedureel programmeren.
* Het toegangspunt tot het Kotlin-programma is de "hoofd" -functie vergelijkbaar met Java, C #, enz.

### Syntaxisvoorbeeld ###

Het volgende is een voorbeeld van de Kotlin-syntaxis.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

In de bovenstaande code definieert het sleutelwoord **fun** de functie met de naam main. Binnen de functie wordt een alleen-lezen variabele 'publiek' gedeclareerd met het sleutelwoord **val**. Door de **println**-methode te gebruiken, wordt "Hello World from Kotlin" op de console afgedrukt. De waarde van de variabele doelgroep wordt in de string geïnjecteerd met het **$** teken.

## Kotlin vs Java
De Kotlin is een officiële taal om Android-apps te schrijven met veel geavanceerde functies, maar veel deskundige Java-ontwikkelaars tonen nog steeds geen interesse om over te stappen naar Kotlin. Ze denken dat ze alles alleen met Java kunnen. Hieronder volgt de vergelijking tussen twee technologieën die de Java-ontwikkelaars kunnen overtuigen om over te stappen:

| Parameter | Java | Kotlin |
|--------------------|-----------|---------------- -|
| Singletons Objecten | | |
| Soorten jokertekens | | |
| Compilatie | Bytecodes | Virtuele machine |
| Lambda-expressie | | |
| Invariante matrix | | |
| Niet-private velden | | |
| Slimme casts | | |
| Nulveiligheid | | |
| Statische leden | | |

## Referenties ##

- [Kotlin (programmeertaal) - Wikipedia](https://en.wikipedia.org/wiki/Kotlin_(programmeertaal))

