{
  "date" : "2019-10-11",
  "keywords": [ "pdb file", "pdb", "extension", "format", "What is a pdb file", "pdb file format", "PDB metadata" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDB Dosya Biçimi - Bir Program Veritabanı Dosyası",
  "description":"PDB dosya formatı ve PDB dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "PDB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Bir PDB dosyası nedir?

.pdb uzantılı bir dosya, derlenmiş bir yürütülebilir dosya (EXE/DLL) için hata ayıklama bilgileri içeren bir program veritabanı dosyasıdır. PDB dosyaları, bir uygulama programı hata ayıklama modunda derlendiğinde Microsoft Compilers tarafından oluşturulur. PDB dosyasının varlığı, modüllerin tüm sembolleri hakkında önemli bilgiler içerdiğinden yürütülebilir bir dosyanın tersine mühendislik işlemine yardımcı olabilir. Bu nedenle bu dosyalar son yürütülebilir dosyadan ayrı tutulur. Microsoft'un [DgbHelp API'si](https://docs.Microsoft.com/en-us/windows/win32/debug/dbghelp-functions), ortaklar ve dışa aktarmalar, genel semboller, yerel semboller gibi bilgileri elde etmek için bir PDB dosyası açabilir. veri, kaynak dosyaları ve satır numaralarını yazın.

## PDB Dosya Biçimi

PDB, Microsoft'un tescilli dosya biçimidir ve henüz hiçbir yerde resmi olarak belgelenmemiştir. Ancak, bir başlangıç belgesi [burada](https://github.com/Microsoft/microsoft-pdb) mevcuttur ve başvurulabilir.

### PDB Akışları

PDB dosyaları, her akışın sanal bir bağımsız dosya gibi davrandığı ve bilgi içerdiği birden çok akıştan oluşur. PDB dosya yazarları bu dosyalara yazabilir ve dosya yalnızca açık bir taahhüt verildikten sonra sonlandırılır. Bir derleyici, bir PDB dosyasına yazmaya devam edebilir, ancak yalnızca tüm kullanıcı kodu başarıyla derlenirse taahhütte bulunabilir. Bir PDB dosyası aşağıdaki akışlardan oluşur:

|Akış No. |İçindekiler |Kısa Açıklama|
---|---|---|
|1| Pdb (başlık) |Sürüm bilgisi ve bu PDB'yi EXE'ye bağlamak için bilgi|
|2| Tpi (Tip yöneticisi) |Yürütülebilir dosyada kullanılan tüm türler.|
|3| Dbi (Hata ayıklama bilgisi) |Bölüm katkılarını ve 'Modlar' listesini tutar|
|4| İsim Haritası| Karma bir dize tablosu tutar|
|4-(n+4)| n Mod'lar (Modül bilgisi)| Her Mod akışı, bir derleme alanı için sembolleri ve satır numaralarını tutar|
|n+4| Global sembol hash| İsme göre global sembollerde arama yapmaya izin veren bir indeks |
|n+5| Genel sembol hash| Genel sembollerde adreslere göre arama yapılmasını sağlayan bir dizin|
|n+6| Sembol kayıtları| Global ve genel sembollerin gerçek sembol kayıtları|
|n+7| Hash yazın| TPI akışı tarafından kullanılan karma.|

Bir PDB dosyasındaki her akış, mutlaka ardışık olarak numaralandırılmayan birkaç sayfadan oluşur.

### PDB başlığı

Bir PDB dosyası, belirli biçimi tanımlamak ve doğrulamak için bir imzadan oluşan bir Başlığa sahiptir. İmzanın uzunluğu PDB formatına bağlıdır. Başlık, tek bir sayfadan daha uzun olabilir.

### PDB Meta Verileri
PDB meta verileri, her akış için sayfaların uzunluğunu ve sırasını vererek tüm bileşen akışlarını tanımaktan sorumludur. Dizilere sıralı olarak emirler verilir; 0'dan başlayarak. Bazı meta verileri içeren sıralanmamış bir kök akış da vardır.

## Referanslar
* [PDB - Wikipedia](https://en.wikipedia.org/wiki/Program_database)
* [Microsoft PDB](https://github.com/Microsoft/microsoft-pdb)

