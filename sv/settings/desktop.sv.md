{
"datum": "2023-05-31",
  "keywords": [
"skrivbordsfil",
"vad är en skrivbordsfil",
"vad innehåller skrivbordsfilen",
"exempel skrivbordsfil",
"hur man öppnar skrivbordsfilen",
"vilket är formatet på skrivbordsfilen",
"fil",
"skrivbordsfiltillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Skrivbordsfilformat - Skrivbordsfil",
  "description":"Läs mer om DESKTOP-format och API:er som kan skapa och öppna DESKTOP-filer.",
"linktitle": "SKRIVBORD",
  "menu": {
    "docs": {
      "identifier": "settings-desktop",
      "parent": "settings"
}
},
"lastmod": "2023-05-31"
}

## Vad är en DESKTOP fil?

En .desktop-fil är en konfigurationsfil som används av Linux-skrivbordsmiljöer för att definiera programgenvägar och startprogram. Den tillhandahåller metadata om en applikation som dess namn, ikon, kommando att köra och andra egenskaper. Dessa filer används vanligtvis för att skapa genvägar i programmenyer, skrivbordsstartare eller paneler i Linux-baserade system.

## Vad innehåller DESKTOP-filen?

En .desktop-fil följer ett specifikt format och innehåller flera nyckelfält:

- **[Desktop Entry]:** Detta är huvudsektionens rubrik för .desktop-filen.
- **Namn:** Anger programmets namn.
- **Kommentar:** Ger en kort beskrivning eller kommentar om ansökan.
- **Exec:** Definierar kommando som ska köras när programmet startas.
- **Ikon:** Anger sökväg till ikonfil som är kopplad till programmet.
- **Terminal:** Anger om programmet ska köras i ett terminalfönster.
- **Typ:** Anger typ av post som "Applikation" eller "Länk."
- **Kategorier:** Anger kategorier eller grupper under vilka applikationen ska visas i menyn.
- **StartupNotify:** Anger om skrivbordsmiljön ska visa ett startmeddelande för programmet.
- **NoDisplay:** Anger om programmet ska döljas från menyer.
- **Åtgärder:** Definierar ytterligare åtgärder som kan utföras på programmet som att öppna en specifik fil.

## Exempel DESKTOP-fil

Här är ett exempel på en .desktop-fil för en fiktiv textredigerare som heter "MyTextEditor":

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

I det här exemplet definierar .desktop-filen applikationen "MyTextEditor" med dess associerade egenskaper. Den innehåller också två ytterligare åtgärder, "Öppna nytt fönster" och "Öppna befintlig fil", som kan nås från snabbmenyn i programstartaren.

Genom att placera en .desktop-fil i specifika kataloger som `/usr/share/applications` eller `~/.local/share/applications` kommer skrivbordsmiljön att känna igen den och visa applikationen i enlighet med detta i menyer eller tillåta att den startas från skrivbordet.

## Hur öppnar man filen DESKTOP?

Flera program kan öppna och hantera .desktop-filer. Dessa program är vanligtvis filhanterare eller skrivbordsmiljöer på Linux-baserade system. Här är några exempel:

- **Nautilus (filer):** Standardfilhanteraren för GNOME-skrivbordsmiljön.
- **Nemo:** Filhanteraren för skrivbordsmiljön Cinnamon.
- **Dolphin:** Standardfilhanteraren för KDE Plasma-skrivbordsmiljön.
- **Thunar:** Standardfilhanteraren för Xfce-skrivbordsmiljön.
- **KDE-menyredigerare:** Ett verktyg specifikt för KDE Plasma-skrivbordsmiljö som låter dig visa och redigera .desktop-filer.

Dessa filhanterare och skrivbordsmiljöer tillhandahåller ett grafiskt gränssnitt för hantering av .desktop-filer. De låter dig visa och redigera egenskaper för .desktop-filer, skapa programstartare och organisera genvägar i programmenyer eller på skrivbordet.

.desktop-filerna är vanliga textfiler, så du kan också öppna och redigera dem med en valfri textredigerare. Högerklicka helt enkelt på .desktop-filen och välj "Öppna med" eller "Öppna med ett annat program" för att välja en textredigerare från listan över installerade program.

## Vilket är formatet på DESKTOP-filen?

.desktop-filformatet följer specifik struktur och format. Det är en vanlig textfil med en uppsättning nyckel-värdepar organiserade i sektioner. Här är en översikt över formatet:

- **Sektionsrubriker:** Varje avsnitt börjar med en rubrik omgiven av hakparenteser ([]). Den primära sektionen heter vanligtvis [Desktop Entry], som innehåller huvudmetadata för applikation eller startprogram.
- **Nyckel-värdepar:** Inom varje avsnitt definierar du egenskaper med nyckel-värdepar. Formatet är "Key=Value". Nyckeln identifierar egendom och värde ger motsvarande data.
- **Egenskapssyntax:** Egenskapsvärdena kan vara av olika typer, inklusive strängar, booleska värden, filsökvägar eller listor. Formatet för varje fastighetsvärde beror på dess typ.
- **Kommentarer:** Du kan inkludera kommentarer i .desktop-filen med "#"-symbolen. Allt som följer "#" på raden betraktas som en kommentar och ignoreras.

## Referenser
* [Desktop Entry Files](https://www.baeldung.com/linux/desktop-entry-files)

