{
  "date": "2021-07-13",
  "keywords": [
"scr fil",
"hvad er en scr-fil",
"fil",
"scr eksempel",
"scr filtypenavnet",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "SCR - Windows Screensaver-fil",
  "description": "Lær om SCR-filformat og API'er, der kan oprette og åbne SCR-filer.",
  "linktitle": "SCR",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-sc-dar"
}
},
  "lastmod": "2021-07-13"
}

## Hvad er en SCR fil? 
En fil med filtypen .scr er en pauseskærmsfil, der bruges af Microsoft Windows-operativsystemet. Det omfatter animationer, grafik, diasshow eller video, der kan bruges som en Windows-pauseskærm. SCR-filer er almindeligvis gemt i hovedbiblioteket i Microsoft Windows. Pauseskærmene skulle forhindre CRT- eller plasma-computerskærme i at lide med en tilstand, der opstår, når skærmen viser det samme billede for længe. Selv om de nyeste skærme ikke lider i en sådan tilstand, men pauseskærme bruges stadig til at forhindre skærmen af sikkerhedsmæssige årsager.

## SCR filformat 
En pauseskærm er et computerprogram, der fylder den med animerede billeder eller mønstre, når der ikke udføres nogen aktivitet på en computer i lang tid. Pauseskærmene blev introduceret for at forhindre indbrænding af fosfor på plasma-, katodestrålerør (CRT) og OLED-computerskærme. Pauseskærme er normalt sat op til at anvende et grundlæggende sikkerhedslag ved at kræve en adgangskode for at genåbne enheden. Pauseskærme er normalt udviklet og kodet ved hjælp af forskellige programmeringssprog samt grafiske grænseflader. For det meste bruger udviklerne af pauseskærme programmeringssprogene C eller C++ sammen med grafiske biblioteker eller GDI'er, såsom OpenGL, som fungerer på mange platforme, der er i stand til 3D-gengivelse. Pauseskærmens output gemmes som en bærbar eksekverbar fil.

### SCR-filbrug
I de gamle CRT- eller plasmabaserede skærme blev skærmbrændingen rapporteret, fordi det samme billede blev vist på skærmen i en lang periode. Skærmforbrændingen er et tilfælde, hvor egenskaberne af de udsatte områder af fosforbelægning inde i skærmen ændres gradvist og til sidst fører til et mørkere skyggebillede på skærmen. Så det var meningen, at pauseskærmene skulle ændre skærmbilledet kontinuerligt, og normalt var de .scr-filer essentielle for skærme af pengeautomater eller jernbanebilletautomater. Senere løste LCD-skærme og mere avancerede versioner af skærme problemet. Derfor bruges pauseskærmene stadig i moderne tid til at beskytte de inaktive enheder mod anden persons brug. Det kræver adgangskoden eller mønsteret for at få adgang til enheden igen.

## Oprettelse af en pauseskærm ved hjælp af C#
Selvom vi kan oprette en pauseskærm i et hvilket som helst af .NET-programmeringssprogene, er C#-programmeringssproget her givet:

```
class MyCoolScreensaver : Screensaver
{
   public MyCoolScreensaver()
   {
      Initialize += new EventHandler(MyCoolScreensaver_Initialize);
      Update += new EventHandler(MyCoolScreensaver_Update);
      Exit += new EventHandler(MyCoolScreensaver_Exit);
   }

   void MyCoolScreensaver_Initialize(object sender, EventArgs e)
   {
   }

   void MyCoolScreensaver_Update(object sender, EventArgs e)
   {
      Graphics0.Clear(Color.Black);
      Graphics0.DrawString(
         DateTime.Now.ToString(),
         SystemFonts.DefaultFont, Brushes.Blue,
         0, 0);
   }

   void MyCoolScreensaver_Exit(object sender, EventArgs e)
   {
   }

   [STAThread]
   static void Main()
   {
      Screensaver ss = new MyCoolScreensaver();
      ss.Run();
   }
}
```
Skift udvidelsen af den eksekverbare fil fra .exe til .scr. Så SCR-filen kan navngives som ScreenSaver.scr.

## Referencer 

* [Screensaver](https://en.wikipedia.org/wiki/Screensaver)

* [Skriv en pauseskærm, der faktisk virker](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)



