{
  "date" : "2021-06-24",
  "keywords" :[ "PART", "parcial", "extensão", "arquivo", "formato", "web", "baixado" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PART - Arquivo parcialmente baixado",
  "description":"Saiba mais sobre o formato de arquivo PART e APIs que podem criar e abrir arquivos PART.",
  "linktitle" : "PART",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## O que é um arquivo PART? ##

Um arquivo de parte ou extensão .part é um arquivo parcialmente baixado. É usado quando os downloads estão em andamento ou foram interrompidos devido a algum problema, dando ao gerenciador de downloads a oportunidade de retomar o download sempre que possível.
Isso significa que o navegador, como Firefox ou programas de transferência de arquivos como eMule, eMule plus, FlashGet, etc. armazena uma parte do arquivo, chamada Part file, enquanto o download está ocorrendo em seu dispositivo. Este arquivo de parte mostrará se o download está em andamento ou foi interrompido antes da conclusão. Não apenas isso, mas o arquivo PART armazena todos os dados até que o download seja concluído, e é por isso que alguns deles podem ser retomados posteriormente se você quiser iniciar o download novamente.

## Formato de arquivo PART ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
