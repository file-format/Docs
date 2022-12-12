{
  "date" : "2021-07-13",
  "keywords" :[ "fișier scr", "ce este un fișier scr", "fișier", "exemplu scr", "extensie fișier scr", "extensie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SCR - Fișier de economizor de ecran Windows",
  "description":"Aflați despre formatul de fișier SCR și despre API-urile care pot crea și deschide fișiere SCR.",
  "linktitle" : "SCR",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-13"
}

## Ce este un fișier SCR?
Un fișier cu extensia .scr este un fișier de economizor de ecran utilizat de sistemul de operare Microsoft Windows. Acesta cuprinde animații, grafică, prezentare de diapozitive sau videoclipuri care pot fi utilizate ca screensaver Windows. Fișierele SCR sunt stocate în mod obișnuit în directorul principal al Microsoft Windows. Screensaver-urile trebuiau să împiedice monitoarele CRT sau cu plasmă să sufere de o afecțiune care apare atunci când ecranul arată aceeași imagine pentru prea mult timp. Deși, ultimele monitoare nu suferă într-o astfel de stare, dar economizoarele de ecran sunt încă folosite pentru a preveni ecranul din motive de securitate.

## Format de fișier SCR
Un protector de ecran este un program de calculator care îl umple cu imagini sau modele animate atunci când nu se efectuează nicio activitate pe computer pentru o perioadă lungă de timp. Screensaver-urile au fost introduse pentru a preveni arderea fosforului pe monitoarele de computer cu plasmă, cu raze catodice (CRT) și OLED. Screensaverele sunt de obicei configurate pentru a aplica un nivel de securitate de bază, solicitând o parolă pentru redeschiderea dispozitivului. Screensaverele sunt de obicei dezvoltate și codificate folosind diverse limbaje de programare, precum și interfețe grafice. În cea mai mare parte, dezvoltatorii de screensavere folosesc limbaje de programare C sau C++, împreună cu biblioteci grafice sau GDI, cum ar fi OpenGL, care funcționează pe multe platforme capabile de randare 3D. Ieșirea screensaverelor este salvată ca fișier executabil portabil.

### Utilizarea fișierului SCR
În monitoarele vechi CRT sau cu plasmă, a fost raportată arderea ecranului deoarece aceeași imagine a fost afișată pe ecran pentru o perioadă lungă de timp. Arderea ecranului este un caz în care proprietățile zonelor expuse de acoperire cu fosfor din interiorul ecranului se schimbă treptat și, în cele din urmă, duc la o imagine de umbră întunecată pe ecran. Așadar, screensaverele trebuiau să schimbe imaginea ecranului în mod continuu și, de obicei, fișierele .scr erau esențiale pentru monitoarele bancomatelor sau automatelor de bilete de cale ferată. Mai târziu, ecranele LCD și versiunile mai avansate de monitoare au rezolvat problema. Prin urmare, screensaverele sunt încă folosite în epoca modernă pentru a proteja dispozitivele inactive de utilizarea a doua persoană. Este nevoie de parola sau modelul pentru a reaccesa dispozitivul.

## Crearea unui screensaver folosind C#
Deși putem crea un screen saver în oricare dintre limbajele de programare .NET, aici este dat limbajul de programare C#:

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
Schimbați extensia fișierului executabil din .exe în .scr. Deci fișierul SCR poate fi numit ScreenSaver.scr.

## Referințe

* [Screensaver](https://en.wikipedia.org/wiki/Screensaver)
* [Scrieți un screensaver care funcționează de fapt](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)


