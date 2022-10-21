{
  "date" : "2021-06-24",
  "keywords" :[ "PART", "partial", "extension", "file", "format", "web", "heruntergeladen" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PART - Teilweise heruntergeladene Datei",
  "description":"Erfahren Sie mehr über das PART-Dateiformat und APIs, die PART-Dateien erstellen und öffnen können.",
  "linktitle" :"TEIL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Was ist eine PART-Datei? ##

Eine Part-Datei oder .part-Erweiterung ist eine teilweise heruntergeladene Datei. Es wird verwendet, wenn Downloads im Gange sind oder aufgrund eines Problems unterbrochen wurden, und gibt dem Download-Manager die Möglichkeit, den Download wann immer möglich fortzusetzen.
Dies bedeutet, dass der Browser wie Firefox oder Dateiübertragungsprogramme wie eMule, eMule plus, FlashGet usw. einen Teil der Datei, die so genannte Teildatei, speichert, während der Download auf Ihrem Gerät stattfindet. Diese Teildatei zeigt Ihnen, ob der Download im Gange ist oder vor Abschluss unterbrochen wurde. Darüber hinaus speichert die PART-Datei alle Daten, bis der Download abgeschlossen ist, weshalb einige von ihnen später wieder aufgenommen werden können, wenn Sie den Download erneut starten möchten.

## PART-Dateiformat ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
