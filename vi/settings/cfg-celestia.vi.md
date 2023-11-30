{
"ngày": "27-09-2023",
  "keywords": [
"cfg",
"tệp cfg",
"tệp cấu hình cfg celestia",
"tập tin cfg là gì",
"làm thế nào để mở tập tin cfg",
"tài liệu",
"phần mở rộng tập tin cfg",
"sự mở rộng"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Định dạng tệp CFG - Tệp cấu hình Celestia",
  "description":"Tìm hiểu về định dạng tệp cấu hình CFG Celestia và các API có thể tạo và mở tệp CFG.",
"linktitle":"CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia",
      "parent": "settings"
}
},
"lastmod": "2023-09-27"
}

## Tập tin CFG là gì?

Tệp cấu hình Celestia là tệp văn bản thuần túy được sử dụng bởi Celestia, chương trình mô phỏng vũ trụ 3D. Những tệp này rất quan trọng để tùy chỉnh cách Celestia hoạt động, những thiên thể nào được hiển thị và cách chương trình xuất hiện. Tuy nhiên, việc chỉnh sửa những tệp này đòi hỏi phải chú ý cẩn thận vì những thay đổi không đúng cách có thể làm gián đoạn quá trình tải của Celestia, khiến nó không thể chạy bình thường.

## Celestia

Celestia là phần mềm mô phỏng thiên văn học 3D mã nguồn mở, miễn phí cho phép người dùng khám phá và hình dung vũ trụ theo cách tương tác và thực tế cao. Nó được phát triển bởi Chris Laurel và được phát hành lần đầu tiên vào đầu những năm 2000. Celestia có sẵn cho các hệ điều hành Windows, macOS và Linux.

Các tính năng và khía cạnh chính của Celestia bao gồm:

- **Hình ảnh 3D thực tế:** Celestia cung cấp hình ảnh chi tiết và chính xác về hệ mặt trời của chúng ta cũng như các ngôi sao, thiên hà và các thiên thể khác. Nó sử dụng các mô hình và kết cấu 3D chất lượng cao để tạo ra trải nghiệm trực quan sống động.

- **Cơ sở dữ liệu thiên thể mở rộng:** Phần mềm đi kèm với cơ sở dữ liệu tích hợp rộng lớn về các thiên thể đã biết, bao gồm các ngôi sao, hành tinh, mặt trăng, tiểu hành tinh, sao chổi và tàu vũ trụ. Người dùng có thể dễ dàng định vị và khám phá những đối tượng này.

- **Độ chính xác về mặt khoa học:** Mặc dù Celestia là công cụ trực quan hóa nhưng nó nhằm mục đích thể hiện các thiên thể và hiện tượng thiên thể một cách chính xác nhất có thể, dựa trên dữ liệu khoa học có sẵn.

## Định dạng tệp được Celestia sử dụng

Celestia sử dụng nhiều định dạng tệp khác nhau cho các khía cạnh khác nhau của mô phỏng thiên văn học 3D. Dưới đây là một số định dạng tệp chính được Celestia sử dụng:

1. **Tệp cấu hình (.cel)**
- *Mô tả*: Tệp văn bản thuần túy cho phép người dùng tùy chỉnh hành vi, hình thức và nội dung của Celestia.
- *Mục đích*: Tùy chỉnh cài đặt, xác định vị trí và chỉ định các thiên thể.

2. **Mô hình 3D và mắt lưới**
- *Định dạng*: [.3ds](/vi/3d/3ds/), [.obj](/vi/3d/obj/), [.dae](/vi/3d/dae/), .ac
- *Mô tả*: Các định dạng tệp mô hình 3D được hỗ trợ dùng để hiển thị các thiên thể và tàu vũ trụ.
- *Mục đích*: Hiển thị vật thể 3D trong Celestia.

3. **Tệp kết cấu**
- *Định dạng*: [.jpg](/vi/image/jpeg/), [.png](/vi/image/png/), [.dds](/vi/image/dds/)
- *Mô tả*: Những tệp này cung cấp kết cấu bề mặt cho các thiên thể.
- *Mục đích*: Ánh xạ họa tiết lên mô hình 3D để có hình thức chân thực.

4. **Danh mục sao và tệp dữ liệu**
- *Định dạng*: Định dạng tùy chỉnh, [.csv](/vi/ Spreadsheet/csv/), [.tsv](/vi/ Spreadsheet/tsv/)
- *Mô tả*: Tệp dữ liệu dùng để thể hiện các ngôi sao và các thiên thể khác, đảm bảo mô phỏng chính xác.
- *Mục đích*: Trình bày chính xác các thiên thể.

