{
  "date" : "2021-07-13",
  "keywords" :[ "file scr", "che cos'è un file scr", "file", "esempio scr", "estensione file scr", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SCR - File salvaschermo di Windows",
  "description":"Scopri il formato di file SCR e le API che possono creare e aprire file SCR.",
  "linktitle" : "SCR",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-13"
}

## Che cos'è un file SCR?
Un file con estensione .scr è un file salvaschermo utilizzato dal sistema operativo Microsoft Windows. Comprende animazioni, grafica, presentazione o video che possono essere utilizzati come salvaschermo di Windows. I file SCR sono comunemente archiviati nella directory principale di Microsoft Windows. Gli screen saver avrebbero dovuto impedire ai monitor di computer CRT o plasma di soffrire di una condizione che si verifica quando lo schermo mostra la stessa immagine per troppo tempo. Sebbene i monitor più recenti non soffrano in tali condizioni, gli screen saver vengono comunque utilizzati per impedire lo schermo per motivi di sicurezza.

## Formato file SCR
Uno screen saver è un programma per computer che lo riempie di immagini o motivi animati quando nessuna attività viene eseguita su un computer per molto tempo. Gli screensaver sono stati introdotti per prevenire il burn-in del fosforo su monitor di computer al plasma, a tubi catodici (CRT) e OLED. Gli screensaver sono generalmente impostati per applicare un livello di sicurezza di base, richiedendo una password per riaprire il dispositivo. Gli screensaver vengono generalmente sviluppati e codificati utilizzando vari linguaggi di programmazione e interfacce grafiche. Per lo più gli sviluppatori di screensaver utilizzano i linguaggi di programmazione C o C++, insieme a librerie grafiche o GDI, come OpenGL, che funziona su molte piattaforme in grado di eseguire il rendering 3D. L'output dello screensaver viene salvato come file eseguibile portatile.

### Utilizzo del file SCR
Nei vecchi monitor CRT o al plasma è stata segnalata la bruciatura dello schermo perché la stessa immagine è stata visualizzata sullo schermo per un lungo periodo. La bruciatura dello schermo è un caso in cui le proprietà delle aree esposte del rivestimento al fosforo all'interno dello schermo cambiano gradualmente e alla fine portano a un'immagine d'ombra oscurata sullo schermo. Quindi gli screensaver avrebbero dovuto cambiare continuamente l'immagine dello schermo e di solito i file .scr erano essenziali per i monitor degli sportelli automatici o delle biglietterie ferroviarie. Successivamente gli LCD e le versioni più avanzate dei monitor hanno risolto il problema. Pertanto gli screensaver sono ancora utilizzati nell'era moderna per proteggere i dispositivi inattivi dall'uso da parte di una seconda persona. Richiede la password o la sequenza per accedere nuovamente al dispositivo.

## Creazione di uno screensaver utilizzando C#
Sebbene sia possibile creare uno screen saver in qualsiasi linguaggio di programmazione .NET, qui viene fornito il linguaggio di programmazione C#:

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
Modificare l'estensione del file eseguibile da .exe a .scr. Quindi il file SCR può essere chiamato come ScreenSaver.scr.

## Riferimenti

* [Salvaschermo](https://en.wikipedia.org/wiki/Screensaver)
* [Scrivi uno screensaver che funzioni davvero](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)


