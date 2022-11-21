{
  "date" : "2021-06-24",
  "keywords" :[ "BÖLÜM", "kısmi", "uzantı", "dosya", "biçim", "web", "indirilen"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BÖLÜM - Kısmen İndirilen Dosya",
  "description":"PART dosya formatı ve PART dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "PART",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## PARÇA dosyası nedir? ##

Bir parça dosyası veya .part uzantısı kısmen indirilmiş bir dosyadır. İndirmeler devam ederken veya herhangi bir sorun nedeniyle kesintiye uğradığında kullanılır ve indirme yöneticisine mümkün olduğunda indirmeye devam etme fırsatı verir.
Bu, Firefox gibi tarayıcının veya eMule, eMule plus, FlashGet vb. dosya aktarım programlarının, cihazınızda indirme işlemi gerçekleşirken dosyanın Parça dosyası adı verilen bir bölümünü sakladığı anlamına gelir. Bu parça dosyası, indirme işleminin devam edip etmediğini veya tamamlanmadan önce kesintiye uğradığını size gösterecektir. Sadece bu değil, PART dosyası indirme tamamlanana kadar tüm verileri saklar, bu nedenle indirmeyi tekrar başlatmak isterseniz bazılarına daha sonra devam edilebilir.

## PARÇA Dosya Biçimi ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
