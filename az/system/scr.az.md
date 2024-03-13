{
  "date": "2021-07-13",
  "keywords": [
"scr faylı",
"scr faylı nədir",
"fayl",
"scr nümunəsi",
"scr fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "SCR - Windows Ekran Qoruyucu Faylı",
  "description": "SCR faylları yarada və aça bilən SCR fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "SCR",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-sc-azr"
}
},
  "lastmod": "2021-07-13"
}

## SCR faylı nədir? 
.scr uzantılı fayl Microsoft Windows əməliyyat sistemi tərəfindən istifadə edilən ekran qoruyucu fayldır. O, Windows ekran qoruyucusu kimi istifadə edilə bilən animasiyalar, qrafiklər, slayd şouları və ya videolardan ibarətdir. SCR faylları adətən Microsoft Windows-un əsas kataloqunda saxlanılır. Ekran qoruyucuları CRT və ya plazma kompüter monitorlarının ekranda eyni təsviri çox uzun müddət göstərdiyi zaman yaranan bir vəziyyətlə qarşılaşmasının qarşısını almalı idi. Baxmayaraq ki, ən son monitorlar belə vəziyyətdən əziyyət çəkmirlər, lakin təhlükəsizlik baxımından ekran qoruyucuları hələ də ekranın qarşısını almaq üçün istifadə olunur.

## SCR fayl formatı 
Ekran qoruyucu kompüterdə uzun müddət heç bir fəaliyyət görülmədikdə onu animasiya şəkilləri və ya naxışlarla dolduran kompüter proqramıdır. Ekran qoruyucuları plazmada, Cathode Ray Tube (CRT) və OLED kompüter monitorlarında fosforun yanmasının qarşısını almaq üçün təqdim edilib. Ekran qoruyucuları adətən cihazı yenidən açmaq üçün parol tələb etməklə əsas təhlükəsizlik qatını tətbiq etmək üçün qurulur. Ekran qoruyucuları adətən müxtəlif proqramlaşdırma dillərindən, eləcə də qrafik interfeyslərdən istifadə etməklə hazırlanır və kodlaşdırılır. Əsasən ekran qoruyucularının tərtibatçıları C və ya C++ proqramlaşdırma dillərindən, Qrafik kitabxanalardan və ya 3D göstərə bilən bir çox platformada işləyən OpenGL kimi GDI-lərdən istifadə edirlər. Ekran qoruyucularının çıxışı portativ icra edilə bilən fayl kimi saxlanılır.

### SCR faylının istifadəsi
Köhnə CRT və ya plazma əsaslı monitorlarda eyni görüntü uzun müddət ekranda göstərildiyi üçün ekranın yanması barədə məlumat verilmişdir. Ekranın yanması, ekranın içərisində olan fosfor örtüyünün açıq sahələrinin xüsusiyyətlərinin tədricən dəyişdiyi və nəticədə ekranda qaranlıq bir kölgə şəklinə səbəb olduğu haldır. Beləliklə, ekran qoruyucuları ekran görüntüsünü davamlı olaraq dəyişdirməli idi və adətən onlar .scr faylları ATM və ya Dəmiryol bilet maşınlarının monitorları üçün zəruri elementlər idi. Daha sonra LCD-lər və monitorların daha təkmil versiyaları problemi həll etdi. Buna görə də ekran qoruyucuları hələ də müasir dövrdə boş cihazları ikinci şəxsin istifadəsindən qorumaq üçün istifadə olunur. Cihaza yenidən daxil olmaq üçün parol və ya nümunə tələb olunur.

## C# istifadə edərək ekran qoruyucusu yaratmaq
.NET proqramlaşdırma dillərindən hər hansı birində ekran qoruyucusu yarada bilsək də, burada C# proqramlaşdırma dili verilmişdir:

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
İcra edilə bilən faylın genişləndirilməsini .exe-dən .scr-ə dəyişdirin. Beləliklə, SCR faylı ScreenSaver.scr kimi adlandırıla bilər.

## İstinadlar 

* [Screensaver](https://en.wikipedia.org/wiki/Screensaver)

* [Əslində İşləyən Ekran Qoruyucusu Yazın](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)



