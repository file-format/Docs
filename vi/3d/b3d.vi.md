{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp B3D; được sử dụng trong trò chơi blitz3d và API có thể mở và tạo tệp B3D.",
  "title" :"B3D - Tệp mô hình thực thể Blitz3D",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## Tệp B3D là gì?

Tệp có phần mở rộng .b3d là tệp mô hình được Blitz3D sử dụng. Tệp này có thể chứa các mô hình trò chơi điện tử cho các nhân vật, tòa nhà, địa hình và các đối tượng khác. Blitz3D là ngôn ngữ lập trình được sử dụng để tạo **trò chơi blitz3d**. Blitz3D là một ngôn ngữ lập trình mạnh mẽ, linh hoạt và dễ sử dụng được thiết kế cho mục đích duy nhất là viết trò chơi điện tử. Các nhà phát triển có thể tạo các trò chơi 3D đầy hành động, giải đố 2D, phiêu lưu, RPG, bất cứ thứ gì chỉ bằng cách sử dụng Blitz3D.

Blitz3D dựa trên ngôn ngữ lập trình BASIC; cũng dễ học và sử dụng. Tất cả những sự thật này đang làm cho Blitz trở nên lý tưởng cho người mới bắt đầu cũng như những lập trình viên có kinh nghiệm hơn. Mặc dù các tính năng được coi là hơi lỗi thời so với hầu hết các công cụ 3D hiện đại, Blitz3D vẫn tiếp tục được nhiều lập trình viên trò chơi trên toàn thế giới sử dụng.

## Tóm tắt lịch sử của Blitz3D

Blitz3D về cơ bản được phát hành cho hệ điều hành Microsoft Windows vào tháng 9 năm 2001, để cạnh tranh với các ngôn ngữ phát triển trò chơi tương tự khác. Blitz3D là phiên bản nâng cấp so với công cụ 2D BlitzBasic trước đó, mở rộng bộ lệnh của nó với việc bổ sung API cho công cụ 3D dựa trên DirectX 7. Người dùng Blitz3D cũng nên so sánh BlitzMax, một công cụ sau này của BlitzBasic. BlitzMax là phiên bản phức tạp nhưng mạnh hơn của Blitz3D, hỗ trợ các ngôn ngữ lập trình hướng đối tượng. Đây là API đồ họa được cập nhật để phù hợp hơn với các ký tự Unicode, OpenGL và xuất sang OSX và Linux thay vì chỉ Windows.

## Ví dụ B3D
Một tệp b3d chứa 1 đoạn TEXS, 1 đoạn BRUS và 1 đoạn NODE sẽ có dạng như sau:

```
BB3D
  1
  TEXS
    ...list of textures...
  BRUS
    ...list of brushes...
  NODE
    ...stuff in the node...
```
Một lưới đơn giản, không hoạt hình và không có kết cấu sẽ trông như thế này:

```
BB3D
  1                           ;version
  NODE
    "root_node"               ;node name
    0,0,0                     ;position
    1,1,1                     ;scale
    1,0,0,0                   ;rotation
    MESH                      ;the mesh
      -1                      ;brush: no brush
      VRTS                    ;vertices in the mesh
        0                     ;no normal/color info in verts
        0,0                   ;no texture coords in verts
        {x,y,z...}            ;vertex coordinates
      TRIS                    ;triangles in the mesh
        -1                    ;no brush for this triangle
        {v0,v1,v2...}         ;vertices
```


## Người giới thiệu
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [CƠ BẢN Blitz](https://vi.wikipedia.org/wiki/Blitz_BASIC)

