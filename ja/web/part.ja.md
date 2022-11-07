{
  "date" : "2021-06-24",
  "keywords" :["部分","部分","拡張子","ファイル","フォーマット","ウェブ","ダウンロード済み"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PART - 部分的にダウンロードされたファイル",
  "description":"PART ファイル形式と,PART ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "PART",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## .PART ファイルとは何ですか? ##

パーツ ファイルまたは .part 拡張子は、部分的にダウンロードされたファイルです。これは、ダウンロードが進行中または何らかの問題で中断されたときに使用され、ダウンロード マネージャーが可能な限りダウンロードを再開できるようにします。
これは、Firefox などのブラウザや、eMule、eMule plus、FlashGet などのファイル転送プログラムが、デバイスでダウンロードが行われている間、Part ファイルと呼ばれるファイルの一部を保存することを意味します。このパーツ ファイルは、ダウンロードが進行中か、完了前に中断されたかを示します。これだけでなく、ダウンロードが完了するまで PART ファイルにすべてのデータが保存されるため、ダウンロードを再開したい場合に一部のデータを後で再開できます。

## PART ファイル形式 ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
