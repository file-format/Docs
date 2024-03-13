{
  "date": "2022-01-23",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GDOC Faylı - Google Sənəd Qısayolu",
  "description": "GDOC faylının nə olduğu və GDOC fayllarını yarada və aça bilən API-lər haqqında öyrənin.",
  "linktitle": "GDOC",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-gdo-azc"
}
},
  "lastmod": "2022-01-23"
}

## GDOC faylı nədir?

GDOC faylı bulud əsaslı sənəd saxlama xidməti olan Google Diskdə yerləşən fayla işarə edən qısa yol faylıdır. Google Disk müştərisi kompüterdə quraşdırıldıqda və onun daxilində sənəd yaradıldıqda, disk onlayn bulud yaddaşında sənəd yaradır və bu sənədin [URL](/web/url/)-ni yerli Google Disk qovluğunda GDOC faylına yazır. Bu qısayol faylı iki dəfə kliklədikdə, standart veb brauzer sənədi [URL](/web/url/) yerindən açır. Bu qısayol faylı bu qovluqdan çıxarılarsa, onlayn sənədə keçid pozulur.

## GDOC Fayl Format - Ətraflı Məlumat

GDOC faylında [JSON](/web/json/) fayl formatında yazılmış onlayn sənədin qısa yolu var. GDOC fayllarını açan brauzer URL məlumatını oxuyur və istifadəçinin sənədin saxlandığı bu Google hesabına daxil olması şərti ilə əlaqəli sənədi nümayiş etdirmək üçün açır. GDOC fayllarında sənədin məzmunu yoxdur.

### GDOC fayl nümunəsi

GDOC faylı mətn redaktorunda açıla bilər və məzmunu aşağıdakı kimi görünür.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

Göründüyü kimi, məzmun sənədin URL-i və əlaqəli sənəd ID-si olan JSON-da formatlanır.

## İstinadlar

* [Google Docs not opening either gdoc or docx files](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=en)

