{
  "date" : "2019-10-11",
  "keywords" :[ "arsc", ".arsc", "wat is een arsc-bestand", "hoe een arsc-bestand te openen", "extensie", "bestand", "arsc-bestand", "arsc-bestandsformaat", "arsc-bestandsextensie" ,"arsc-bestandsvoorbeeld"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARSC - Android-pakketbrontabelbestand",
  "description":"Meer informatie over ARSC-bestandsindeling en API's die ARSC-bestanden kunnen maken en openen.",
  "linktitle" : "ARSC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-22"
}

## Wat is een ARSC-bestand?

Een ARSC-bestand is een Android-brontabelbestand dat de lijst met bronnen van de toepassing in tabelindeling bevat. Dit bevat informatie zoals resourcenamen, eigenschappen en ID's. ARSC-bestanden maken deel uit van APK-pakketten die worden gebruikt om deze Android-apps te installeren. Alle bronnen, zoals afbeeldingen, lay-outs, stijlen en tekenreeksen, in een Android-applicatie worden geconverteerd naar binaire bestanden wanneer het APK-bestand wordt gegenereerd. Het ARSC-bestand wordt tegelijkertijd ook gegenereerd, met een lijst van alle gecompileerde bronnen van het programma en hun ID's.

## ARSC-bestandsindeling

De .arsc-extensiebestanden zijn binaire bestanden die worden gegenereerd nadat de compiler, zoals ANT (Eclipse) of Gradle (AS), de Android-toepassingscode compileert om het [APK](/nl/compression/apk/)-bestand te produceren. U kunt het APK-bestand uitpakken met elk archiveringshulpprogramma zoals WinZip om de inhoud ervan te bekijken, dit zijn de gecompileerde java-klassebestanden, dwz klassen.dex. Naast deze bevat het ook dit ARSC-bestand dat meta-informatie bevat over:

* De XML-knooppunten
* De attributen
* De resource-ID's

Resources in een APK-bestand worden verwezen door de resource-ID's, terwijl de kenmerken tijdens runtime worden omgezet in een waarde. De Android aapt-tool verzamelt alle bronnen die zijn gedefinieerd in bestanden tijdens het bouwen en wijst er bron-ID's aan toe. Nadat identifiers zijn toegewezen aan de gecompileerde bronnen, wordt een R.java-bestand gegenereerd op basis van de broncode en de resources.arsc.

## Referenties

* [Binaire resourcetabelstructuur](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)

