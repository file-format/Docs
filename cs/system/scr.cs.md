{
  "date" : "2021-07-13",
  "keywords" :[ "soubor scr", "co je soubor scr", "soubor", "příklad scr", "přípona souboru scr", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SCR - soubor spořiče obrazovky Windows",
  "description":"Další informace o formátu souboru SCR a rozhraních API, která mohou vytvářet a otevírat soubory SCR.",
  "linktitle" : "SCR",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-13"
}

## Co je soubor SCR?
Soubor s příponou .scr je soubor spořiče obrazovky používaný operačním systémem Microsoft Windows. Obsahuje animace, grafiku, prezentaci nebo video, které lze použít jako spořič obrazovky Windows. Soubory SCR jsou běžně uloženy v hlavním adresáři Microsoft Windows. Spořiče obrazovky měly zabránit tomu, aby CRT nebo plazmové počítačové monitory trpěly stavem, který nastává, když obrazovka ukazuje stejný obraz příliš dlouho. Nejnovější monitory sice v takovém stavu netrpí, ale spořiče obrazovky se stále používají k zamezení obrazovky z bezpečnostních důvodů.

## Formát souboru SCR
Spořič obrazovky je počítačový program, který ji vyplní animovanými obrázky nebo vzory, když na počítači po dlouhou dobu neprobíhá žádná činnost. Spořiče obrazovky byly zavedeny, aby zabránily vypalování fosforu na plazmových, katodových trubicích (CRT) a OLED počítačových monitorech. Spořiče obrazovky jsou obvykle nastaveny tak, aby aplikovaly základní vrstvu zabezpečení tím, že pro opětovné otevření zařízení vyžadují heslo. Spořiče obrazovky jsou obvykle vyvíjeny a kódovány pomocí různých programovacích jazyků a grafických rozhraní. Vývojáři spořičů obrazovky většinou používají programovací jazyky C nebo C++ spolu s grafickými knihovnami nebo GDI, jako je OpenGL, které funguje na mnoha platformách schopných 3D vykreslování. Výstup spořičů obrazovky je uložen jako přenosný spustitelný soubor.

### Využití souboru SCR
U starých CRT nebo plazmových monitorů bylo vypálení obrazovky hlášeno, protože stejný obraz byl zobrazován na obrazovce po dlouhou dobu. Vypálení obrazovky je případ, kdy se vlastnosti exponovaných oblastí fosforového povlaku uvnitř obrazovky postupně mění a nakonec vedou ke ztmavení stínového obrazu na obrazovce. Spořiče obrazovky tedy měly neustále měnit obraz obrazovky a obvykle byly soubory .scr nezbytností pro monitory bankomatů nebo železničních automatů na jízdenky. Později tento problém vyřešily LCD a pokročilejší verze monitorů. Proto se spořiče obrazovky v moderní době stále používají k ochraně nečinných zařízení před použitím druhou osobou. Pro opětovný přístup k zařízení vyžaduje heslo nebo vzor.

## Vytvoření spořiče obrazovky pomocí C#
Přestože můžeme vytvořit spořič obrazovky v kterémkoli z programovacích jazyků .NET, zde je uveden programovací jazyk C#:

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
Změňte příponu spustitelného souboru z .exe na .scr. Takže soubor SCR může být pojmenován jako ScreenSaver.scr.

## Reference

* [Spořič obrazovky](https://en.wikipedia.org/wiki/Screensaver)
* [Napište spořič obrazovky, který skutečně funguje](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)


