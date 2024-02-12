{
  "date" : "2024-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "File CUBE - File khối Gaussian - File .cube là gì và làm cách nào để mở nó?",
  "description" : "Tìm hiểu về Gaussian Cube File và cách mở nó.",
  "linktitle" : "CUBE",
  "menu" : {
    "docs" : {
      "identifier" : "data-vi-cube",
      "parent" : "data"
    }
  },
  "lastmod" : "2024-01-25"
}

## Tệp CUBE là gì?

Định dạng tệp CUBE, còn được gọi là tệp Gaussian Cube (.cube) được sử dụng trong hóa học tính toán để lưu trữ dữ liệu phân tử, đặc biệt là thông tin mật độ electron thu được từ các tính toán hóa học lượng tử. Định dạng này thường được liên kết với **gói phần mềm Gaussian**, được sử dụng rộng rãi để thực hiện các phép tính cấu trúc điện tử ban đầu.

Tệp Gaussian Cube lưu trữ dữ liệu ba chiều, thường biểu thị mật độ electron hoặc các tính chất khác của phân tử, thu được thông qua tính toán hóa học lượng tử. Tệp chứa phần tiêu đề có siêu dữ liệu (chẳng hạn như nguồn gốc, số điểm dữ liệu dọc theo mỗi trục và khoảng cách), theo sau là lưới các giá trị số biểu thị thuộc tính quan tâm (ví dụ: mật độ electron) tại mỗi điểm lưới trong không gian.

Tệp Gaussian Cube (.cube) là tệp văn bản thuần túy có cấu trúc cụ thể. Tiêu đề chứa thông tin về hệ thống phân tử và lưới dữ liệu, đồng thời các giá trị dữ liệu được sắp xếp theo định dạng lưới ba chiều. Các tệp Gaussian Cube thường được sử dụng để trực quan hóa các đặc tính phân tử bằng phần mềm trực quan hóa phân tử. Các chương trình như **VMD (Động lực học phân tử trực quan)** hoặc **PyMOL** có thể đọc các tệp Khối Gaussian để hiển thị bề mặt phân tử, mật độ electron hoặc các thuộc tính được tính toán khác.

## Ví dụ đơn giản về file Gaussian Cube:

```
Ví dụ về tệp khối
Được tạo bởi Gaussian
   0 1 0 0 0 0 0 0 0
   0,0000000000000000E+00 0,00000000000000000E+00 0,0000000000000000E+00
  50 0,10000000000000000E+01 0,0000000000000000E+00 0,00000000000000000E+00
  50 0,00000000000000000E+00 0,1000000000000000E+01 0,00000000000000000E+00
  50 0,00000000000000000E+00 0,0000000000000000E+00 0,10000000000000000E+01
    0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02
    ... (giá trị dữ liệu về mật độ electron tại mỗi điểm lưới)
```

## Giới thiệu về Gaussian

Gaussian là một bộ ứng dụng phần mềm cho hóa học lượng tử và hóa học tính toán. Trọng tâm chính của Gaussian là các phương pháp hóa học lượng tử ab initio, là các phương pháp tiếp cận có độ chính xác cao nhưng tính toán chuyên sâu để nghiên cứu cấu trúc điện tử của các phân tử. Phần mềm này được sử dụng rộng rãi trong môi trường nghiên cứu và học thuật cho nhiều ứng dụng khác nhau, bao gồm dự đoán tính chất phân tử, nghiên cứu cơ chế phản ứng và khám phá cấu trúc phân tử.

##Giới thiệu về NWChem

NWChem là một phần mềm hóa học tính toán mã nguồn mở được thiết kế để mô phỏng hóa học lượng tử hiệu suất cao. Nó sử dụng các phương pháp ban đầu như Hartree-Fock và lý thuyết hàm mật độ, hỗ trợ tính toán song song để tính toán hiệu quả trên các cụm và tìm thấy các ứng dụng trong các lĩnh vực khoa học đa dạng, bao gồm hóa học tính toán, hóa sinh và khoa học vật liệu. NWChem được biết đến với tính linh hoạt, cho phép các nhà nghiên cứu nghiên cứu các hệ thống hóa học khác nhau và tính chất nguồn mở của nó khuyến khích sự đóng góp và tùy chỉnh của cộng đồng.

##Giới thiệu về VMD

VMD, viết tắt của Visual Molecular Dynamics, là chương trình trực quan hóa phân tử mạnh mẽ và được sử dụng rộng rãi để hiển thị, phân tích và tạo hoạt ảnh cho các quỹ đạo động lực phân tử (MD), cũng như các cấu trúc phân tử tĩnh. Nó đặc biệt phổ biến trong các lĩnh vực hóa học tính toán, sinh học phân tử và tin sinh học cấu trúc. VMD vượt trội trong việc trực quan hóa các cấu trúc phân tử, cung cấp kết xuất 3D chất lượng cao của các phân tử và phức hợp phân tử. Nó hỗ trợ nhiều định dạng tập tin phân tử.

## Giới thiệu về PyMOL

PyMOL là một hệ thống trực quan hóa phân tử và công cụ phần mềm được sử dụng để hiển thị ba chiều các cấu trúc phân tử. Nó đặc biệt phổ biến trong các lĩnh vực sinh học cấu trúc, tin sinh học và hóa học tính toán. PyMOL cung cấp kết xuất 3D chất lượng cao về cấu trúc phân tử, cho phép người dùng trực quan hóa và khám phá hình dạng, bề mặt và tương tác của các đại phân tử sinh học.

## Làm cách nào để mở tệp CUBE?

Tệp CUBE có thể được mở và tham chiếu bằng các chương trình sau.

- **NWChem** (Miễn phí) cho (Windows, MAC, Linux)

## Người giới thiệu
* [Định dạng tệp khối Gaussian](https://paulbourke.net/dataformats/cube/)
