{
  "date" : "2021-07-13",
  "keywords" : [ "scr file", "what is an scr file", "file", "scr example", "scr file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "SCR - Windows Screensaver File",
  "description":"Learn about SCR file format and APIs that can create and open SCR files.",
  "linktitle" : "SCR",
  "menu" : {
    "docs" : {
      "parent" : "system"
    }
  },
  "lastmod" : "2021-07-13"
}

## What is an SCR file? 
A file with .scr extension is a screen saver file used by the Microsoft Windows operating system. It comprises animations, graphic, slide show, or video that can be used as a Windows screensaver. SCR files are commonly stored in the main directory of Microsoft Windows. The Screen savers were supposed to prevent CRT or plasma computer monitors from suffering with a condition that occurs when the screen shows the same image for too long. Although, the latest monitors do not suffer in such condition, but the screen savers are still used to prevent the screen for security reasons.

## SCR File Format 
A screen saver is a computer program that fills it with animated images or patterns when no activity performs on a computer for a long time. The screensavers were introduced to prevent phosphor burn-in on plasma, Cathode Ray Tube (CRT) and OLED computer monitors. Screensavers are usually set up to apply a basic layer of security, by requiring a password to re-open the device. Screensavers are usually developed and coded using various programming languages as well as graphics interfaces. Mostly the developers of screensavers use the C or C++ programming languages, along with Graphical libraries or GDIs, such as OpenGL, which works on many platforms capable of 3D rendering. The screensavers output is saved as a portable executable file.

### SCR file usage
In the Old CRT or plasma based monitors the screen burn was reported because the same image was displayed on the screen for a long period. The screen burn is a case when the properties of the exposed areas of phosphor coating inside of the screen change gradually and eventually leading to a darkened shadow image on the screen. So the screensavers were supposed to change the screen image continuously and usually they .scr files were essentials for the monitors of ATM or Railway ticketing machines. Later on LCDs and more advanced versions of monitors resolved the issue. Therefore the screensavers are still used in modern era to protect the idle devices from the second person use. It requires the password or pattern to re-access the device.

## Creating a Screensaver using C#
Although we can create a screen saver in any of the .NET programming languages, here the C# programming language is given:

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
Change the extension of the executable file from .exe to .scr. So the SCR file can be named as ScreenSaver.scr.

## References 

* [Screensaver](https://en.wikipedia.org/wiki/Screensaver)
* [Write a Screensaver that Actually Works](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)

