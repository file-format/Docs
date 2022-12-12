{
  "date" : "2021-06-24",
  "keywords" :[ "ЧАСТИНА", "частково", "розширення", "файл", "формат", "веб", "завантажено"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ЧАСТИНА - частково завантажений файл",
  "description":"Дізнайтеся про формат файлу PART та API, які можуть створювати та відкривати файли PART.",
  "linktitle" : "PART",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Що таке файл PART? ##

Файл частини або розширення .part – це частково завантажений файл. Він використовується, коли завантаження тривають або були перервані через будь-яку проблему, надаючи менеджеру завантажень можливість відновити завантаження, коли це можливо.
Це означає, що браузер, як-от Firefox, або програми передачі файлів, як-от eMule, eMule plus, FlashGet тощо, зберігають частину файлу, що називається Part-файл, під час завантаження на ваш пристрій. Цей файл частини покаже вам, чи триває завантаження або було перервано до завершення. Не тільки це, але й файл PART зберігає всі дані до завершення завантаження, тому деякі з них можна пізніше відновити, якщо ви захочете почати завантаження знову.

## PART Формат файлу ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
