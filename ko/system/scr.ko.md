{
  "date" : "2021-07-13",
  "keywords" :[ "scr 파일", "scr 파일이란", "파일", "scr 예제", "scr 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SCR - Windows 화면 보호기 파일",
  "description":"SCR 파일 형식과 SCR 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "SCR",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-13"
}

## .SCR 파일이란?
확장자가 .scr인 파일은 Microsoft Windows 운영 체제에서 사용하는 화면 보호기 파일입니다. Windows 화면 보호기로 사용할 수 있는 애니메이션, 그래픽, 슬라이드 쇼 또는 비디오로 구성됩니다. SCR 파일은 일반적으로 Microsoft Windows의 기본 디렉토리에 저장됩니다. 스크린 세이버는 CRT 또는 플라즈마 컴퓨터 모니터가 동일한 이미지를 너무 오랫동안 화면에 표시할 때 발생하는 상태로 고통받는 것을 방지하기 위한 것이었습니다. 그러나 최신 모니터는 이러한 상태에서 문제가 발생하지 않지만 보안상의 이유로 여전히 화면 보호기를 사용하여 화면을 방지합니다.

## SCR 파일 형식
화면 보호기는 컴퓨터에서 오랫동안 아무런 활동도 수행하지 않을 때 애니메이션 이미지나 패턴으로 화면을 채우는 컴퓨터 프로그램입니다. 스크린 세이버는 플라즈마, CRT(Cathode Ray Tube) 및 OLED 컴퓨터 모니터에서 형광체 번인을 방지하기 위해 도입되었습니다. 화면 보호기는 일반적으로 장치를 다시 열 때 암호를 요구하여 기본 보안 계층을 적용하도록 설정됩니다. 화면 보호기는 일반적으로 다양한 프로그래밍 언어와 그래픽 인터페이스를 사용하여 개발 및 코딩됩니다. 대부분의 화면 보호기 개발자는 3D 렌더링이 가능한 많은 플랫폼에서 작동하는 OpenGL과 같은 그래픽 라이브러리 또는 GDI와 함께 C 또는 C++ 프로그래밍 언어를 사용합니다. 화면 보호기 출력은 이식 가능한 실행 파일로 저장됩니다.

### SCR 파일 사용
구형 CRT 또는 플라즈마 기반 모니터에서는 동일한 이미지가 오랫동안 화면에 표시되어 화면 화상이 보고되었습니다. 화면 번은 화면 내부의 형광체 코팅의 노출 영역의 특성이 점차적으로 변하여 결국 화면에 어두운 그림자 이미지로 이어지는 경우입니다. 따라서 화면 보호기는 화면 이미지를 지속적으로 변경해야 했으며 일반적으로 .scr 파일은 ATM 또는 철도 발권기의 모니터에 필수적이었습니다. 나중에 LCD 및 고급 버전의 모니터가 문제를 해결했습니다. 따라서 화면 보호기는 두 번째 사람이 사용하지 않는 장치를 보호하기 위해 현대 시대에도 여전히 사용됩니다. 장치에 다시 액세스하려면 암호 또는 패턴이 필요합니다.

## C#을 사용하여 화면 보호기 만들기
모든 .NET 프로그래밍 언어로 화면 보호기를 만들 수 있지만 여기에 C# 프로그래밍 언어가 제공됩니다.

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
실행 파일의 확장자를 .exe에서 .scr로 변경합니다. 따라서 SCR 파일의 이름은 ScreenSaver.scr로 지정할 수 있습니다.

## 참고문헌

* [스크린세이버](https://en.wikipedia.org/wiki/Screensaver)
* [실제로 작동하는 화면 보호기 작성](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)


