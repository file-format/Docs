{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"Tệp GCODE - Tệp .gcode là gì và làm cách nào để mở tệp?",
   "description":"Tìm hiểu về định dạng tệp GCODE và các API có thể tạo và mở tệp GCODE.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-vi",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## Tệp GCODE là gì?

**Tệp GCODE** là tệp văn bản thuần túy chứa hướng dẫn điều khiển máy công cụ được vi tính hóa và máy in 3D; Mã G hoặc Mã hình học là ngôn ngữ được sử dụng để điều khiển chuyển động và hoạt động của các máy **CNC (Điều khiển số máy tính)**; Máy CNC bao gồm máy phay, máy tiện, bộ định tuyến và máy in 3D.

Các lệnh mã G được viết bằng cú pháp cụ thể thường bao gồm các chữ cái và số; mỗi lệnh hướng dẫn máy thực hiện hành động cụ thể như di chuyển dao đến vị trí cụ thể, thay dao hoặc điều chỉnh tốc độ.

Mã G thường được tạo bởi phần mềm **CAM (Computer-Aided Manufacturing)**; Phần mềm CAM lấy mô hình 3D hoặc thiết kế 2D và tạo ra các đường chạy dao và hướng dẫn mã G tương ứng; Sau đó, tệp mã G được tải vào máy CNC hoặc máy in 3D để thực thi.

Các tệp mã G thường có phần mở rộng tệp .nc hoặc .gcode, ví dụ: program.nc hoặc print.gcode.

## Cấu trúc tệp GCODE:

Tệp GCODE là tệp văn bản thuần túy với mỗi dòng chứa lệnh cụ thể; các lệnh này bao gồm từ điều khiển chuyển động của máy đến điều chỉnh nhiệt độ, tốc độ và các thông số quan trọng khác để chế tạo vật thể.

Cú pháp của GCODE bao gồm sự kết hợp của các chữ cái và số; mỗi đại diện cho hành động hoặc tham số riêng biệt; các lệnh phổ biến bao gồm G0 và G1 để di chuyển, M3 và M5 để điều khiển trục xoay, và S và F để điều chỉnh tốc độ và tốc độ tiến dao tương ứng.

## Tạo GCODE:

Phần mềm cắt lát như **Simplify3D** và **Slic3r**, chuyển các bản vẽ Thiết kế có sự hỗ trợ của máy tính (CAD) sang GCODE; Phần mềm CAD được sử dụng để tạo mô hình 3D, sau đó được xuất ở các định dạng như STL; phần mềm cắt lát lấy các mô hình này và tạo tệp GCODE chỉ định các chi tiết như chiều cao lớp, tốc độ in và cài đặt nhiệt độ.

## Ví dụ về GCODE

Dưới đây là ví dụ đơn giản về mã G để di chuyển máy CNC:

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## Làm cách nào để mở tệp GCODE?

Để mở tệp mã G, bạn có thể sử dụng nhiều loại phần mềm khác nhau tùy theo nhu cầu của mình.

Nếu bạn đã tạo mã G cho máy in 3D; bạn có thể mở nó bằng phần mềm đi kèm với máy in 3D hoặc phần mềm cắt chuyên dụng; các ví dụ bao gồm **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** hoặc **Repetier-Host**; những chương trình này thường có giao diện thân thiện với người dùng cho phép bạn tải và hiển thị mã G.

Các tệp GCODE là văn bản thuần túy nên bạn có thể mở chúng bằng bất kỳ trình soạn thảo văn bản nào; các trình soạn thảo văn bản phổ biến bao gồm **Notepad (trên Windows)**, **TextEdit (trên macOS)** hoặc **Gedit (trên Linux)**; chỉ cần **nhấp chuột phải** vào tệp mã G, chọn **Mở bằng** và chọn trình soạn thảo văn bản.

