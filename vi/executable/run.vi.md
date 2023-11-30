{
  "date" : "2023-01-31",
  "keywords" :["tệp chạy", "tệp đang chạy là gì", "tệp", "cách mở tệp đang chạy", "phần mở rộng của tệp chạy","tiện ích mở rộng"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp RUN và các API có thể tạo và mở tệp RUN.",
  "title" :"Định dạng tệp RUN - Tệp thực thi Linux",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## Tập tin RUN là gì?

Định dạng tệp .run thường được sử dụng để phân phối phần mềm hoặc trình cài đặt ứng dụng trong môi trường Linux. Để cài đặt phần mềm, bạn sẽ cần làm cho tệp có thể thực thi được, việc này có thể được thực hiện bằng lệnh sau:

```bash
chmod +x file_name.run 
```

Sau đó, bạn có thể chạy tệp bằng lệnh sau:

```bash
./file_name.run 
```

Quá trình cài đặt có thể khác nhau tùy thuộc vào tệp và chương trình cụ thể mà bạn đang cố cài đặt.

Định dạng tệp .run là một loại tập lệnh shell được sử dụng để phân phối trình cài đặt phần mềm hoặc ứng dụng trong môi trường Linux. Đây là gói độc lập bao gồm mọi thứ cần thiết để cài đặt phần mềm, bao gồm tệp nhị phân, thư viện và tệp cấu hình.

Điều quan trọng cần lưu ý là các tệp .run cũng có thể chứa mã độc, vì vậy, bạn nên xác minh nguồn của tệp và quét vi-rút trước khi chạy.

Ngoài ra, một số tệp .run có thể yêu cầu quyền root để chạy và cài đặt, vì vậy bạn có thể cần sử dụng lệnh "sudo" để chạy tệp có quyền nâng cao:

```bash
sudo ./filename.run
```

## Làm cách nào để mở tệp RUN?

Để mở tệp .run, bạn cần làm cho nó có thể thực thi được bằng lệnh "chmod":

```bash
chmod +x filename.run 
```

Khi tệp được thực thi, bạn có thể chạy tệp bằng cách gõ:

```bash
./filename.run
```

Chạy tệp .run không giống như mở tệp đó trong trình soạn thảo văn bản. Chạy tệp .run sẽ thực thi các hướng dẫn của nó, có thể là bất cứ điều gì từ cài đặt chương trình đến chạy tập lệnh. Để xem nội dung của tệp .run, bạn cần mở tệp đó trong trình soạn thảo văn bản, chẳng hạn như nano hoặc vim:

```
nano filename.run
```
hoặc
```
vim filename.run
```

## Người giới thiệu
* [Cách thực thi tệp .bin và .run trong Ubuntu](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)


