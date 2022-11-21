{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XFDF Dosya Formatı - XFDF dosyası nedir?",
  "description":"XFDF dosyası ve XFDF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## XFDF dosyası nedir?

.xfdf uzantılı bir dosya, Adobe Acrobat yazılımı ile oluşturulan bir XML Form Veri Biçimidir. [FDF](/tr/pdf/fdf/) gibi, XFDF de form öğeleri açıklamasını ve bunların değerlerini XML biçiminde içerir. Bu, PDF formundaki metin alanlarının adlarını ve değerlerini içerebilir. XFDF, insanlar tarafından okunabilir biçimde kaydedilir ve C# gibi programlama dilleri kullanılarak programlı olarak okunabilir.

## XFDF Dosya Biçimi - Daha Fazla Bilgi

XFDF dosyaları, verilerin içe ve dışa aktarılması için kullanılan evrensel bir biçim olan XML dosya biçiminde kaydedilir. Bir XFDF dosya yapısı, aşağıda gösterildiği gibi bir başlık, ardından alan değerleri ve öğe verilerinden oluşur.

|Öğe|Öznitelik|İçerik|
---|---|---|
|\<XFDF> ||En üstteki öğe|
|\<fields> ||Bu şablon için tüm alan değerleri|
|<field (T)> |ad |Alan adı|
|<value (V)> |değer |Alan değeri|

## Referanslar

* [Acrobat'tan FDF Format Desteği](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for -acroforms.html)
* [Adobe Geliştirici Kaynakları](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

