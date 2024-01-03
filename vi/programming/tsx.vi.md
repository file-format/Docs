{
  "date" : "2023-12-28",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Tệp TSX - Tệp React TypeScript - Tệp .tsx là gì và cách mở tệp?",
  "description":"Tìm hiểu về file TSX React TypeScript và cách mở file.",
  "linktitle" : "TSX",
  "menu" : {
    "docs" : {
      "identifier": "programming-vi-tsx",
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-12-28"
}

## Tệp TSX là gì?

Phần mở rộng tệp ".tsx" thường được liên kết với các tệp TypeScript có chứa mã **React**. **TypeScript là siêu bộ JavaScript** bổ sung kiểu gõ tĩnh vào ngôn ngữ và **React là thư viện JavaScript để xây dựng giao diện người dùng**. Khi làm việc với React và TypeScript cùng nhau, các nhà phát triển thường sử dụng phần mở rộng ".tsx" cho các tệp của họ để cho biết rằng chúng chứa cả TypeScript và JSX (phần mở rộng cú pháp của React dành cho JavaScript).

## Ví dụ về tệp TSX

TypeScript cho phép bạn xác định loại cho các biến, tham số hàm và hơn thế nữa. Bạn sẽ thường thấy mã TypeScript trong tệp ".tsx" chỉ định các loại đạo cụ, trạng thái và các biến khác được sử dụng trong các thành phần React.

```
// Ví dụ: Mã TypeScript trong thành phần React
giao diện MyComponentProps {
   tên: chuỗi;
   tuổi: số lượng;
}
const MyComponent: React.FC<MyComponentProps> = ({ name, age }) => {
   // Logic thành phần ở đây
   return <div>{name} đã {age} tuổi.</div>;
};
```

## JSX (Phần mở rộng cú pháp phản ứng)

JSX là một phần mở rộng cú pháp cho JavaScript được React khuyên dùng. Nó trông giống như XML/HTML và được sử dụng để mô tả giao diện người dùng sẽ trông như thế nào.

```
// Ví dụ: JSX trong thành phần React
const MyComponent: React.FC<MyComponentProps> = ({ name, age }) => {
   return <div>{name} đã {age} tuổi.</div>;
};
```

Tệp ".tsx" thường chứa định nghĩa của thành phần React bằng cách sử dụng các thành phần chức năng hoặc thành phần lớp.

```
// Ví dụ: Định nghĩa thành phần React trong file ".tsx"
const MyComponent: React.FC = () => {
   return <div>Xin chào, React!</div>;
};
```

Bạn sẽ thường thấy các câu lệnh nhập ở đầu tệp, chứa các phần phụ thuộc và mô-đun cần thiết.

```
// Ví dụ: Nhập câu lệnh vào file ".tsx"
nhập React từ 'Reac';
```

## Làm cách nào để mở tệp TSX?

Tệp TSX là tệp văn bản thuần túy nên bạn có thể mở chúng trong bất kỳ trình soạn thảo văn bản nào, ví dụ: Sổ tay. Tuy nhiên, đây là các tệp mã hóa và được mở bằng IDE, ví dụ: Mã Visual Studio.