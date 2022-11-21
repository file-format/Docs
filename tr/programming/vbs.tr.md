{
  "date" : "2021-08-24", 
  "keywords" :[ "vbs", "file", "extension", "file format", "Visual Basic Script", "Programlama Kılavuzu", "vbs örneği", "Microsoft Visual Basic", "VBScript"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBS - Visual Basic Komut Dosyası",
  "description":"VBS dosya formatı ve VBS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-24"
}

## VBS dosyası nedir?

VBS veya VBScript, Microsoft Visual Basic'in betik sürümüyle bağlantılıdır. Bilgi işlem ortamında, kullanıcının birçok yönüne erişmesine ve kontrol etmesine izin verilir. VBScript'in, ortamın öğelerini ve araçlarını kullanmak için **Bileşen Nesne Modeli** adlı bir model kullanmasına izin verilir. Bu ortam, VBScript'in çalışması ve çalıştırılması için belirtilmiştir.

Web geliştirme alanında müşteri tarafından erişildiğinde Javascript'e benzer şekilde hizmet vermektedir. Ayrıca sunucular tarafından web sayfalarının işlenmesi için kullanılır. [HTML](/tr/web/html/) uygulamaları gibi diğer bazı betik dosyası türlerinde düşünülebilir.


## Kısa Tarih ##

İlk olarak 1996 yılında, Microsoft tarafından Windows Komut Dosyaları için belirtilen teknolojilerin bir parçası olarak piyasaya sürüldü. Başlangıçta Web geliştiricilerinin yardımı için özel olarak geliştirilmiştir. Aynı yıl, Visual Basic Script'in özellikleriyle birlikte Microsoft Windows'un Internet Explorer adlı gezgini piyasaya sürüldü.

Teknoloji ve web geliştirmedeki ilerlemeyle birlikte, birçok gelişmiş özellik ile birlikte VBScript'in birçok sürümü piyasaya sürüldü. Üstelik önümüzdeki yıl bu betik dili yeni özelliklerle Microsoft Windows'un bir parçası olacak.

## Teknik Şartname ##

Sunucu tarafındaki web sayfaları için VBScript ile birlikte **Aktif Sunucu Sayfaları** gibi araçlar kullanılır. Bu betik dili, Windows'un betik bileşeninde de kullanılabilir. Bu dilin dosyaları Windows'ta bir .vbs uzantısıyla depolanır.

Bu dilin kodunda kullanılan döngüler gibi birçok kontrol yapısı vardır. Ayrıca, komut satırı olan ve adlandırılmış veya adlandırılmamış olabilen bağımsız değişkenleri de içerir. Bu dilin dosyaları, bir Windows işletim sisteminin klasörlerinde veya masaüstünde kolayca saklanabilir. Microsoft Script Editor gibi VBScript programları için belirli bir entegre geliştirme ortamı olmamasına rağmen, bu dilin geliştirilmesine olanak sağlar.

VBScript, Windows'un Script ana bilgisayarı tarafından barındırıldığında, komut dosyası dillerinde oldukça yaygın olan ancak Visual Basic 6.0'da bulunmayan çeşitli özellikler sağlar. Kolay veya doğrudan erişim içeren özellikler arasında Ağ Yazıcıları, adsız ve adlandırılmış komut satırı bağımsız değişkenleri, stdout ve stdin, Ağ Paylaşımları, Windows Yönetim Araçları, grup üyeliği gibi ağların kullanıcı bilgileri ve çok daha fazlası yer alır.

## VBS Dosya Biçimi Örneği ##

```
<% Option Explicit %>
 <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
 <html>
 	<head>
 		<title>VBScript Example</title>
 	</head>
 	<body>
 		<div><% 
 			' Grab current time from Now() function.
 			' An '=' sign occurring after a context switch (<%) is shorthand 
 			' for a call to the Write() method of the Response object.
 			Dim timeValue : timeValue = Now %>
 			The time, in 24-hour format, is 
 			<%=Hour(timeValue)%>:<%=Minute(timeValue)%>:<%=Second(timeValue)%>.
 		</div>
 	</body>
 </html>
```

## Referans ##

* [VBS - Wikipedia'dan](https://en.wikipedia.org/wiki/VBScript)



