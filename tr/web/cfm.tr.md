{
  "date" : "2021-07-13",
  "keywords" :[ "CFM", "uzantı", "dosya", "biçim", "sistem", "Cold Fusion İşaretleme Dili", "dil", "CFM web sayfaları", "CFML motoru", "CFML"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFM - Soğuk Füzyon İşaretlemesi",
  "description":"CFM dosya formatı ve CFM dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CFM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## .cfm dosyası nedir? ##

**Cold Fusion İşaretleme Dili**'nde kullanılan web sayfaları ve dosyalar, CFM'nin uzantılarını içerir ve CFM web sayfaları olarak adlandırılır. Bu web geliştirme betik dili, Google App Engine, .NET çerçevesi ve JVM üzerinde çalışır. Bir programlama dili veya dilin kodunu içerebilir. Sayfalarından herhangi birine kullanıcı tarafından erişildiğinde, ColdFusion web sunucusu onu yürütür. CFML yazmak için CFScript (JavaScript'e yakın) veya etiketler kullanılabilir. CFML, [HTML](/tr/web/html/) dışında [CSS](/tr/web/css/), [JavaScript](/tr/web/js/), [XML](/tr/web/) gibi diğer dilleri oluşturmak için kullanılabilir. xml/) ve daha fazlası.

Bu dilin ve desteklediği etiketlerin kullanımı daha çok dinamik web uygulamalarının geliştirilmesindedir. Uygulamanın geliştirildiği platformun çevrimdışı kullanımı sırasında herhangi bir hata oluşursa, dosyalar doğrudan çevrimiçi olarak tarayıcıda çalıştırılabilir.
 

CFML, belirli sunucu dosya uzantılarının (.cfc, .cfm) CFML motoruna işlenmek üzere verildiği şekilde çalışır. Motorlar Java tabanlıysa, Java servlet'leri kullanılarak elde edilir. CFML'nin motoru sadece fonksiyonları ve etiketleri işler ve CFML etiketleri dışındaki fonksiyonları ve metni herhangi bir değişiklik yapmadan web sunucusuna döndürür.


## Kısa Tarih ##

1995 yılında ilk olarak Allaire adlı bir şirket tarafından kuruldu. 2005 yılında Adobe satın aldı ve halen ColdFusion'u geliştirmek için hizmetler sağlıyor. Geçen yıllar içerisinde birçok kişi ve firma tarafından geliştirildi ve güncellendi. 2012 yılında OpenCFML adlı bir vakıf kuruldu. Daha sonra, 2015 yılında eski Railo, CFM'nin performansını iyileştirmek için hizmetlerini sağladı ve daha iyi işlevsellik için kaynakları azalttı. En son güncellemesi 2020 yılında çıkmış ve 2028 yılına kadar devam edeceği duyurulmuştur.

## CFM Dosya Biçimi ##

CFM dosyalarının ve web sayfalarının kodu, küçük bir farkla çoğunlukla HTML gibi etiketlerden oluşur. Bu dosyalar, ColdFusion betiklerinin çalışmasını sağlayan çeşitli işlemleri gerçekleştirmekten sorumludur.
* Bu dosyalara herhangi bir işletim sisteminin tarayıcısı kullanılarak doğrudan hem Windows hem de macOS üzerinde erişilebilir ve çalıştırılabilir.
* Adobe ColdFusion, PC'de web sayfalarının ve dinamik uygulamaların geliştirilmesi için platform sağlar.
* Bu dosyalar metin tabanlı olduğundan, NotePad gibi herhangi bir metin düzenleyici veya bir işletim sistemindeki başka bir metin düzenleyici bu dosyaları açmak için kullanılabilir.
* Herhangi bir CFM dosyası bir metin düzenleyicide açıldığında, bir kişinin web geliştiricisi olmadığı sürece anlayamayacağı etiketlerden ve komut dizilerinden oluşan kodu görüntüler.

## CFM Kullanım Örneği ##

Aşağıda basit bir kullanım örneği CFM dosyası gösterilmektedir.

### CFM Belgesi ###

```html
<!--- temperature.cfc --->
<cfcomponent>
  <cffunction name="FtoC" access="public" returntype="numeric">
    <cfargument name="fahrenheit" required="yes" type="numeric" />
    <cfset answer= (fahrenheit - 32)*100/180 />
    <cfreturn answer />
  </cffunction>
</cfcomponent>
<!--- test.cfm --->
<cfset fDegrees = 212 />
<cfinvoke component="temperature" method="FtoC" returnvariable="result">
  <cfinvokeargument name="fahrenheit" value="#fDegrees#" />
</cfinvoke>
<cfoutput>#fDegrees#&deg;F = #result#&deg;C</cfoutput> <br />
```

## Referanslar ##

- [CFM - Wikipedia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

