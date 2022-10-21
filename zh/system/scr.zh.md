{
  "date" : "2021-07-13",
  "keywords" :["scr 文件","什么是 scr 文件","文件","scr 示例","scr 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SCR - Windows 屏幕保护程序文件",
  "description":"了解 SCR 文件格式和可以创建和打开 SCR 文件的 API。",
  "linktitle" : "SCR",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-13"
}

## 什么是一 .SCR 文件？
扩展名为 .scr 的文件是 Microsoft Windows 操作系统使用的屏幕保护程序文件。它包括可用作 Windows 屏幕保护程序的动画、图形、幻灯片或视频。 SCR 文件通常存储在 Microsoft Windows 的主目录中。屏幕保护程序应该防止 CRT 或等离子计算机显示器在屏幕显示相同图像时间过长时出现这种情况。虽然，最新的显示器不会受到这种情况的影响，但出于安全原因，仍然使用屏幕保护程序来阻止屏幕。

## SCR 文件格式
屏幕保护程序是一种计算机程序，当计算机上长时间没有活动时，它会用动画图像或图案填充它。引入屏幕保护程序是为了防止等离子、阴极射线管 (CRT) 和 OLED 计算机显示器上的荧光粉烧屏。屏幕保护程序通常设置为应用基本安全层，需要密码才能重新打开设备。屏幕保护程序通常使用各种编程语言以及图形界面进行开发和编码。大多数屏幕保护程序的开发人员使用 C 或 C++ 编程语言，以及图形库或 GDI，例如 OpenGL，它适用于许多能够进行 3D 渲染的平台。屏幕保护程序输出保存为可移植的可执行文件。

### SCR 文件使用情况
在旧的 CRT 或基于等离子的显示器中，会报告屏幕烧伤，因为同一图像长时间显示在屏幕上。烧屏是指屏幕内部的荧光粉涂层暴露区域的性质逐渐变化并最终导致屏幕上的阴影图像变暗的情况。所以屏幕保护程序应该不断地改变屏幕图像，通常它们的 .scr 文件是 ATM 或铁路售票机监视器的必需品。后来液晶显示器和更高级版本的显示器解决了这个问题。因此，屏幕保护程序在现代仍然使用，以保护空闲设备免受第二人使用。它需要密码或图案才能重新访问设备。

## 使用 C# 创建屏幕保护程序
尽管我们可以使用任何 .NET 编程语言创建屏幕保护程序，但这里给出了 C# 编程语言：

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
将可执行文件的扩展名从 .exe 更改为 .scr。所以 SCR 文件可以命名为 ScreenSaver.scr。

## 参考

* [屏幕保护程序](https://en.wikipedia.org/wiki/Screensaver)
* [编写一个实际工作的屏幕保护程序](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)


