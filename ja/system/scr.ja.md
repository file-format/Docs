{
  "date" : "2021-07-13",
  "keywords" :[ "scr ファイル", "scr ファイルとは", "ファイル", "scr の例", "scr ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SCR - Windows スクリーンセーバー ファイル",
  "description":"SCR ファイル形式と,SCR ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "SCR",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-13"
}

## .SCR オプション番号
拡張子が .scr のファイルは、Microsoft Windows オペレーティング システムで使用されるスクリーン セーバー ファイルです。 Windows スクリーンセーバーとして使用できるアニメーション、グラフィック、スライド ショー、またはビデオで構成されます。 SCR ファイルは通常、Microsoft Windows のメイン ディレクトリに保存されます。スクリーン セーバーは、CRT またはプラズマ コンピューター モニターが、画面に同じ画像が長時間表示されたときに発生する状態に陥るのを防ぐためのものでした。ただし、最新のモニターはこのような状態に陥ることはありませんが、セキュリティ上の理由からスクリーン セーバーを使用して画面が表示されないようにしています。

## SCR ファイル形式
スクリーン セーバーは、コンピューターで長時間何も操作が行われていない場合に、アニメーション イメージまたはパターンで画面を埋めるコンピューター プログラムです。スクリーンセーバーは、プラズマ、陰極線管 (CRT)、および OLED コンピューター モニターでの蛍光体の焼き付きを防ぐために導入されました。通常、スクリーンセーバーは、デバイスを再度開くときにパスワードを要求することで、基本的なセキュリティ層を適用するように設定されています。通常、スクリーンセーバーは、さまざまなプログラミング言語とグラフィック インターフェイスを使用して開発およびコーディングされます。ほとんどのスクリーンセーバーの開発者は、3D レンダリングが可能な多くのプラットフォームで動作する OpenGL などのグラフィカル ライブラリまたは GDI と共に、C または C++ プログラミング言語を使用します。スクリーンセーバーの出力は、移植可能な実行可能ファイルとして保存されます。

### SCR ファイルの使用法
古い CRT またはプラズマ ベースのモニターでは、同じ画像が長時間画面に表示されるため、画面の焼き付きが報告されていました。スクリーン バーンは、スクリーン内部の蛍光体コーティングの露出領域の特性が徐々に変化し、最終的にスクリーン上の暗い影のイメージにつながる場合です。そのため、スクリーンセーバーは画面イメージを継続的に変更することになっており、通常、.scr ファイルは ATM や鉄道の券売機のモニターに不可欠でした。その後、LCD およびより高度なバージョンのモニターで問題が解決されました。したがって、スクリーンセーバーは、アイドル状態のデバイスを 2 人目の使用から保護するために、現代でも使用されています。デバイスに再アクセスするには、パスワードまたはパターンが必要です。

## C# を使用してスクリーンセーバーを作成する
任意の .NET プログラミング言語でスクリーン セーバーを作成できますが、ここでは C# プログラミング言語を示します。

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
実行可能ファイルの拡張子を .exe から .scr に変更します。そのため、SCR ファイルは ScreenSaver.scr という名前にすることができます。

## 参考文献

* [スクリーンセーバー](https://en.wikipedia.org/wiki/Screensaver)
* [実際に動くスクリーンセーバーを書く](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)


