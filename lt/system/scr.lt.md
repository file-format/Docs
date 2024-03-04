{
  "date": "2021-07-13",
  "keywords": [
"scr failą",
"kas yra scr failas",
"failą",
"scr pavyzdys",
"scr failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "SCR – „Windows“ ekrano užsklandos failas",
  "description": "Sužinokite apie SCR failo formatą ir API, kurios gali kurti ir atidaryti SCR failus.",
  "linktitle": "SCR",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-sc-ltr"
}
},
  "lastmod": "2021-07-13"
}

## Kas yra SCR failas? 
Failas su plėtiniu .scr yra ekrano užsklandos failas, naudojamas Microsoft Windows operacinėje sistemoje. Jį sudaro animacijos, grafika, skaidrių demonstracija arba vaizdo įrašas, kurį galima naudoti kaip Windows ekrano užsklandą. SCR failai paprastai saugomi pagrindiniame Microsoft Windows kataloge. Ekrano užsklandos turėjo užkirsti kelią CRT arba plazminiams kompiuterių monitoriams nuo būklės, kuri atsiranda, kai ekrane per ilgai rodomas tas pats vaizdas. Nors naujausi monitoriai tokios būklės nenukenčia, tačiau ekrano užsklandos vis tiek naudojamos siekiant apsaugoti ekraną saugumo sumetimais.

## SCR failo formatas 
Ekrano užsklanda yra kompiuterinė programa, kuri užpildo ją animuotais vaizdais arba raštais, kai kompiuteryje ilgą laiką nevykdoma jokia veikla. Ekrano užsklandos buvo sukurtos siekiant užkirsti kelią fosforo perdegimui plazmoje, katodinių spindulių vamzdeliuose (CRT) ir OLED kompiuterių monitoriuose. Ekrano užsklandos paprastai nustatomos taip, kad būtų taikomas pagrindinis saugos lygis, reikalaujant slaptažodžio norint iš naujo atidaryti įrenginį. Ekrano užsklandos dažniausiai kuriamos ir koduojamos naudojant įvairias programavimo kalbas bei grafines sąsajas. Dažniausiai ekrano užsklandų kūrėjai naudoja C arba C++ programavimo kalbas kartu su grafinėmis bibliotekomis arba GDI, pvz., OpenGL, kuri veikia daugelyje 3D atvaizdavimo platformų. Ekrano užsklandos išvestis išsaugoma kaip nešiojamasis vykdomasis failas.

### SCR failo naudojimas
Senuose CRT arba plazminiuose monitoriuose buvo pranešta apie ekrano nudegimą, nes ekrane ilgą laiką buvo rodomas tas pats vaizdas. Ekrano nudegimas – tai atvejis, kai ekrano viduje esančių fosforo dangos sričių savybės keičiasi palaipsniui ir galiausiai ekrane atsiranda tamsesnis šešėlinis vaizdas. Taigi ekrano užsklandos turėjo nuolat keisti ekrano vaizdą ir dažniausiai .scr failai buvo būtini bankomatų ar geležinkelio bilietų pardavimo automatų monitoriams. Vėliau LCD ir pažangesnės monitorių versijos išsprendė problemą. Todėl ekrano užsklandos vis dar naudojamos šiuolaikinėje eroje, kad apsaugotų neveikiančius įrenginius nuo antrojo asmens naudojimo. Norint iš naujo pasiekti įrenginį, reikalingas slaptažodis arba šablonas.

## Ekrano užsklandos kūrimas naudojant C#
Nors galime sukurti ekrano užsklandą bet kuria .NET programavimo kalba, čia pateikiama C# programavimo kalba:

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
Pakeiskite vykdomojo failo plėtinį iš .exe į .scr. Taigi SCR failas gali būti pavadintas kaip ScreenSaver.scr.

## Nuorodos 

* [Ekrano užsklanda](https://en.wikipedia.org/wiki/Screensaver)

* [Parašykite ekrano užsklandą, kuri iš tikrųjų veikia](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)



