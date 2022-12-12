{
  "date" : "2021-06-24",
  "keywords" :[ "RÉSZ", "részleges", "kiterjesztés", "fájl", "formátum", "web", "letöltve" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RÉSZ - Részben letöltött fájl",
  "description":"További információ a PART fájlformátumról és az API-król, amelyek PART fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "PART",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Mi az a PART fájl? ##

A részfájl vagy a .part kiterjesztésű fájl részben letöltött fájl. Akkor használatos, ha a letöltés folyamatban van, vagy bármilyen probléma miatt megszakadt, így a letöltéskezelőnek lehetősége nyílik a letöltés folytatására, amikor csak lehetséges.
Ez azt jelenti, hogy a böngésző, például a Firefox vagy az olyan fájlátviteli programok, mint az eMule, eMule plus, FlashGet stb., tárolja a fájl egy részét, az úgynevezett Part file-t, miközben a letöltés az eszközén történik. Ez a részfájl megmutatja, hogy a letöltés folyamatban van-e, vagy a befejezés előtt megszakadt-e. Nem csak ez, hanem a PART fájl is tárolja az összes adatot a letöltés befejezéséig, ezért ezek egy része később folytatható, ha újra akarja indítani a letöltést.

## PART Fájlformátum ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
