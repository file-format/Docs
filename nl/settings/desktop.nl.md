{
"datum": "31-05-2023",
  "keywords": [
"bureaubladbestand",
"wat is een desktopbestand",
"Wat bevat het bureaubladbestand",
"voorbeeld bureaubladbestand",
"Hoe bureaubladbestand openen",
"wat is het formaat van het desktopbestand",
"bestand",
"desktop bestandsextensie",
"verlenging"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"DESKTOP-bestandsindeling - Desktop-invoerbestand",
  "description":"Leer meer over DESKTOP-indeling en API's waarmee DESKTOP-bestanden kunnen worden gemaakt en geopend.",
"linktitle":"DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop",
"parent" : "settings"
}
},
"laatste mod": "2023-05-31"
}

## Wat is een DESKTOP-bestand?

Een .desktop-bestand is een configuratiebestand dat door Linux-desktopomgevingen wordt gebruikt om snelkoppelingen en opstartprogramma's voor toepassingen te definiëren. Het biedt metagegevens over een applicatie, zoals de naam, het pictogram, de uit te voeren opdracht en andere eigenschappen. Deze bestanden worden doorgaans gebruikt om snelkoppelingen te maken in toepassingsmenu's, bureaubladstartprogramma's of panelen in Linux-gebaseerde systemen.

## Wat bevat het DESKTOP-bestand?

Een .desktop-bestand volgt een specifiek formaat en bevat verschillende sleutelvelden:

- **[Bureaubladinvoer]:** Dit is de hoofdsectiekop voor het .desktop-bestand.
- **Naam:** Specificeert de naam van de applicatie.
- **Opmerking:** Geeft een korte beschrijving of commentaar over de toepassing.
- **Exec:** Definieert de opdracht die moet worden uitgevoerd bij het starten van de applicatie.
- **Icoon:** Specificeert het pad naar het pictogrambestand dat aan de toepassing is gekoppeld.
- **Terminal:** Specificeert of de applicatie in een terminalvenster moet worden uitgevoerd.
- **Type:** Specificeert het type invoer, zoals 'Applicatie' of 'Link'.
- **Categorieën:** Specificeert categorieën of groepen waaronder de applicatie in het menu moet worden weergegeven.
- **StartupNotify:** Specificeert of de desktopomgeving een opstartmelding voor de toepassing moet tonen.
- **NoDisplay:** Specificeert of de applicatie verborgen moet worden in menu's.
- **Acties:** Definieert aanvullende acties die op de toepassing kunnen worden uitgevoerd, zoals het openen van een specifiek bestand.

## Voorbeeld DESKTOP-bestand

Hier is een voorbeeld van een .desktop-bestand voor een fictieve teksteditor genaamd "MyTextEditor":

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

In dit voorbeeld definieert het .desktop-bestand de applicatie "MyTextEditor" met de bijbehorende eigenschappen. Het bevat ook twee extra acties, "Nieuw venster openen" en "Bestaand bestand openen", die toegankelijk zijn via het contextmenu van de applicatiestarter.

Door een .desktop-bestand in specifieke mappen zoals `/usr/share/applications` of `~/.local/share/applications` te plaatsen, zal de desktopomgeving het herkennen en de applicatie dienovereenkomstig in menu's weergeven of toestaan dat deze wordt gestart vanuit bureaublad.

## Hoe het DESKTOP-bestand te openen?

Verschillende softwareprogramma's kunnen .desktop-bestanden openen en verwerken. Deze programma's zijn doorgaans bestandsbeheerders of desktopomgevingen op Linux-gebaseerde systemen. Hier zijn enkele voorbeelden:

- **Nautilus (Bestanden):** De standaard bestandsbeheerder voor de GNOME-desktopomgeving.
- **Nemo:** De bestandsbeheerder voor de Cinnamon-desktopomgeving.
- **Dolphin:** De standaard bestandsbeheerder voor de KDE Plasma-bureaubladomgeving.
- **Thunar:** De standaard bestandsbeheerder voor de Xfce-desktopomgeving.
- **KDE Menu Editor:** Een hulpmiddel specifiek voor de KDE Plasma-bureaubladomgeving waarmee u .desktop-bestanden kunt bekijken en bewerken.

Deze bestandsbeheerders en desktopomgevingen bieden een grafische interface voor het beheren van .desktop-bestanden. Hiermee kunt u de eigenschappen van .desktop-bestanden bekijken en bewerken, applicatiestartprogramma's maken en snelkoppelingen organiseren in applicatiemenu's of op het bureaublad.

De .desktop-bestanden zijn platte tekstbestanden, dus u kunt ze ook openen en bewerken met een teksteditor naar keuze. Klik eenvoudig met de rechtermuisknop op het .desktop-bestand en selecteer "Openen met" of "Openen met een andere applicatie" om een teksteditor te kiezen uit de lijst met geïnstalleerde programma's.

## Wat is het formaat van het DESKTOP-bestand?

Het .desktop-bestandsformaat volgt een specifieke structuur en formaat. Het is een tekstbestand met een reeks sleutel-waardeparen, georganiseerd in secties. Hier is een overzicht van het formaat:

- **Sectiekoppen:** Elke sectie begint met een kop tussen vierkante haakjes ([]). De primaire sectie heet doorgaans [Desktop Entry], die de belangrijkste metagegevens voor de applicatie of het opstartprogramma bevat.
- **Sleutel-waardeparen:** Binnen elke sectie definieert u eigenschappen met behulp van sleutel-waardeparen. Het formaat is "Sleutel=Waarde". De sleutel identificeert eigendom en waarde levert overeenkomstige gegevens op.
- **Eigenschapsyntaxis:** De eigenschapswaarden kunnen van verschillende typen zijn, waaronder tekenreeksen, Booleaanse waarden, bestandspaden of lijsten. Het formaat voor elke eigenschapswaarde is afhankelijk van het type.
- **Opmerkingen:** U kunt opmerkingen in het .desktop-bestand opnemen met het '#'-symbool. Alles wat online volgt op '#' wordt beschouwd als commentaar en wordt genegeerd.

## Referenties
* [Bureaubladinvoerbestanden] (https://www.baeldung.com/linux/desktop-entry-files)

