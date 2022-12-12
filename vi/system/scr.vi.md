{
  "date" : "2021-07-13",
  "keywords" :[ "tệp scr", "tệp scr là gì", "tệp", "ví dụ scr", "phần mở rộng tệp scr","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SCR - Tệp bảo vệ màn hình Windows",
  "description":"Tìm hiểu về định dạng tệp SCR và các API có thể tạo và mở tệp SCR.",
  "linktitle" : "SCR",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-13"
}

## Tệp SCR là gì?
Tệp có phần mở rộng .scr là tệp trình bảo vệ màn hình được sử dụng bởi hệ điều hành Microsoft Windows. Nó bao gồm các hoạt ảnh, đồ họa, trình chiếu hoặc video có thể được sử dụng làm trình bảo vệ màn hình Windows. Các tệp SCR thường được lưu trữ trong thư mục chính của Microsoft Windows. Trình bảo vệ màn hình được cho là để ngăn màn hình máy tính CRT hoặc plasma khỏi tình trạng xảy ra khi màn hình hiển thị cùng một hình ảnh quá lâu. Mặc dù, các màn hình mới nhất không bị tình trạng như vậy nhưng các trình bảo vệ màn hình vẫn được sử dụng để ngăn chặn màn hình vì lý do bảo mật.

## Định dạng tệp SCR
Trình bảo vệ màn hình là một chương trình máy tính lấp đầy nó bằng các hình ảnh hoặc mẫu hoạt hình khi không có hoạt động nào thực hiện trên máy tính trong một thời gian dài. Trình bảo vệ màn hình đã được giới thiệu để ngăn hiện tượng đốt cháy phốt pho trên màn hình máy tính plasma, Cathode Ray Tube (CRT) và OLED. Trình bảo vệ màn hình thường được thiết lập để áp dụng một lớp bảo mật cơ bản, bằng cách yêu cầu mật khẩu để mở lại thiết bị. Trình bảo vệ màn hình thường được phát triển và mã hóa bằng nhiều ngôn ngữ lập trình cũng như giao diện đồ họa. Hầu hết các nhà phát triển trình bảo vệ màn hình sử dụng ngôn ngữ lập trình C hoặc C++, cùng với Thư viện đồ họa hoặc GDI, chẳng hạn như OpenGL, hoạt động trên nhiều nền tảng có khả năng hiển thị 3D. Đầu ra của trình bảo vệ màn hình được lưu dưới dạng tệp thực thi di động.

### Sử dụng tệp SCR
Trong màn hình dựa trên CRT hoặc plasma cũ, hiện tượng cháy màn hình được báo cáo do cùng một hình ảnh được hiển thị trên màn hình trong một thời gian dài. Cháy màn hình là trường hợp đặc tính của các vùng tiếp xúc với lớp phủ phốt pho bên trong màn hình thay đổi dần dần và cuối cùng dẫn đến hình ảnh bóng tối trên màn hình. Vì vậy, các trình bảo vệ màn hình được cho là thay đổi hình ảnh màn hình liên tục và thông thường, các tệp .scr của chúng là những thứ cần thiết cho màn hình của máy bán vé ATM hoặc Đường sắt. Sau đó, màn hình LCD và các phiên bản màn hình cao cấp hơn đã giải quyết được vấn đề. Do đó, trình bảo vệ màn hình vẫn được sử dụng trong thời kỳ hiện đại để bảo vệ các thiết bị nhàn rỗi khỏi việc sử dụng của người thứ hai. Nó yêu cầu mật khẩu hoặc mẫu để truy cập lại thiết bị.

## Tạo Trình bảo vệ màn hình bằng C#
Mặc dù chúng ta có thể tạo trình bảo vệ màn hình bằng bất kỳ ngôn ngữ lập trình .NET nào, ở đây ngôn ngữ lập trình C# được đưa ra:

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
Thay đổi phần mở rộng của tệp thực thi từ .exe thành .scr. Vì vậy, tệp SCR có thể được đặt tên là ScreenSaver.scr.

## Người giới thiệu

* [Trình bảo vệ màn hình](https://vi.wikipedia.org/wiki/Trình bảo vệ màn hình)
* [Viết Trình bảo vệ màn hình thực sự hoạt động](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)