5. **Bản đồ khối kết cấu**
- *Mô tả*: Bản đồ khối được sử dụng để mô phỏng hình dáng của các thiên thể ở xa như các thiên hà.
- *Mục đích*: Hiển thị các vật thể ở xa với kết cấu chân thực.

6. **Tệp tập lệnh**
- *Mô tả*: Những tệp này chứa các tập lệnh tùy chỉnh được viết bằng ngôn ngữ tập lệnh của Celestia.
- *Mục đích*: Cho phép người dùng tạo các sự kiện và hoạt ảnh động trong vũ trụ của Celestia.

## Tập tin cấu hình Celestia

Dưới đây là tổng quan cơ bản về những gì bạn có thể làm với tệp cấu hình Celestia:

1. **Đặt vị trí của bạn**: Bạn có thể chỉ định vị trí của mình trên Trái đất bằng cách sử dụng các thông số vĩ độ, kinh độ và độ cao. Điều này cho phép Celestia hiển thị chính xác bầu trời đêm từ vị trí của bạn.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **Tùy chỉnh các tùy chọn xem của bạn:** Bạn có thể điều chỉnh các tùy chọn xem khác nhau như trường nhìn, cài đặt thời gian và tùy chọn hiển thị.

```
Viewpoint
{
    Location "My Location"
    Follow "Earth"
    Eye [0.0 0.0 0.0]
    Center [0.0 0.0 0.0]
    Up [0.0 1.0 0.0]
    Fov 45
}

Time
{
    Date "2023-09-25T12:00:00.000Z"
    Clock "Now"
}

Rendering
{
    Atmosphere false
    Stars 7
    Planetshine 0.25
}

```

3. **Đang tải các thiên thể:** Bạn có thể thêm các thiên thể như sao, hành tinh, tiểu hành tinh, tàu vũ trụ, v.v. vào mô phỏng của mình. Mỗi đối tượng được xác định trong tệp cấu hình với các thuộc tính của nó.

```
Star "Sun"
{
    RA 0
    Dec 0
    Distance 0
    AppMag -26.74
    SpectralType "G2V"
}

Planet "Earth"
{
    Parent "Sol"
    Texture "earth.jpg"
    Radius 6371
    EllipticalOrbit
    {
        Period 365.25
        SemiMajorAxis 149.6e6
        Eccentricity 0.017
        Inclination 0
        AscendingNode 0
        ArgOfPericenter 102.94
        MeanAnomaly 100.464
}
}
```

4. **Xác định tàu vũ trụ:** Bạn có thể tạo tàu vũ trụ hư cấu của riêng mình hoặc sử dụng tàu vũ trụ có thật bằng cách chỉ định các tham số của chúng như vị trí, hướng và mô hình 3D.

```
Spacecraft "Voyager 1"
{
    Parent "Sol"
    Class "spacecraft"
    Mesh "voyager.3ds"
    Radius 0.01
    EllipticalOrbit
    {
        Period 30700
        SemiMajorAxis 1.08e11
        Eccentricity 0.044
        Inclination 3.4
        AscendingNode 49.0
        ArgOfPericenter 44.0
        MeanAnomaly 35.0
}
}
```

5. **Tạo tập lệnh:** Bạn có thể viết tập lệnh bằng ngôn ngữ tập lệnh tùy chỉnh của Celestia để tạo các sự kiện và hoạt ảnh động.

## Làm cách nào để mở tập tin CFG?

Các chương trình mở hoặc tham chiếu tệp CFG

- Celestia (Miễn phí) cho (Windows, Mac, Linux)

## Các tập tin CFG khác

Dưới đây là các loại tệp khác sử dụng phần mở rộng tệp **.cfg**.

**Cài đặt**
- [CFG - Tệp cấu hình Celestia](/vi/settings/cfg-celestia/)
- [CFG - Tệp kết nối máy chủ Citrix](/vi/settings/cfg-citrix/)
- [CFG - Tệp cấu hình MAME](/vi/settings/cfg-mame/)
- [CFG - Tệp cấu hình LightWave](/vi/settings/cfg-lightwave/)

**Trò chơi**
- [CFG - Tệp ngôn ngữ đánh dấu Wesnoth](/vi/game/cfg-wesnoth/)
- [CFG - Tệp cấu hình MUGEN](/vi/game/cfg-mugen/)
- [CFG - Tệp cấu hình công cụ nguồn](/vi/game/cfg-sourceengine/)

**Hệ thống & Linh tinh**
- [Tệp CFG - CFG](/vi/system/cfg/)
- [CFG - Tệp cấu hình mô hình Cal3D](/vi/misc/cfg-cal3d/)

## Người giới thiệu
* [Celestia](https://en.wikipedia.org/wiki/Celestia)

