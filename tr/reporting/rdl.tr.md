{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDL - Rapor Tanımlama Dili Dosyası",
  "keywords" :[ "rdl", "rapor tanımlama dili", "XmlTextWriter", "XSD", "RDL öğesi"],
  "description":"SQL Server Reporting Services rapor tanımının XML temsili olan RDL dosya biçimi hakkında bilgi edinin.",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-01"
}

## RDL dosyası nedir? ##

RDL (Rapor Tanımlama Dili), raporların tanımlanması için Microsoft tarafından belirlenen bir kıyaslamadır. Bir RDL dosyası, bir veya daha fazla RDL Öğesinden oluşur. Oysa bir RDL öğesi, veri türünden ve kardinalitesinden oluşur. Bir eleman basit veya karmaşık olabilir. Basit öğenin herhangi bir alt öğesi veya niteliği yoktur, oysa karmaşık bir öğenin alt öğesi ve isteğe bağlı nitelikleri vardır.

## RDL XML Şeması Tanımı
Bir XML Şema Tanımı (XSD) dosyası, RDL dosyasını doğrular. Şema, bir .rdl dosyasında RDL öğelerinin nerede bulunabileceğine ilişkin kuralları tanımlar. Bir RDL öğesi basit veya karmaşık olabilir. Basit bir öğenin alt öğeleri veya nitelikleri yoktur ve karmaşık bir öğenin alt öğeleri ve isteğe bağlı olarak nitelikleri vardır.

## RDL oluşturma
RDL doğası gereği açık ve genişletilebilir olduğundan, XML şemasına dayalı olarak RDL dosyaları oluşturan birçok uygulama ve araç oluşturulabilir. Bir uygulamadan RDL oluşturmanın en basit yollarından biri, **System.Xml** ad alanının ve System.Linq ad alanının Microsoft .NET Framework sınıflarını kullanmaktır. Özellikle **XmlTextWriter** sınıfı, RDL yazmak için kullanılabilir. **XmlTextWriter** kullanarak herhangi bir .NET Framework uygulamasında baştan sona eksiksiz bir rapor tanımı oluşturabilirsiniz. Geliştiriciler, RDL'yi genişletmek için özel özelliklere sahip özel rapor öğeleri de ekleyebilir.

## RDL Türleri
Aşağıdaki tablo, RDL öğelerinde kullanılan türleri ve öznitelikleri listeler.

|Tür|Açıklama|
---|---|
|İkili |64 tabanlı kodlanmış ikili değere sahip bir özellik.|
|Boole| Nesnenin değeri olarak true veya false olan bir özellik. Aksi belirtilmedikçe, atlanan isteğe bağlı bir Boolean nesnesinin değeri False olur.|
|Tarih |ISO8601 tarih biçiminde belirtilen tam tarih veya tarih saat değerine sahip bir özellik: YYYY-AA-GG[THH:MM[:SS[.S]]].|
|Enum |Atanan değerler listesinden biri olması gereken dize metin değerine sahip bir özellik.|
|Float |Kayan değere sahip bir özellik. İsteğe bağlı ondalık ayırıcı olarak nokta (.) kullanılır.|
|Tamsayı |Tamsayı (int32) değerine sahip bir özellik.|
|Dil |ABD İngilizcesi için "en-us" gibi bir dil ve kültür kodu içeren metin değerine sahip bir özellik. Değer, belirli bir dil veya Microsoft .NET Framework'te kendisi için varsayılan bir dilin tanımlandığı tarafsız bir dil olmalıdır.|
|Ad |Dize metin değeri olan bir özellik. Adlar, öğenin ad alanı içinde benzersiz olmalıdır. Belirtilmezse, bir öğenin ad alanı, bir adı olan en içteki içeren nesnedir.|
|NormalizedString |Normalleştirilmiş dize metin değerine sahip bir özellik.|
|Boyut |Bir boyut öğesi bir sayı içermelidir (isteğe bağlı ondalık ayırıcı olarak nokta karakteri kullanılır). Sayının ardından cm, mm, in, pt veya pc gibi bir CSS uzunluk birimi için bir tanımlayıcı gelmelidir. Numara ile belirtici arasında bir boşluk isteğe bağlıdır. Boyut göstergeleri hakkında daha fazla bilgi için bkz. CSS Değerleri ve Birim Referansı.RDL'de Boyut için maksimum değer 160 inç'tir. Minimum boyut 0 inç'tir.|
|String |Dize metin değeri olan bir özellik.|
|UnsignedInt |İşaretsiz tamsayı (uint32) değerine sahip bir özellik.|
|Variant |Herhangi bir basit XML tipine sahip bir özellik.|

## RDL Veri Türleri
RDL'de DataType Enumeration, bir özniteliğin, ifadenin veya parametrenin veri türünü tanımlar. Aşağıdaki tablo, CLR veri türlerinin RDL veri türlerine nasıl karşılık geldiğini gösterir.

|CLR Tür(ler)i |İlgili Veri Türü|
---|---|
|Boole| Boole |
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, Bayt, SByte |Tamsayı|
|Tek, Çift |Yüzer|
|Dize, Karakter, GUID, Zaman Aralığı |Dize|


## Referanslar ##

- [Rapor Tanımlama Dili (Wikipedia)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Rapor Tanımlama Dili (SSRS)](https://docs.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

