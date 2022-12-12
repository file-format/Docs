{
  "date" : "2021-06-24",
  "keywords" :[ "PART", "partial", "extension", "file", "format", "web", "downloaded" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PART - Tệp được tải xuống một phần",
  "description":"Tìm hiểu về định dạng tệp PHẦN và các API có thể tạo và mở tệp PHẦN.",
  "linktitle" : "PART",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Tệp PHẦN là gì? ##

Tệp một phần hoặc phần mở rộng .part là tệp được tải xuống một phần. Nó được sử dụng khi quá trình tải xuống đang diễn ra hoặc bị gián đoạn do bất kỳ sự cố nào, tạo cơ hội cho trình quản lý tải xuống tiếp tục tải xuống bất cứ khi nào có thể.
Điều này có nghĩa là trình duyệt, chẳng hạn như Firefox hoặc các chương trình truyền tệp như eMule, eMule plus, FlashGet, v.v. lưu trữ một phần của tệp, được gọi là tệp Phần, trong khi quá trình tải xuống đang diễn ra trên thiết bị của bạn. Tệp phần này sẽ hiển thị cho bạn nếu quá trình tải xuống đang diễn ra hoặc đã bị gián đoạn trước khi hoàn tất. Không chỉ điều này mà tệp PHẦN lưu trữ tất cả dữ liệu cho đến khi quá trình tải xuống hoàn tất, đó là lý do tại sao một số dữ liệu sau đó có thể được tiếp tục nếu bạn muốn bắt đầu tải xuống lại.

## PHẦN Định dạng tệp ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
