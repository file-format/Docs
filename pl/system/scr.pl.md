{
  "date" : "2021-07-13",
  "keywords" :["plik scr", "co to jest plik scr", "plik", "przykład scr", "rozszerzenie pliku scr", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SCR - plik wygaszacza ekranu systemu Windows",
  "description":"Poznaj format pliku SCR i interfejsy API, które mogą tworzyć i otwierać pliki SCR.",
  "linktitle" : "SCR",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-13"
}

## Czym jest plik SCR?
Plik z rozszerzeniem .scr to plik wygaszacza ekranu używany przez system operacyjny Microsoft Windows. Zawiera animacje, grafikę, pokaz slajdów lub wideo, które można wykorzystać jako wygaszacz ekranu systemu Windows. Pliki SCR są zwykle przechowywane w głównym katalogu systemu Microsoft Windows. Wygaszacze ekranu miały zapobiegać cierpieniu monitorów CRT lub plazmowych na stan, który występuje, gdy ekran wyświetla ten sam obraz przez zbyt długi czas. Chociaż najnowsze monitory nie cierpią w takim stanie, ale wygaszacze ekranu są nadal używane do zapobiegania ekranowi ze względów bezpieczeństwa.

## Format pliku SCR
Wygaszacz ekranu to program komputerowy, który wypełnia go animowanymi obrazami lub wzorami, gdy na komputerze nie jest wykonywana żadna czynność przez dłuższy czas. Wygaszacze ekranu zostały wprowadzone, aby zapobiec wypaleniu luminoforu na monitorach plazmowych, kineskopowych (CRT) i OLED. Wygaszacze ekranu są zwykle konfigurowane w celu zastosowania podstawowej warstwy zabezpieczeń, wymagając podania hasła w celu ponownego otwarcia urządzenia. Wygaszacze ekranu są zwykle opracowywane i kodowane przy użyciu różnych języków programowania, a także interfejsów graficznych. Twórcy wygaszaczy ekranu używają głównie języków programowania C lub C++, a także bibliotek graficznych lub GDI, takich jak OpenGL, który działa na wielu platformach zdolnych do renderowania 3D. Dane wyjściowe wygaszaczy ekranu są zapisywane jako przenośny plik wykonywalny.

### Użycie pliku SCR
W starych monitorach CRT lub plazmowych zgłaszano wypalanie ekranu, ponieważ ten sam obraz był wyświetlany na ekranie przez długi czas. Wypalenie ekranu to przypadek, w którym właściwości odsłoniętych obszarów powłoki luminoforowej wewnątrz ekranu zmieniają się stopniowo, prowadząc ostatecznie do przyciemnienia cienia obrazu na ekranie. Tak więc wygaszacze ekranu miały stale zmieniać obraz ekranu i zazwyczaj pliki .scr były niezbędne dla monitorów bankomatów lub biletomatów kolejowych. Później problem rozwiązały monitory LCD i bardziej zaawansowane wersje monitorów. Dlatego wygaszacze ekranu są nadal używane w epoce nowożytnej, aby chronić bezczynne urządzenia przed użyciem przez drugą osobę. Wymaga hasła lub wzoru, aby ponownie uzyskać dostęp do urządzenia.

## Tworzenie wygaszacza ekranu przy użyciu języka C#
Chociaż wygaszacz ekranu możemy stworzyć w dowolnym języku programowania .NET, tutaj podany jest język programowania C#:

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
Zmień rozszerzenie pliku wykonywalnego z .exe na .scr. Tak więc plik SCR można nazwać jako ScreenSaver.scr.

## Bibliografia

* [Wygaszacz ekranu](https://en.wikipedia.org/wiki/Screensaver)
* [Napisz wygaszacz ekranu, który faktycznie działa](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)


