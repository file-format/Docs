{
  "date": "2021-07-13",
  "keywords": [
"scr comhad",
"cad is comhad scr",
"comhad",
"scr shampla",
"síneadh comhad scr",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "SCR - Comhad spárálaíscáileáin Windows",
  "description": "Foghlaim faoi fhormáid comhaid SCR agus APIs is féidir comhaid SCR a chruthú agus a oscailt.",
  "linktitle": "SCR",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-sc-gar"
}
},
  "lastmod": "2021-07-13"
}

## Cad is comhad SCR ann? 
Is comhad spárálaíscáileáin é comhad a bhfuil síneadh .scr air a úsáideann córas oibriúcháin Microsoft Windows. Cuimsíonn sé beochan, grafach, taispeántas sleamhnán, nó físeáin is féidir a úsáid mar spárálaíscáileáin Windows. Stóráiltear comhaid SCR go coitianta i bpríomh-eolaire Microsoft Windows. Bhí na spárálaíscáileáin ceaptha chun monatóireacht a dhéanamh ar ríomhaire CRT nó plasma a chosc ó fhulaingt le riocht a tharlaíonn nuair a thaispeánann an scáileán an íomhá céanna ar feadh ró-fhada. Cé nach bhfuil na monatóirí is déanaí ag fulaingt i riocht den sórt sin, ach úsáidtear na spárálaíscáileáin fós chun an scáileán a chosc ar chúiseanna slándála.

## Formáid Comhaid SCR 
Is clár ríomhaire é spárálaíscáileáin a líonann sé le híomhánna nó patrúin beoite nuair nach mbíonn aon ghníomhaíocht ar ríomhaire le fada an lá. Tugadh isteach na spárálaíscáileáin chun cosc a chur ar dhó-isteach fosfair ar phlasma, ar mhonatóirí ríomhaire Catode Ray (CRT) agus OLED. De ghnáth socraítear spárálaíscáileáin chun sraith bhunúsach slándála a chur i bhfeidhm, trí phasfhocal a éileamh chun an gléas a athoscailt. Go hiondúil déantar spárálaíscáileáin a fhorbairt agus a chódú ag úsáid teangacha ríomhchlárúcháin éagsúla chomh maith le comhéadain ghrafaice. Den chuid is mó úsáideann forbróirí spárálaíscáileáin na teangacha ríomhchlárúcháin C nó C++, chomh maith le leabharlanna grafacha nó GDIanna, mar OpenGL, a oibríonn ar go leor ardán atá in ann rindreáil 3D. Déantar aschur an spárálaíscáileáin a shábháil mar chomhad inrite iniompartha.

### Úsáid comhad SCR
Sa Sean CRT nó monatóirí plasma-bhunaithe tuairiscíodh an sruthán scáileáin toisc go raibh an íomhá céanna ar taispeáint ar an scáileán ar feadh tréimhse fada. Is cás é an sruthán scáileáin nuair a athraíonn airíonna na réimsí nochta de bhrataithe fosfair taobh istigh den scáileán de réir a chéile agus ar deireadh thiar as a dtagann íomhá scáth dorcha ar an scáileán. Mar sin bhí na spárálaíscáileáin ceaptha an íomhá scáileáin a athrú go leanúnach agus de ghnáth bhí siad ina gcomhaid .scr riachtanach do mhonatóirí meaisíní ticéadaithe ATM nó Iarnróid. Réitigh LCDanna agus leaganacha níos airde de mhonatóirí an cheist níos déanaí. Dá bhrí sin úsáidtear na spárálaíscáileáin fós sa ré nua-aimseartha chun na gléasanna díomhaoin a chosaint ó úsáid an dara duine. Éilíonn sé an focal faire nó patrún chun an gléas a rochtain arís.

## Spárálaíscáileáin á gcruthú ag úsáid C#
Cé gur féidir linn spárálaíscáileáin a chruthú in aon cheann de na teangacha ríomhchlárúcháin .NET, tugtar an teanga ríomhchlárúcháin C# anseo:

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
Athraigh síneadh an chomhaid inrite ó .exe go .scr. Mar sin is féidir an comhad SCR a ainmniú mar ScreenSaver.scr.

## Tagairtí 

* [Scáileán]( https://ga.wikipedia.org/wiki/Screensaver)

* [Scríobh spárálaíscáileáin a oibríonn i ndáiríre](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)



