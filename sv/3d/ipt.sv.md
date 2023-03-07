{
  "date" : "2019-10-11",
  "keywords" :[ "IPT", "IPT-fil", "IPT-filformat", "filformat", "3d","ipt-filnedladdning"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om IPT-filformat och API:er som kan öppna och skapa IPT-filer.",
  "title" :"IPT - Autodesk Inventor Part File",
  "linktitle" : "IPT",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-01-25"
}

## Vad är en IPT fil?

En fil med filtillägget .ipt är inbyggt Autodesks Inventor Part-filformat för delar.
![IPT File](../ipt2.jpg "IPT File")
Den används i kombination med Autodesks monteringsfiler (.iam). IPT-filer kan importeras i 3DS Max som Body Objects där geometrin i ACIS solids-formatet förblir i samma format. 3DS Max behåller objektnamnet som tilldelats i Autodesk Inventor och komponentmodellerna kan redigeras på samma sätt som andra objekt, inklusive att använda modifierare, ändra material, lägga till belysning och kameror, skapa animationer och så vidare. Du kan öppna IPT-filer med applikationer som Autodesk Inventor och Autodesk Fusion.

## IPT filformat

En Autodesk **IPT-filtillägg** som används för att spara en fil som består av skisser, funktioner och kroppar som gör att delen kan användas i sammanställningar. En skiss är den mest använda komponenten och de flesta delar börjar med en skiss. Det är profilen för ett objekt och eventuell geometri som krävs för att skapa objektet. Flera funktioner utgör en "delmodell" och en flerkroppsdel kan dela funktioner. De geometriska förhållandena som parallella och vinkelräta styrs av skissrestriktioner. Effekten av modifieringar kan observeras genom att justera begränsningarna eller dimensionsparametrarna för att kontrollera storleken och formen på en modell.
![IPT File Format](../ipt.jpg "IPT File Format")

**Obs!** IPT-filformatsspecifikationer är inte tillgängliga offentligt.

## Ladda ner IPT-fil
Det är lite svårt att hitta och ladda ner IPT-filen för en 3d-modell. Därför kan du ladda ner ett exempel på en IPT-fil härifrån:

- [Sample.ipt](../sample.ipt)

## Referenser

* [IPT-filer - Autodesk](https://knowledge.autodesk.com/support/inventor/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/Inventor-Help/files/GUID-94B779C0-6B2B-499A-A4F9-2E4BAB49712F-htm.html)
