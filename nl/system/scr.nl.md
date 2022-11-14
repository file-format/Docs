{
  "date" : "2021-07-13",
  "keywords" :[ "scr-bestand", "wat is een scr-bestand", "bestand", "scr-voorbeeld", "scr-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SCR - Windows Screensaver-bestand",
  "description":"Meer informatie over SCR-bestandsindelingen en API's die SCR-bestanden kunnen maken en openen.",
  "linktitle" : "SCR",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-13"
}

## Wat is een SCR-bestand?
Een bestand met de extensie .scr is een schermbeveiligingsbestand dat wordt gebruikt door het Microsoft Windows-besturingssysteem. Het bestaat uit animaties, afbeeldingen, diavoorstellingen of video's die als Windows-screensaver kunnen worden gebruikt. SCR-bestanden worden gewoonlijk opgeslagen in de hoofdmap van Microsoft Windows. De screensavers moesten voorkomen dat CRT- of plasmacomputermonitoren zouden lijden aan een aandoening die optreedt wanneer het scherm te lang hetzelfde beeld vertoont. Hoewel de nieuwste monitoren niet in een dergelijke toestand lijden, worden de schermbeveiligingen nog steeds gebruikt om het scherm om veiligheidsredenen te voorkomen.

## SCR-bestandsindeling
Een screensaver is een computerprogramma dat het vult met geanimeerde afbeeldingen of patronen wanneer er gedurende lange tijd geen activiteit op een computer wordt uitgevoerd. De screensavers zijn geïntroduceerd om het inbranden van fosfor op plasma, Cathode Ray Tube (CRT) en OLED-computermonitoren te voorkomen. Screensavers zijn meestal ingesteld om een basisbeveiligingslaag toe te passen, door een wachtwoord te vereisen om het apparaat opnieuw te openen. Screensavers worden meestal ontwikkeld en gecodeerd met behulp van verschillende programmeertalen en grafische interfaces. Meestal gebruiken de ontwikkelaars van screensavers de programmeertalen C of C++, samen met grafische bibliotheken of GDI's, zoals OpenGL, dat op veel platforms werkt die in staat zijn tot 3D-rendering. De uitvoer van de screensaver wordt opgeslagen als een draagbaar uitvoerbaar bestand.

### SCR-bestandsgebruik
In de oude CRT- of plasmagebaseerde monitoren werd het inbranden van het scherm gemeld omdat hetzelfde beeld gedurende een lange periode op het scherm werd weergegeven. Het inbranden van het scherm is een geval waarin de eigenschappen van de blootgestelde delen van de fosforcoating aan de binnenkant van het scherm geleidelijk veranderen en uiteindelijk leiden tot een donkerder schaduwbeeld op het scherm. Dus de screensavers moesten het schermbeeld continu veranderen en meestal waren het .scr-bestanden die essentieel waren voor de monitoren van geldautomaten of treinkaartjes. Later losten LCD's en meer geavanceerde versies van monitoren het probleem op. Daarom worden de screensavers in de moderne tijd nog steeds gebruikt om de inactieve apparaten te beschermen tegen gebruik door een tweede persoon. Het vereist het wachtwoord of patroon om opnieuw toegang te krijgen tot het apparaat.

## Een screensaver maken met C#
Hoewel we een schermbeveiliging kunnen maken in een van de .NET-programmeertalen, wordt hier de C#-programmeertaal gegeven:

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
Wijzig de extensie van het uitvoerbare bestand van .exe in .scr. Het SCR-bestand kan dus worden genoemd als ScreenSaver.scr.

## Referenties

* [Screensaver](https://en.wikipedia.org/wiki/Screensaver)
* [Schrijf een screensaver die echt werkt](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)


