{
  "date" : "2021-04-20",
  "keywords": [ "JSPF file", "jspf", "JSPF example", "extension", "format", "jspf tutorial", "jsp fragment", "JSPF file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSPF - JSP Parça Dosya Biçimi",
  "description":"JSPF dosya formatı ve JSPF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "JSPF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-21"
}

## JSPF dosyası nedir?
.jspf uzantılı dosyaya JSP fragmanı denir; başka bir JSP dosyasında bulunan statik bir dosya. JSPF dosyaları kendi başlarına derlenmezler, ancak içerdikleri sayfa boyunca derlenirler. Sözdizimi, Java Sunucu Sayfaları (JSP) koduna benzer. Sadece bir JSP parçası içerir; tüm JSP belgesini içermez.

## JSPF dosya formatı
JSP 2.0 Spesifikasyonunda "JSP fragmanı" terimi aşırı yüklendiğinden bunun yerine "JSP segmenti" terimi kullanılmaktadır. JSP parçaları, .jsp veya .jspf uzantılarını kullanabilir ve **/WEB-INF/jspf** içine veya diğer statik dosyalara yerleştirilmelidir. Tam sayfa olmayan JSP parçaları .jspf uzantısını kullanmalı ve **/WEB-INF/jspf** içine yerleştirilmelidir.

### JSP veya JSP Fragment Dosya Organizasyonu
Bir JSP dosyası, listelendikleri sırayla aşağıdaki bölümleri içerir:

1. Yorumları açma
2. JSP sayfası direktif(ler)i
3. İsteğe bağlı etiket kitaplığı direktif(ler)i
4. İsteğe bağlı JSP bildirim(ler)i
5. HTML ve JSP kodu

Bir JSP veya JSPF dosyasının her ikisi de, **Açılış Yorumu** olarak adlandırılan, sunucu tarafı tarzı bir yorumla başlar:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Bu yorum, JSP sayfası oluşturma sırasında kaldırıldığı için yalnızca sunucu tarafında görülebilir.

## JSP Fragment dosyası ne zaman kullanılır?
Bir JSP sayfası, diğer JSP sayfalarında da yeniden kullanılabilen belirli ama karmaşık bir yapı gerektirdiğinde, bunu halletmenin bir yolu, Bileşik Görünüm modelini (Java Taslaklarının Desenler bölümü) kullanarak onu parçalara ayırmaktır. Örneğin, bir JSP sayfasının sunum yapısında bazen aşağıdaki mantıksal düzen bulunur:

{{< figure src="../jspf.png" alt="JSPF Dosya Biçimi" >}}

Bu durumda, bu bileşik JSP sayfası, her biri ayrı bir JSP parçası olarak adlandırılacak olan çeşitli modüllere dönüştürülebilir. JSP parçaları daha sonra bileşik JSP sayfasında uygun konumlara yerleştirilebilir. Bu nedenle, statik içerme yönergeleri kendi kendine çağrılmayacak bir sayfayı dahil etmek için kullanıldığında JSPF dosyası kullanılır, .jspf uzantılı dosyalar Web uygulama arşivinin /WEB-INF/jspf/ dizinine yerleştirilmelidir ( savaş).

## JSPF Örneği
```
<%@ include file="/WEB-INF/jspf/header.jspf" %>
...
<%@ include file="/WEB-INF/jspf/menuBar.jspf" %>
...
<jsp:include page="<%= currentBody %>" />
...
<%@ include file="/WEB-INF/jspf/footnote.jspf" %>
...
<%@ include file="/WEB-INF/jspf/footer.jspf" %>
...
```

## Referanslar

* [Java Sunucu Sayfaları için Kod Kuralları](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

