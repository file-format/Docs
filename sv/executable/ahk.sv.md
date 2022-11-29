{
  "date" : "2022-04-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om AHK-filformat och API:er som kan skapa och öppna AHK-filer.",
  "title" :"AHK-filformat- AutoHotkey-skriptfil",
  "linktitle" : "AHK",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-04-25"
}

## Vad är AHK fil?

En AHK-fil är en skriptfil som genereras med AutoHotkey-programvaran som används för automatisering av uppgifter i Microsoft Windows. Den innehåller instruktioner för automatisering av uppgifter med kortkommandon som kan användas för att utföra omedelbara åtgärder. Filen exekveras av AutoHotkey och alla åtgärder utförs sekventiellt. AHK-filer är tillräckligt kraftfulla för att utföra komplexa uppgifter med snabbtangenterna som definieras med snabbtangenterna. AHK-filer kan öppnas med textredigerare som Microsoft Notepad och Notepad++.

## AHK filformat

AHK-filer sparas på skiva som vanliga textfiler och innehåller kodrader som kan köras av AutoHotkey. AutoHotkey är ett gratis skriptspråk med öppen källkod och låter användare skapa enkla till komplexa skript för att utföra åtgärder som formulärfyllare, autoklickning, exekvering av makron, etc. En AHK-fil kan åtminstone utföra en enda åtgärd och sedan avsluta .

Det finns tillgängliga verktyg som kan användas för att konvertera AHK till [Exe](/sv/körbara/exe/)-filer.

### AHK Exempel

Följande exempel använder Win+Z-tangenten för att köra Microsoft Notepad eller föra fram det om det redan körs.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## Hur skapar jag en AHK-fil?

Följande steg kan användas för att skapa en AHK-fil. Dessa förutsätter att AutoHotkey redan är installerad på maskinen.

* Högerklicka på skrivbordet.
* Hitta "Ny" i menyn.
* Klicka på "AutoHotkey Script" i menyn "New".
* Ge skriptet ett nytt namn.
* Hitta den nyskapade filen på skrivbordet och högerklicka på den.
* Klicka på "Redigera skript".
* Ett fönster borde ha dykt upp, förmodligen Anteckningar.
* Spara filen.

## Referenser

* [AutoHotkey](https://www.autohotkey.com/)
* [Batchfil - av Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

