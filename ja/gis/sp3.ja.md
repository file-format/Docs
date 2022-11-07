{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SP3 - NGS SP3 ファイル",
  "description":"SP3 ファイル形式と,SP3 ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "SP3",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## SP3 ファイルとは何ですか?

拡張子が .sp3 のファイルは、軌道情報を格納するための National Geodetic Survey (NGS) 軌道形式です。これは、NGS の SP1 および SP2 形式の拡張であり、軌道と同時に計算される衛星クロック補正情報が含まれています。主に位置とクロックに基づいており、速度は含まれていません。この形式は 1989 年の Remondi で提案され、1991 年に採用されました。衛星時計の補正情報に加えて、軌道精度指数、コメント行、GPS 週、および最初のエポックに関連付けられた週の秒数などの情報が含まれます。 SP3 ファイルは、Wolfram Research Mathematica で開くことができます。

## SP3 ファイル形式 - 詳細情報

SP3 ファイルは ASCII ファイル形式でディスクに保存され、その内容は任意のテキスト エディタで開いて表示できます。 SP3 ファイルの構造は、次の図で確認できます。

{{< figure src="../sp3-file-format.png" title="" >}}

## 参考文献

* [拡張標準プロダクト 3 軌道フォーマット (SP3-c)](http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20similar ,a%20more%20flexible%20header%20structure)
* [National Geodetic Survey Standard GPS Orbit Formats の拡張](https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)

