{
  "date": "2022-12-07",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ไฟล์ DT0 - รูปแบบไฟล์ DTED ระดับ 0",
  "description": "เรียนรู้เกี่ยวกับรูปแบบไฟล์ DT0 และ API ที่สามารถสร้างและเปิดไฟล์ DT0",
  "linktitle": "DT0",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-dt-th0"
}
},
  "lastmod": "2022-12-07"
}

## ไฟล์ DT0 คืออะไร??

ไฟล์ DT0 เป็นไฟล์ Digital Terrain Elevation Data (DTED) ที่มีข้อมูลระดับ 0 เพื่อศึกษาข้อมูลระดับความสูงของภูมิประเทศ ข้อมูลระดับความสูงจะมีระยะห่างเท่ากันในไฟล์ DT0 และสามารถอ่านได้โดยโปรแกรม GIS ยอดนิยม เช่น ESRI ArcGIS Pro, TatukGIS, Blue Marble Geographic Global Mapper และ Pitney Bowes MapInfo ไฟล์ DT0 ส่วนใหญ่จะใช้โดยชุมชนวิทยาศาสตร์และเทคนิคเพื่อศึกษาความลาดชัน ระดับความสูง และความขรุขระของพื้นผิวของภูมิประเทศทั่วโลก

รูปแบบไฟล์ DT0 คล้ายกับประเภทไฟล์ [DT1](/gis/dt1/) และ [DT2](/gis/dt2/) แต่มีรายละเอียดน้อยกว่า

### รูปแบบไฟล์ DT0

ไฟล์ DT0 จะถูกบันทึกเป็นไฟล์ไบนารีลงแผ่นดิสก์ สิ่งเหล่านี้สามารถอ่านได้โดยใช้แอปพลิเคชัน GIS มากมาย ไฟล์ DT0 สามารถรวมเข้ากับ File Geodatabase Raster Catalog ที่สามารถใช้สร้างภาพโมเสคขนาดใหญ่ได้

## วิธีแปลงไฟล์แรสเตอร์เป็น DTED

มีเครื่องมือหลายอย่างที่สามารถแปลงไฟล์ Raster เป็น DTED ได้ [ArgGIS Pro](https://pro.arcgis.com/en/pro-app/latest/tool-reference/data-management/raster-to-dted.htm) เป็นหนึ่งในเครื่องมือที่สามารถแปลง Raster เป็น DTED ได้

## อ้างอิง

 * [ArgGIS Pro](https://pro.arcgis.com/en/pro-app/latest/tool-reference/data-management/raster-to-dted.htm)
 * [รูปแบบไฟล์ KML](/gis/kml/)

