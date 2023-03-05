{
  "date" : "2022-01-04",
  "keywords" :[ ".dst", "файл", "формат", "расширение", "API", "подшивка AutoCAD" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DST — файл подшивки AutoCAD",
  "description" :"Узнайте о файле .dst и API, которые могут создавать и открывать файлы DST.",
  "linktitle" : "DST",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2022-01-04"
}

## .DST вариант №

Файл DST — это файл AutoCAD, который содержит ассоциации и информацию для определения наборов листов. Они хранятся в папке хранения подшивки по умолчанию, AutoCAD Sheets Sets. Файлы DST не содержат фактических компоновок чертежей, но ссылаются на них из выбранных файлов [DWG](/ru/cad/dwg/) и [DWT](/ru/cad/dwt/), связанных с этими подшивками. В сетевой среде все члены команды должны иметь сетевой доступ к этим связанным файлам. Файлы DST сохраняются на диск в формате [XML](/ru/web/xml/).

## Формат файла DST — дополнительная информация

Файлы DST создаются с помощью инструмента AutoDesk Sheet Set Manager (SSM). Когда кто-то из команды обращается к файлу, файл DST открывается на короткое время, а затем сохраняется с обновленной информацией. Одновременный доступ к одному и тому же файлу DST управляется инструментом SSM, который показывает значок блокировки, когда файл находится в доступе.

В любой конкретный момент статус листа может находиться в одном из следующих состояний.

* Лист доступен для редактирования.
* Лист заблокирован.
* Лист отсутствует или находится в неожиданном месте папки.

## использованная литература

* [Об использовании наборов листов DST](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2017/ENU/AutoCAD-LT/files/GUID-577D8EA0-85F2 -4829-B4F9-8CAD6F7AAACC-htm.html)
* [Подробнее о наборах листов](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2017/ENU/AutoCAD-LT/files/GUID-34D889BC-19AD- 4CD1-ADB1-F359D9B515FB-htm.html)
* [Освоение наборов листов AutoCAD](https://damassets.autodesk.net/content/dam/autodesk/www/cad-manager-center/articles/Mastering-AutoCAD-Sheet-Sets_Preview_EN.pdf)

