{
  "date" : "2021-06-24",
  "keywords" :["部分","部分","扩展","文件","格式","网络","下载"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"部分 - 部分下载的文件",
  "description":"了解 PART 文件格式和可以创建和打开 PART 文件的 API。",
  "linktitle" : "PART",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## 什么是零件文件？ ##

零件文件或 .part 扩展名是部分下载的文件。当下载正在进行或由于任何问题而中断时使用它，使下载管理器有机会尽可能恢复下载。
这意味着浏览器（例如 Firefox）或文件传输程序（例如 eMule、eMule plus、FlashGet 等）会在您的设备上进行下载时存储文件的一部分，称为 Part 文件。该部分文件将显示下载是否正在进行或在完成之前被中断。不仅如此，PART 文件还会存储所有数据，直到下载完成，这就是为什么如果您想再次开始下载，以后可以恢复其中的一些数据。

## 部分文件格式##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download" folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
