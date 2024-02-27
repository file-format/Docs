{
  "date": "2023-05-31",
  "keywords": [
"desktop-fil",
"hvad er en desktop-fil",
"hvad indeholder desktop-filen",
"eksempel desktop-fil",
"hvordan man åbner desktop-fil",
"hvad er formatet på skrivebordsfilen",
"fil",
"desktop filtypenavn",
"udvidelse"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "DESKTOP-filformat - Desktop-indgangsfil",
  "description": "Lær om DESKTOP-format og API'er, der kan oprette og åbne DESKTOP-filer.",
  "linktitle": "DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop-da",
      "parent": "settings"
}
},
  "lastmod": "2023-05-31"
}

## Hvad er DESKTOP fil?

En .desktop-fil er en konfigurationsfil, der bruges af Linux-desktopmiljøer til at definere applikationsgenveje og startere. Det giver metadata om en applikation, såsom dens navn, ikon, kommando, der skal udføres og andre egenskaber. Disse filer bruges typisk til at oprette genveje i applikationsmenuer, skrivebordsstartere eller paneler i Linux-baserede systemer.

## Hvad indeholder DESKTOP-filen?

En .desktop-fil følger et specifikt format og indeholder flere nøglefelter:

- **[Desktop Entry]:** Dette er hovedsektionens overskrift for .desktop-filen.
- **Navn:** Angiver navnet på applikationen.
- **Comment:** Provides brief description or comment about application.
- **Exec:** Definerer kommandoen, der skal udføres, når applikationen startes.
- **Ikon:** Angiver stien til ikonfil, der er knyttet til applikationen.
- **Terminal:** Angiver, om programmet skal køres i et terminalvindue.
- **Type:** Angiver type indgang såsom Applikation eller Link.
- **Categories:** Specifies categories or groups under which the application should be displayed in the menu.
- **StartupNotify:** Specificerer, om skrivebordsmiljøet skal vise en opstartsmeddelelse for applikationen.
- **NoDisplay:** Specifies whether application should be hidden from menus.
- **Handlinger:** Definerer yderligere handlinger, der kan udføres på et program, såsom at åbne en bestemt fil.

## Eksempel DESKTOP fil

Her er et eksempel på en .desktop-fil til en fiktiv teksteditor kaldet MyTextEditor:

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

I dette eksempel definerer .desktop-filen applikationen MyTextEditor med dens tilknyttede egenskaber. Det inkluderer også to yderligere handlinger, Åbn nyt vindue og Åbn eksisterende fil, som kan tilgås fra kontekstmenuen i programstarteren.

Ved at placere en .desktop-fil i specifikke mapper såsom `/usr/share/applications` eller `~/.local/share/applications`, vil skrivebordsmiljøet genkende den og vise applikationen i overensstemmelse hermed i menuer eller tillade, at den startes fra skrivebord.

## Hvordan åbner jeg filen DESKTOP?

Flere softwareprogrammer kan åbne og håndtere .desktop-filer. Disse programmer er typisk filhåndteringer eller skrivebordsmiljøer på Linux-baserede systemer. Her er nogle eksempler:

- **Nautilus (filer):** Standard filhåndtering for GNOME-skrivebordsmiljø.
- **Nemo:** Filhåndteringen til Cinnamon-skrivebordsmiljøet.
- **Dolphin:** Standard filhåndtering for KDE Plasma skrivebordsmiljø.
- **Thunar:** Standard filhåndtering for Xfce desktop-miljø.
- **KDE Menu Editor:** Et værktøj specifikt til KDE Plasma-skrivebordsmiljø, der giver dig mulighed for at se og redigere .desktop-filer.

Disse filhåndteringer og skrivebordsmiljøer giver grafisk grænseflade til styring af .desktop-filer. De giver dig mulighed for at se og redigere egenskaber for .desktop-filer, oprette applikationsstartere og organisere genveje i applikationsmenuer eller på skrivebordet.

.desktop-filerne er almindelige tekstfiler, så du kan også åbne og redigere dem med en teksteditor efter eget valg. Du skal blot højreklikke på .desktop-filen og vælge Åbn med eller Åbn med et andet program for at vælge en teksteditor fra listen over installerede programmer.

## Hvad er formatet på DESKTOP fil?

.desktop-filformatet følger specifik struktur og format. Det er en almindelig tekstfil med et sæt nøgleværdi-par organiseret i sektioner. Her er en oversigt over formatet:

- **Sektionsoverskrifter:** Hver sektion begynder med en overskrift omsluttet af firkantede parenteser ([]). Den primære sektion hedder typisk [Desktop Entry], som indeholder de vigtigste metadata for applikation eller launcher.
- **Nøgle-værdi-par:** Inden for hver sektion definerer du egenskaber ved hjælp af nøgle-værdi-par. Formatet er Nøgle=Værdi. Nøglen identificerer egenskab og værdi giver tilsvarende data.
- **Ejendomssyntaks:** Egenskabsværdierne kan være af forskellige typer, herunder strenge, booleske værdier, filstier eller lister. Formatet for hver ejendomsværdi afhænger af dens type.
- **Kommentarer:** Du kan inkludere kommentarer i .desktop-filen ved at bruge '#'-symbolet. Alt efter '#' på linjen betragtes som en kommentar og ignoreres.

## Referencer
* [Desktop Entry Files](https://www.baeldung.com/linux/desktop-entry-files)


