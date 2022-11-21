{
  "date" : "2021-01-20",
  "keywords" :["xslt", "Dosya", "Uzantı", "Dosya Formatı", "Dosya Uzantısı", "Genişletilebilir Stil Sayfası Dili"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLT Dosya Biçimi",
  "description":"XSLT dosya formatı ve XSLT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-01-20"
}

## XSLT dosyası nedir?

.xslt uzantılı bir dosya, XSL talimatlarını kullanarak bir XML dosyasını dönüştürmek ve biçimlendirmek için kullanılan bir Genişletilebilir Stil Sayfası Dil Dönüşümü dosyasıdır. Biçim, XML belgelerini metin belgesi veya .html web sayfası gibi standart çıktı biçimlerine dönüştürmek için kullanılır. Bu dönüşüm, mevcut XML belgesinin içeriğine dayalı olarak yeni bir belge oluşturur. XSLT, onu teorik olarak isteğe bağlı hesaplamalar yapabilir hale getiriyor.

## XSLT Dosya Biçimi

XLST dosya biçimi, herhangi bir metin düzenleyicide görüntülenebilen düz metin biçimindeki dönüştürme talimatlarını içerir. Dilde üç revizyon yapılmıştır.

* `XSLT 1.0` - XSLT 1.0, Kasım 1999'da bir W3C tavsiyesi olarak yayınlandı.
* `XSLT 2.0` - Tarihleri, saatleri ve süreleri işlemek için düzenli ifadeler, işlevler ve işleçler, çoklu çıktı belgeleri, gruplama ve daha zengin bir yazı sistemi ve güçlü tip denetimi kullanarak Dize manipülasyonu gibi değişiklikleri içerir.
* `XSLT 3.0` - 8 Haziran 2017'de W3C Tavsiyesinin bir parçası haline geldi ve ana yeni özellikler arasında akış dönüştürme, büyük stil sayfalarının modülerliğini geliştirmeye yönelik Paketler, örneğin bir xsl:try talimatıyla dinamik hataların daha iyi işlenmesi, ve haritalar ve diziler için destek, XSLT'nin XML'in yanı sıra JSON'u işlemesini sağlar.

### XSLT Örneği

Aşağıdaki örnek [w3schools](https://www.w3schools.com/xml/xsl_intro.asp) sitesinden alınmıştır.
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
## Referanslar ##

* [XSLT - Wikipedia Tarafından](https://en.wikipedia.org/wiki/XSLT)
* [XSLT Öğeleri](https://en.wikipedia.org/wiki/XSLT_elements)

