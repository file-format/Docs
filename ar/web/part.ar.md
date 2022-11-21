{
  "date" : "2021-06-24",
  "keywords" :["جزء" , "جزئي" , "امتداد" , "ملف" , "تنسيق" , "ويب" , "تم التنزيل"] ,
  "author" : {
    "display_name" : "Sami Cheema"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"الجزء - الملف الذي تم تنزيله جزئيًا" ,
  "description":"تعرف على تنسيق ملف PART وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات PART وفتحها." ,
  "linktitle" : "PART",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2021-06-24"
}

## ما هو ملف PART؟ ##

ملف جزء أو ملحق. جزء هو ملف تم تنزيله جزئيًا. يتم استخدامه عندما تكون التنزيلات قيد التقدم أو تمت مقاطعتها بسبب أي مشكلة ، مما يمنح مدير التنزيل فرصة لاستئناف التنزيل كلما أمكن ذلك.
هذا يعني أن المستعرض ، مثل Firefox أو برامج نقل الملفات مثل eMule و eMule plus و FlashGet وما إلى ذلك ، يخزن جزءًا من الملف ، يسمى Part file ، أثناء التنزيل على جهازك. سيوضح لك ملف الجزء هذا ما إذا كان التنزيل قيد التقدم أو تمت مقاطعته قبل اكتماله. ليس هذا فقط ولكن ملف PART يخزن جميع البيانات حتى يكتمل التنزيل وهذا هو السبب في إمكانية استئناف بعضها لاحقًا إذا كنت تريد بدء التنزيل مرة أخرى.

## تنسيق ملف الجزء ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
