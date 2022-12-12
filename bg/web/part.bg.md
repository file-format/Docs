{
  "date" : "2021-06-24",
  "keywords" :[ "ЧАСТ", "частично", "разширение", "файл", "формат", "уеб", "изтеглено"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ЧАСТ – частично изтеглен файл",
  "description":"Научете за PART файловия формат и API, които могат да създават и отварят PART файлове.",
  "linktitle" : "PART",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Какво е PART файл? ##

Частичен файл или разширение .part е частично изтеглен файл. Използва се, когато изтеглянията са в ход или са били прекъснати поради някакъв проблем, като дава възможност на мениджъра за изтегляне да възобнови изтеглянето, когато е възможно.
Това означава, че браузърът като Firefox или програмите за прехвърляне на файлове като eMule, eMule plus, FlashGet и т.н. съхраняват част от файла, наречена Part file, докато изтеглянето се извършва на вашето устройство. Този част от файла ще ви покаже дали изтеглянето е в ход или е било прекъснато преди завършване. Не само това, но и файлът PART съхранява всички данни, докато изтеглянето приключи, поради което някои от тях могат да бъдат възобновени по-късно, ако искате да започнете изтеглянето отново.

## PART файлов формат ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
