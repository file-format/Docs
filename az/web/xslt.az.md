{
  "date": "2021-01-20",
  "keywords": [
"xslt",
"Fayl",
"Uzatma",
"Fayl Format",
"Fayl uzadılması",
"Genişlənən Üslub Cədvəli Dili"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XSLT fayl formatı",
  "description": "XSLT faylları yarada və aça bilən XSLT fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "XSLT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xsl-azt"
}
},
  "lastmod": "2021-01-20"
}

## XSLT faylı nədir?

.xslt uzantısı olan fayl XSL təlimatlarından istifadə edərək XML faylını çevirmək və üslub etmək üçün istifadə edilən Genişlənən Üslub Cədvəli Dilinin Çevrilmə faylıdır. Bu format XML sənədlərini mətn sənədi və ya .html veb səhifəsi kimi standart çıxış formatlarına çevirmək üçün istifadə olunur. Bu transformasiya mövcud XML sənədinin məzmunu əsasında yeni sənəd yaradır. XSLT onu nəzəri cəhətdən ixtiyari hesablamalar edə bilir.

## XSLT fayl formatı

XLST fayl formatı istənilən mətn redaktorunda baxıla bilən düz mətn formatında transformasiya təlimatlarını ehtiva edir. Dilə üç dəfə düzəliş edilmişdir.

* `XSLT 1.0` - XSLT 1.0 1999-cu ilin noyabrında W3C tövsiyəsi kimi nəşr edilmişdir.

* `XSLT 2.0` - Bu, tarixləri, vaxtları və müddətləri manipulyasiya etmək üçün adi ifadələr, funksiyalar və operatorlardan istifadə edərək String manipulyasiyası, çoxsaylı çıxış sənədləri, qruplaşdırma və daha zəngin tip sistemi və güclü tip yoxlanışı kimi dəyişiklikləri ehtiva edir.

* `XSLT 3.0` - O, 8 iyun 2017-ci ildə W3C Tövsiyəsinin bir hissəsi oldu və əsas yeni xüsusiyyətlər arasında axın transformasiyası, böyük üslub cədvəllərinin modulluğunu təkmilləşdirmək üçün paketlər, məsələn, xsl:try təlimatı ilə dinamik xətaların təkmilləşdirilmiş idarə edilməsi daxildir. və XSLT-yə XML kimi JSON-u idarə etməyə imkan verən xəritələr və massivlər üçün dəstək.


### XSLT Nümunəsi

Aşağıdakı nümunə [w3schools](https://www.w3schools.com/xml/xsl_intro.asp) saytından götürülüb.
```
<?xml version="1.0"?>

<xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">

<xsl:template match="/">
  <html>
  <body>
    <h2>My CD Collection</h2>
    <table border="1">
      <tr bgcolor="#9acd32">
        <th>Title</th>
        <th>Artist</th>
      </tr>
      <xsl:for-each select="catalog/cd">
        <tr>
          <td><xsl:value-of select="title"/></td>
          <td><xsl:value-of select="artist"/></td>
        </tr>
      </xsl:for-each>
    </table>
  </body>
  </html>
</xsl:template>

</xsl:stylesheet>
```
## İstinadlar ##

* [XSLT - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/XSLT)

* [XSLT Elementləri](https://en.wikipedia.org/wiki/XSLT_elements)


