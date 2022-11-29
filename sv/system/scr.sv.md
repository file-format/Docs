{
  "date" : "2021-07-13",
  "keywords" :[ "scr-fil", "vad är en scr-fil", "fil", "scr-exempel", "scr-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SCR - Windows Screensaver File",
  "description":"Läs mer om SCR-filformat och API:er som kan skapa och öppna SCR-filer.",
  "linktitle" : "SCR",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-13"
}

## Vad är en SCR fil?
En fil med filtillägget .scr är en skärmsläckarfil som används av operativsystemet Microsoft Windows. Den består av animationer, grafik, bildspel eller video som kan användas som en Windows-skärmsläckare. SCR-filer lagras vanligtvis i huvudkatalogen i Microsoft Windows. Skärmsläckarna var tänkta att förhindra CRT- eller plasma-datorskärmar från att drabbas av ett tillstånd som uppstår när skärmen visar samma bild för länge. Även om de senaste bildskärmarna inte lider i sådant tillstånd, men skärmsläckarna används fortfarande för att förhindra skärmen av säkerhetsskäl.

## SCR-filformat
En skärmsläckare är ett datorprogram som fyller den med animerade bilder eller mönster när ingen aktivitet utförs på en dator under en längre tid. Skärmsläckarna introducerades för att förhindra att fosfor bränns in på plasma-, katodstrålerör (CRT) och OLED-datorskärmar. Skärmsläckare är vanligtvis inställda för att tillämpa ett grundläggande säkerhetslager genom att kräva ett lösenord för att öppna enheten igen. Skärmsläckare är vanligtvis utvecklade och kodade med hjälp av olika programmeringsspråk samt grafiska gränssnitt. Mestadels använder utvecklarna av skärmsläckare programmeringsspråken C eller C++, tillsammans med grafiska bibliotek eller GDI, såsom OpenGL, som fungerar på många plattformar som kan 3D-rendering. Skärmsläckarens utdata sparas som en bärbar körbar fil.

### SCR-filanvändning
I de gamla CRT- eller plasmabaserade monitorerna rapporterades skärmbränning eftersom samma bild visades på skärmen under en lång period. Skärmbränningen är ett fall när egenskaperna hos de exponerade områdena av fosforbeläggning inuti skärmen ändras gradvis och så småningom leder till en mörkare skuggbild på skärmen. Så skärmsläckarna var tänkta att ändra skärmbilden kontinuerligt och vanligtvis var de .scr-filer nödvändiga för monitorerna på bankomater eller järnvägsbiljettautomater. Senare löste LCD-skärmar och mer avancerade versioner av bildskärmar problemet. Därför används skärmsläckare fortfarande i modern tid för att skydda de inaktiva enheterna från den andra personens användning. Det kräver lösenordet eller mönstret för att komma åt enheten igen.

## Skapa en skärmsläckare med C#
Även om vi kan skapa en skärmsläckare i vilket som helst av .NET-programmeringsspråken, ges här programmeringsspråket C#:

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
Ändra förlängningen av den körbara filen från .exe till .scr. Så SCR-filen kan namnges som ScreenSaver.scr.

## Referenser

* [Screensaver](https://en.wikipedia.org/wiki/Screensaver)
* [Skriv en skärmsläckare som faktiskt fungerar](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)


