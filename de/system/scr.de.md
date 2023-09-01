{
  "date" : "2021-07-13",
  "keywords" :[ "scr-Datei", "was ist eine scr-Datei", "Datei", "scr-Beispiel", "scr-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SCR - Windows-Bildschirmschonerdatei",
  "description":"Erfahren Sie mehr über das SCR-Dateiformat und APIs, die SCR-Dateien erstellen und öffnen können.",
  "linktitle" : "SCR",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-13"
}

## Was ist eine SCR-Datei?
Eine Datei mit der Erweiterung .scr ist eine Bildschirmschonerdatei, die vom Microsoft Windows-Betriebssystem verwendet wird. Es umfasst Animationen, Grafiken, Diashows oder Videos, die als Windows-Bildschirmschoner verwendet werden können. SCR-Dateien werden üblicherweise im Hauptverzeichnis von Microsoft Windows gespeichert. Die Bildschirmschoner sollten verhindern, dass CRT- oder Plasma-Computermonitore unter einem Zustand leiden, der auftritt, wenn der Bildschirm zu lange dasselbe Bild zeigt. Die neuesten Monitore leiden zwar nicht unter einem solchen Zustand, aber die Bildschirmschoner werden immer noch verwendet, um den Bildschirm aus Sicherheitsgründen zu verhindern.

## SCR-Dateiformat
Ein Bildschirmschoner ist ein Computerprogramm, das es mit animierten Bildern oder Mustern füllt, wenn längere Zeit keine Aktivität auf einem Computer ausgeführt wird. Die Bildschirmschoner wurden eingeführt, um das Einbrennen von Phosphor auf Plasma-, Kathodenstrahlröhren- (CRT) und OLED-Computermonitoren zu verhindern. Bildschirmschoner sind normalerweise so eingerichtet, dass sie eine grundlegende Sicherheitsebene anwenden, indem sie ein Passwort erfordern, um das Gerät erneut zu öffnen. Bildschirmschoner werden in der Regel mit verschiedenen Programmiersprachen sowie Grafikschnittstellen entwickelt und codiert. Meistens verwenden die Entwickler von Bildschirmschonern die Programmiersprachen C oder C++ zusammen mit grafischen Bibliotheken oder GDIs wie OpenGL, das auf vielen Plattformen funktioniert, die 3D-Rendering ermöglichen. Die Ausgabe des Bildschirmschoners wird als portable ausführbare Datei gespeichert.

### Nutzung der SCR-Datei
Bei den alten CRT- oder Plasma-basierten Monitoren wurde das Einbrennen des Bildschirms gemeldet, weil das gleiche Bild über einen langen Zeitraum auf dem Bildschirm angezeigt wurde. Das Einbrennen des Bildschirms ist ein Fall, bei dem sich die Eigenschaften der belichteten Bereiche der Phosphorbeschichtung im Inneren des Bildschirms allmählich ändern und schließlich zu einem dunklen Schattenbild auf dem Bildschirm führen. Die Bildschirmschoner sollten also das Bildschirmbild ständig ändern und normalerweise waren die .scr-Dateien für die Monitore von Geldautomaten oder Bahnfahrkartenautomaten unerlässlich. Später lösten LCDs und fortschrittlichere Versionen von Monitoren das Problem. Daher werden die Bildschirmschoner auch in der Neuzeit verwendet, um die ungenutzten Geräte vor der Nutzung durch die zweite Person zu schützen. Für den erneuten Zugriff auf das Gerät ist das Kennwort oder Muster erforderlich.

## Erstellen eines Bildschirmschoners mit C#
Obwohl wir einen Bildschirmschoner in jeder der .NET-Programmiersprachen erstellen können, ist hier die Programmiersprache C# angegeben:

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
Ändern Sie die Erweiterung der ausführbaren Datei von .exe in .scr. Die SCR-Datei kann also als ScreenSaver.scr bezeichnet werden.

## Verweise

* [Bildschirmschoner](https://en.wikipedia.org/wiki/Screensaver)
* [Schreiben Sie einen Bildschirmschoner, der tatsächlich funktioniert](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)


