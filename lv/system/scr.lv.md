{
  "date": "2021-07-13",
  "keywords": [
"scr fails",
"kas ir scr fails",
"failu",
"scr piemērs",
"scr faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "SCR — Windows ekrānsaudzētāja fails",
  "description": "Uzziniet par SCR faila formātu un API, kas var izveidot un atvērt SCR failus.",
  "linktitle": "SCR",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-sc-lvr"
}
},
  "lastmod": "2021-07-13"
}

## Kas ir SCR fails? 
Fails ar paplašinājumu .scr ir ekrānsaudzētāja fails, ko izmanto operētājsistēma Microsoft Windows. Tas ietver animācijas, grafiku, slaidrādi vai video, ko var izmantot kā Windows ekrānsaudzētāju. SCR faili parasti tiek glabāti Microsoft Windows galvenajā direktorijā. Ekrānsaudzētāji bija paredzēti, lai novērstu CRT vai plazmas datoru monitoru ciešanas ar stāvokli, kas rodas, kad ekrānā pārāk ilgi tiek rādīts viens un tas pats attēls. Lai gan jaunākie monitori šādā stāvoklī necieš, taču ekrānsaudzētāji joprojām tiek izmantoti, lai drošības apsvērumu dēļ novērstu ekrānu.

## SCR faila formāts 
Ekrānsaudzētājs ir datorprogramma, kas to piepilda ar animētiem attēliem vai rakstiem, kad datorā ilgstoši netiek veiktas nekādas darbības. Ekrānsaudzētāji tika ieviesti, lai novērstu fosfora izdegšanu plazmas, katodstaru lampas (CRT) un OLED datoru monitoros. Ekrānsaudzētāji parasti tiek iestatīti, lai lietotu pamata drošības līmeni, pieprasot paroli, lai atkārtoti atvērtu ierīci. Ekrānsaudzētāji parasti tiek izstrādāti un kodēti, izmantojot dažādas programmēšanas valodas, kā arī grafiskās saskarnes. Pārsvarā ekrānsaudzētāju izstrādātāji izmanto C vai C++ programmēšanas valodas, kā arī grafiskās bibliotēkas vai GDI, piemēram, OpenGL, kas darbojas daudzās platformās, kas spēj atveidot 3D. Ekrānsaudzētāju izvade tiek saglabāta kā pārnēsājams izpildāms fails.

### SCR faila lietojums
Vecajos CRT vai plazmas monitoros tika ziņots par ekrāna apdegumu, jo ekrānā ilgu laiku tika rādīts viens un tas pats attēls. Ekrāna apdegums ir gadījums, kad ekrāna iekšpusē esošo fosfora pārklājuma zonu īpašības pakāpeniski mainās un galu galā noved pie tumša ēnas attēla uz ekrāna. Tātad ekrānsaudzētājiem bija nepārtraukti jāmaina ekrāna attēls, un parasti tie .scr faili bija nepieciešami bankomātu vai dzelzceļa biļešu automātu monitoriem. Vēlāk LCD un uzlabotas monitoru versijas atrisināja problēmu. Tāpēc ekrānsaudzētāji joprojām tiek izmantoti mūsdienu laikmetā, lai aizsargātu dīkstāves ierīces no otrās personas lietošanas. Lai atkārtoti piekļūtu ierīcei, ir nepieciešama parole vai raksts.

## Ekrānsaudzētāja izveide, izmantojot C#
Lai gan mēs varam izveidot ekrānsaudzētāju jebkurā no .NET programmēšanas valodām, šeit ir norādīta C# programmēšanas valoda:

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
Mainiet izpildāmā faila paplašinājumu no .exe uz .scr. Tātad SCR failu var nosaukt kā ScreenSaver.scr.

## Atsauces 

* [Ekrānsaudzētājs](https://en.wikipedia.org/wiki/Screensaver)

* [Uzrakstiet ekrānsaudzētāju, kas patiešām darbojas](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)



