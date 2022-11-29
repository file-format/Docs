{
  "date" : "2021-06-24",
  "keywords" :[ "DEL", "partiell", "tillägg", "fil", "format", "webb", "nedladdat" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEL - Delvis nedladdad fil",
  "description":"Läs mer om PART-filformat och API:er som kan skapa och öppna PART-filer.",
  "linktitle" : "PART",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Vad är en PART fil? ##

En delfil eller .part-tillägg är en delvis nedladdad fil. Den används när nedladdningar pågår eller har avbrutits på grund av något problem, vilket ger nedladdningshanteraren en möjlighet att återuppta nedladdningen när det är möjligt.
Detta innebär att webbläsaren, som Firefox eller filöverföringsprogram som eMule, eMule plus, FlashGet, etc. lagrar en del av filen, kallad Part file, medan nedladdningen sker på din enhet. Denna delfil kommer att visa dig om nedladdningen pågår eller har avbrutits innan den är klar. Inte bara detta utan PART-filen lagrar all data tills nedladdningen är klar, varför vissa av dem senare kan återupptas om du vill starta nedladdningen igen.

## PART Filformat ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
