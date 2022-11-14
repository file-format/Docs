{
  "date" : "2022-04-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over AHK-bestandsindelingen en API's die AHK-bestanden kunnen maken en openen.",
  "title" :"AHK-bestandsindeling - AutoHotkey-scriptbestand",
  "linktitle" : "AHK",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-04-25"
}

## Wat is een AHK-bestand?

Een AHK-bestand is een scriptbestand dat is gegenereerd met de AutoHotkey-softwaretoepassing die wordt gebruikt voor het automatiseren van taken in Microsoft Windows. Het bevat instructies voor het automatiseren van taken met behulp van sneltoetsen die kunnen worden gebruikt om directe acties uit te voeren. Het bestand wordt uitgevoerd door AutoHotkey en alle acties worden opeenvolgend uitgevoerd. AHK-bestanden zijn krachtig genoeg om complexe taken uit te voeren met behulp van de sneltoetsen die zijn gedefinieerd met behulp van de sneltoetsen. AHK-bestanden kunnen worden geopend met teksteditors zoals Microsoft Notepad en Notepad++.

## AHK-bestandsindeling

AHK-bestanden worden op schijf opgeslagen als platte tekstbestanden en bevatten coderegels die door AutoHotkey kunnen worden uitgevoerd. AutoHotkey is een gratis, open-source scripttaal waarmee gebruikers eenvoudige tot complexe scripts kunnen maken om acties uit te voeren, zoals het invullen van formulieren, automatisch klikken, macro's uitvoeren, enz. Een AHK-bestand kan minimaal één actie uitvoeren en vervolgens afsluiten .

Er zijn tools beschikbaar die gebruikt kunnen worden om AHK naar [Exe](/nl/executable/exe/) bestanden te converteren.

### AHK Voorbeeld

In het volgende voorbeeld wordt de Win+Z-sleutel gebruikt om Microsoft Kladblok uit te voeren of naar voren te halen als deze al actief is.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## Hoe maak ik een AHK-bestand aan?

De volgende stappen kunnen worden gebruikt om een AHK-bestand aan te maken. Deze gaan ervan uit dat AutoHotkey al op de machine is geïnstalleerd.

* Klik met de rechtermuisknop op uw bureaublad.
* Zoek "Nieuw" in het menu.
* Klik op "AutoHotkey Script" in het menu "Nieuw".
* Geef het script een nieuwe naam.
* Zoek het nieuw gemaakte bestand op uw bureaublad en klik er met de rechtermuisknop op.
* Klik op "Script bewerken".
* Er zou een venster moeten verschijnen, waarschijnlijk Kladblok.
* Bewaar het bestand.

## Referenties

* [AutoHotkey](https://www.autohotkey.com/)
* [Batchbestand - door Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

