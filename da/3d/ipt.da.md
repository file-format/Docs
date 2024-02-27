{
  "date": "2019-10-11",
  "keywords": [
"IPT",
"IPT fil",
"IPT filformat",
"filformat",
"3d",
"Download ipt-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om IPT-filformat og API'er, der kan åbne og oprette IPT-filer.",
  "title": "IPT - Autodesk Inventor Part File",
  "linktitle": "IPT",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-ip-dat"
}
},
  "lastmod": "2021-01-25"
}

## Hvad er en IPT fil?

En fil med filtypenavnet .ipt er det oprindelige Autodesks Inventor Part-filformat for dele.
![IPT File](../ipt2.jpg "IPT File")
Det bruges i kombination med Autodesk assembly (.iam) filer. IPT-filer kan importeres i 3DS Max som kropsobjekter, hvor geometrien i ACIS solids-formatet forbliver i det samme format. 3DS Max bevarer objektnavnet som tildelt i Autodesk Inventor, og komponentmodellerne kan redigeres på samme måde som andre objekter, herunder at anvende modifikatorer, ændre materialer, tilføje belysning og kameraer, oprette animationer og så videre. Du kan åbne IPT filer med programmer som Autodesk Inventor og Autodesk Fusion.

## IPT filformat

En Autodesk **IPT filtypenavn** bruges til at gemme en fil, der består af skitser, funktioner og kroppe, der gør delen i stand til at blive brugt i samlinger. En skitse er den mest brugte komponent, og de fleste dele starter med en skitse. Det er profilen af en funktion og enhver geometri, der kræves for at skabe funktionen. Flere funktioner udgør en del-model, og en multi-body-del kan dele funktioner. De geometriske forhold såsom parallel og vinkelret styres af skitsebegrænsninger. Effekten af modifikationer kan observeres ved at justere begrænsningerne eller dimensionelle parametre for at kontrollere størrelsen og formen af en model.
![IPT File Format](../ipt.jpg "IPT File Format")

**Bemærk:** IPT-filformatspecifikationer er ikke offentligt tilgængelige.

## IPT-fil download
Det er lidt svært at finde og downloade IPT-filen af en 3d-model. Derfor kan du downloade en eksempel-IPT-fil herfra:

- [Sample.ipt](../sample.ipt)

## Referencer

 * [IPT-filer - Autodesk](https://help.autodesk.com/view/INVNTOR/2018/ENU/?guid=GUID-94B779C0-6B2B-499A-A4F9-2E4BAB49712F)

