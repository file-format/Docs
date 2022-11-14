{
  "date" : "2020-01-10",
  "keywords" :[ "c", ".c", "wat is ac-bestand", "hoe c-bestand te openen", "extensie", "bestand", "c-bestand", "c-bestandsformaat", "c-bestandsextensie"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"C - C Taalprogrammeerbestand",
  "description":"Meer informatie over C-bestandsindeling en API's die C-bestanden kunnen maken en openen.",
  "linktitle" : "C",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-01-10"
}

## Wat is een C-bestand?

Een bestand dat is opgeslagen met de bestandsextensie c is een broncodebestand geschreven in de programmeertaal C. Het **C-bestand** bevat alle functionaliteit van de toepassing in de vorm van broncode. De verklaring van de broncode wordt geschreven in de header-bestanden die zijn opgeslagen met de extensie [.h](/nl/programming/h/). C++ is de moderne vorm van C-taal en wordt tegenwoordig gebruikt om de meeste software te ontwikkelen.

## Korte geschiedenis

C-taal is ontstaan als gevolg van het maken van verschillende hulpprogramma's voor het UNIX-besturingssysteem. Denis Ritchie, de man achter de creatie van deze programmeertaal, het werk begon oorspronkelijk in de jaren zestig en begin jaren zeventig.

## C-bestandsindeling

C-bestanden zijn geschreven in platte tekstbestandsindeling volgens de syntaxis van de programmeertaal. Een typisch C-bestand heeft:

* import statement bovenaan het bestand om een header Files te importeren
* een of meer methoden om de gewenste functionaliteit te implementeren

### Koptekst importeren

De header-bestanden, met de extensie .h, bevatten noodzakelijke include-statements om andere functionaliteitsbestanden in het project op te nemen. Bovendien bevatten deze de declaraties van methoden die zijn gedefinieerd in het implementatiebestand. Headerbestanden worden opgenomen met behulp van de include-instructie zoals hieronder weergegeven.

```
#include <filename.h>
```

### Implementatie van broncode

De daadwerkelijke implementatie van de functionele eisen wordt als methode gecodeerd in het C-bestand. Elke methode in een C-bestand heeft een retourtype, een methodenaam en kan enkele invoerparameters hebben. Als het retourtype niet ongeldig is, retourneert de methode mogelijk een waarde.

### C Code Voorbeeld
Hier is een ac-voorbeeldprogramma:

```
long some_function();
/* int */ other_function();

/* int */ calling_function()
{
    long test1;
    register /* int */ test2;

    test1 = some_function();
    if (test1 > 0)
          test2 = 0;
    else
          test2 = other_function();
    return test2;
}
```



## **Referenties** ##

* [Klasse-implementatie - door Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)

