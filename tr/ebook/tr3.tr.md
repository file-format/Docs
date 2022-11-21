{
  "date" : "2021-04-10",
  "keywords" :[ "TR3", "Dosya", "Uzantı", "Dosya Formatı", "eKitap", "TomeRaider", "Yadabyte" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"TR3 dosya formatı ve TR3 dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"TR3 - TomeRaider 3 eKitap Dosyası",
  "linktitle" : "TR3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-04-10"
}

## TR3 dosyası nedir? ##

TR3 dosyası, hızlı arama ve sıkıştırma için destek sağlayan bir TomeRaider 3 e-Kitabıdır. Bu, TomeRaider ile ilgili program aracılığıyla düzgün şekilde çalışabilir. Yadabyte, bu yazılımın geliştiricisi, bir İngiliz yazılım ve İngiltere merkezli web geliştirme şirketidir. TomeRaider e-Kitap okuyucu uygulaması, bu TR3 dosyalarının düzgün çalışması ve içeriğinin yönetilmesi için kullanılabilir. Bu ilgili e-Kitap okuyucu, Microsoft Windows tabanlı sistemler ve birçok aktarılabilir araç üzerinde çalışan bilgisayarlara kurulabilir. TR3 dosyası, Windows 10, Windows 7, Windows 8/8.1, Windows Vista, Windows XP gibi işletim sistemlerinde kullanılan eKitap Dosyaları grubuna aittir.

TR3'e özel **HTML etiketleri** aşağıdaki gibidir:

|Etiket|Açıklama|
---|---|
|\<new> |Metin dosyalarından TomeRaider dosyaları oluşturmak için gereken tek şey Yeni etiketidir.<new> etiketi sayfaların başlangıcını tanımlar.|
|\<CATDEF> ... \</CATDEF> |kategori adını tanımlar|
|\<META> ... \</META> | dosya biçiminde kullanılan tüm meta verileri tanımlamak için kullanılan bir etikettir. Bu etiket bir dizi parametre içerir.|
|\<EXPMSG> |Bu etiket, bir dosyanın süresi dolduğunda görünen mesajı kontrol eder. Bir kullanıcı, dosyanın süresi dolduktan sonra bir sayfayı görüntülemeye çalıştığında, asıl sayfa metni yerine süre sonu mesajı görünür.|
|\<DIEMSG> |Bu etiket, EXPMSG'ye benzer. Dosya öldüğünde bir mesaj görüntülemek için kullanılır.|
|\<ENGMSG> |Bu etiket, şifrelenmiş sayfalar için görüntülenen mesajı oluşturmak için kullanılır. Kullanıcı şifreli bir sayfayı kilidini açmadan açmaya çalışırsa, sayfa metni yerine mesaj görünür.|
|\<expmsg> ,\<diemsg> ve \<encmsg> |Sayfa metninde yok sayılır. İlkinden önce dosya başlığı bölümüne yerleştirilmelidirler.<new> etiket.|
|\<SELECTION> . \</ SELECTION> |Sorguları desteklemek için kullanılır. Bu etiket ilkinden önce olmalıdır<new> etiket. Kullanıcının sorgusu için seçim verilerini derler.|
|\<catset> . \</catset> | Her konu için kategori adları atamak için kullanılır.|


## TR3 dosyasını açma sorunları ##

Ortaya çıkabilecek ve dosya biçiminin yanlış çalışmasına neden olabilecek bazı yaygın sorunların listesi aşağıdadır:

* Bozuk dosya
* Virüs nedeniyle Etkilenen Dosya
* Arşiv erişimlerinde TR3 dosyasına uygunsuz bağlantılar
* Dosyaları açmak için sistemde erişim hakkı yok
* Sisteminizdeki eski sürücü
* TR3 raporunun Windows arşivinden kaldırılması
* Daha iyi çıktı için geliştiriciyle iletişime geçmek daha iyi bir seçenek olabilir

