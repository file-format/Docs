{
  "date" : "2021-06-14",
  "keywords" :[ "SAV", "uzantı", "sav dosyası", "sav dosya biçimi", "Veritabanı Dosya Türü", "Veritabanı Dosya Biçimi", "sav dosyası nedir" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"SAV dosya formatı ve SAV dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"SAV - SPSS Veri Dosyası",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "identifier":"database-sav",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## SAV dosyası nedir?
SAV dosyası, istatistiksel analiz için pazar araştırmacıları, sağlık araştırmacıları, anket şirketleri, hükümet, eğitim araştırmacıları, pazarlama kuruluşları, veri madencileri tarafından yaygın olarak kullanılan bir uygulama olan Statistical Package for the Social Sciences (SPSS) tarafından oluşturulan bir veri dosyasıdır. SAV, tescilli bir ikili biçimde kaydedilir ve bir veri kümesinin yanı sıra veri kümesini temsil eden bir sözlükten oluşur, verileri satırlar ve sütunlar halinde kaydeder.

## SAV Dosya Biçimi
SAV dosya formatı nispeten kararlı hale geldi, ancak statik olduğunu söyleyemeyiz. Gerektiğinde geriye ve ileriye dönük uyumluluk isteğe bağlı olarak sağlanır, ancak gerektiği gibi sürdürülmez. Bir SAV dosyasındaki veriler aşağıdaki bölümlere ayrılmıştır:

### Dosya başlığı
176 bayttan oluşur. İlk 4 bayt, dosya için kullanılan karakter kodlamasında **$FL2** veya **$FL3** dizesini gösterir. Son üç bayt, dosyadaki verilerin **ZLIB** kullanılarak sıkıştırıldığını gösterir. Sonraki 60 baytlık dize **@(#) SPSS DATA FILE** ile başlar ve ayrıca işletim sistemini ve dosyayı oluşturan SPSS sürümünü belirler. Başlık daha sonra, gözlem başına değişken sayısını ve sıkıştırma için bir basamak kodunu içeren altı basamaklı alanlarla devam eder ve oluşturma tarihini, saatini ve bir dosya etiketini gösteren karakter verileriyle sona erer.
### Değişken tanımlayıcı kayıtları
Kayıt, SPSS tarafından kullanılan biçimlendirme bilgileriyle birlikte değişkenin türünü ve adını sınıflandıran sabit bir alan dizisi içerir. Her bir değişken kaydı isteğe bağlı olarak en fazla 120 karakterlik bir değişken etiketi ve üç adede kadar eksik değer belirtimi içerebilir.
### Değer etiketleri
Değer etiketleri isteğe bağlıdır ve 3 ve 4 tamsayı etiketlerine sahip kayıt çiftlerinde saklanır. Etiket 3 olan ilk kayıt, her bir çift bir değer ve ilişkili değer etiketi içeren bir dizi alan çiftine sahiptir. Etiket 4 olan ikinci kayıt, değerler/etiketler kümesinin hangi değişkenler için geçerli olduğunu gösterir.
### Belgeler
Tamsayı etiketli tek veya birden çok kayıt 6. İsteğe bağlı belgeler. 80 karakterlik satırlar içerir.
### Uzantı kayıtları
Tamsayı etiketli tek veya birden çok kayıt 7. Uzantı kayıtları, güvenli bir şekilde göz ardı edilebilecek bilgiler sağlar, ancak çoğu durumda korunan bilgiler, yeni yazılımlar tarafından yazılan dosyaların geriye dönük uyumluluğu korumasını sağlar. Uzantı kayıtlarında tamsayı alt tür etiketleri bulunur.
### Sözlük sonlandırıcı
Yalnızca 999 tamsayı etiketiyle kaydedin. Sözlüğü veri gözlemlerinden ayırır.
### Veri gözlemleri
Verilerin gözlem sırasında olduğu kabul edilir, örneğin ilk gözlem için tüm değişken değerleri, ardından ikinci gözlem için tüm değerler vb. Veri kaydının formatı, dosya başlığı kaydındaki sıkıştırma koduna bağlı olarak değişir. Bir .sav dosyasının veri kısmı sıkıştırılmamış olabilir:
- **kod 0**: bayt koduyla sıkıştırılmış
- **kod 1**: ZLIB sıkıştırması kullanılarak sıkıştırılmış
 







## Referanslar ##

* [SPSS Sistem Veri Dosyası Format Ailesi (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)

