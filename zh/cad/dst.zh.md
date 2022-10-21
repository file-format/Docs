{
  "date" : "2022-01-04",
  "keywords" :[".dst","文件","格式","扩展名","API","AutoCAD图纸集"],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DST - AutoCAD图纸集文件",
  "description" :"了解 .dst 文件和可以创建和打开 DST 文件的 API。",
  "linktitle" : "DST",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2022-01-04"
}

## 什么是一 .dst 文件？

DST 文件是一个 AutoCAD 文件，其中包含用于定义图纸集的关联和信息。它们存储在默认图纸集存储文件夹 AutoCAD 图纸集中。 DST 文件不包含实际的图纸布局，但从与这些图纸集关联的选定 [DWG](/zh/cad/dwg/) 和 [DWT](/zh/cad/dwt/) 文件中引用这些布局。在网络环境中，所有团队成员都应具有对这些关联文件的网络访问权限。 DST 文件以 [XML](/zh/web/xml/) 文件格式保存到光盘。

## DST 文件格式 - 更多信息

DST 文件是使用 AutoDesk Sheet Set Manager (SSM) 工具创建的。当团队中的某个人访问文件时，会短暂打开 DST 文件，然后将更新的信息一起存储回来。对同一 DST 文件的同时访问由 SSM 工具管理，该工具在文件处于访问状态时会显示一个锁定图标。

在任何特定时间，工作表状态可以处于以下任何一种状态。

* 该工作表可用于编辑。
* 工作表已锁定。
* 工作表丢失或位于意外的文件夹位置。

## 参考

* [关于使用 DST 图纸集](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2017/ENU/AutoCAD-LT/files/GUID-577D8EA0-85F2 -4829-B4F9-8CAD6F7AAACC-htm.html)
* [了解图纸集](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2017/ENU/AutoCAD-LT/files/GUID-34D889BC-19AD- 4CD1-ADB1-F359D9B515FB-htm.html)
* [掌握 AutoCAD 图纸集](https://damassets.autodesk.net/content/dam/autodesk/www/cad-manager-center/articles/Mastering-AutoCAD-Sheet-Sets_Preview_EN.pdf)

