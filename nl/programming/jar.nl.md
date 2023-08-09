{
  "date" : "2019-10-11",
  "keywords" :[ "JAR", ".jar", "wat is een jar-bestand", "hoe een jar-bestand te openen", "extensie", "bestand", "jar-bestand", "jar-bestandsformaat", ".jar-extensie "],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JAR - Java-archiefbestandsindeling",
  "description":"Meer informatie over JAR-bestandsindelingen en API's die JAR-bestanden kunnen maken en openen.",
  "linktitle" : "JAR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Wat is een JAR-bestand?

Een bestand met de extensie .jar is een Java-archiefbestand dat veel verschillende applicatiegerelateerde bestanden als één bestand bevat. Deze bestandsindeling is gemaakt om de snelheid van het laden van een gedownloade Java-applet in de browser via HTTP-transactie te verminderen, door te vermijden dat meerdere HTTP-verbindingen worden gemaakt. Een enkel JAR-bestand kan Java-klassebestanden ([.class](/nl/programming/class/)), [images](/nl/image/) en [sounds](/nl/audio/) bevatten. Individuele items in een JAR-bestand kunnen digitaal worden ondertekend door de applicatieontwikkelaar om hun oorsprong te verifiëren. JAR-bestanden worden regelmatig gebruikt om functionele API's te maken die specifieke functionaliteit met betrekking tot die API bevatten.

## JAR-bestandsindeling

JAR-bestanden zijn gebaseerd op het populaire [ZIP-bestandsformaat](/nl/compression/zip/) dat de afzonderlijke inhoudsbestanden in een enkel bestand archiveert. Het JAR-bestandsformaat ondersteunt compressie, wat resulteert in een kleinere bestandsgrootte voor downloaden en dus een verdere verbetering van de downloadtijd. Het [JAR-bestandsspecificaties](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) artikel van Oracle geeft volledige details over de interne specificaties van JAR-bestanden.

### Het manifestbestand

Wanneer een JAR-bestand wordt gemaakt, wordt er automatisch een manifestbestand in gemaakt dat de metadata-informatie over de inhoud van het JAR-bestand bevat. Dit bestand toont de inhoud die in het JAR-bestand is verpakt. Een typisch Manifest-bestand ziet er als volgt uit en toont de mappen en klassen die in het JAR-bestand zijn opgenomen.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Manifestspecificaties

Manifestspecificaties worden door Oracle als volgt gedefinieerd.

`manifest-file`: hoofd-sectie nieuwe regel \*individuele-sectie

`main-section`: versie-info nieuwe regel \*main-attribute

`versie-info`: Manifest-Versie: versienummer

`versienummer` : cijfer+{.cijfer+}*

`main-attribute`: (elk legitiem hoofdattribuut) newline

`individuele-sectie`: Naam : waarde nieuwe regel \*perentry-attribuut

`perentry-attribuut`: (elk legitiem perentry-kenmerk) newline

`nieuwe regel`: CR LF | LF | CR (niet gevolgd door LF)

`digit`: {0-9}

### Uitvoerbare JAR

JAR-bestanden kunnen ook bestaan uit een toepassing die kan worden uitgevoerd door Java Virtual Machine (JVM), vergelijkbaar met elke andere toepassing op het Microsoft Windows-besturingssysteem. In dit geval moet de JVM op de hoogte zijn van het toegangspunt van de toepassing dat een klasse is met een openbare statische void-hoofdmethode. Het manifestbestand identificeert een dergelijke klasse met de kop 'Main-Class' in de volgende indeling:

```
Main-Class: com.example.MyClassName
```



## Referenties

* [JAR-bestandsoverzicht](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
* [JAR-bestandsindeling](https://en.wikipedia.org/wiki/JAR_(file_format))

