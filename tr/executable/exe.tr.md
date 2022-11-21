{
  "date" : "2021-06-30",
  "keywords" :[ "exe dosyası", "exe dosya biçimi", "exe dosyası nedir", "dosya", "exe örneği", "exe dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Bir .exe dosyası, Windows işletim sisteminde çalışan Microsoft Yürütülebilir bir dosyadır. EXE dosya formatı hakkında daha fazla bilgi edinin.",
  "title" :"Yürütülebilir EXE dosyası nedir?",
  "linktitle" : "EXE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Bir EXE dosyası nedir?

EXE kelimesi **executable**'ın kısaltmasıdır. Bir .exe dosyası, Microsoft Windows işletim sisteminde yürütülebilen bir programdır. Uygulama geliştiriciler çoğunlukla Windows işletim sistemi için programlarını yürütülebilir biçimde exe dosyaları olarak yayınlarlar. Windows'ta uygulamaları çalıştırmak için standart dosya biçimidir. **Setup.exe**, **Install.exe** ve **cmd.exe**, EXE dosyalarının bazı yaygın ve iyi bilinen adlarıdır.

## EXE Dosya Biçimi

MS-DOS derleyicileri, 64K bellek sınırlamasına sahip bellek modelleriyle tanıtıldı. Genel konsept, x86 CPU'da (CS, DS, ES, SS) farklı segment kayıtlarını farklı veya aynı segmentleri gösterecek şekilde ayarlamaktır, bu nedenle belleğe çeşitli derecelerde erişim sağlar. Bazı özel bellek modelleri şunlardı:

- **Küçük**: Tüm bellek erişimleri 16 bittir (segment kayıtları değişmemiştir). .EXE dosyası yerine .COM dosyası üretir.
- **Küçük**: Tüm bellek erişimleri 16 bittir (segment kayıtları değişmemiştir).
- **Kompakt**: Veri adresleri, erişim sırasında DS veya ES kayıtlarını yeniden yükleyerek ve 1M'ye kadar veriye izin vererek hem segment hem de ofset içerir. Kod erişimleri CS kaydını değiştirmez ve 64K koda izin verir.
- **Orta**: Kod adresleri segment adresini içerir, erişimde CS'yi yeniden yükler ve 1M'ye kadar koda izin verir. Veri erişimleri DS ve ES kayıtlarını değiştirmez, 64K veriye izin verir.
- **Büyük**: Hem kod hem de veri adresleri (segment, ofset) çiftleridir ve her zaman segment adreslerini yeniden yükler. 1M bayt bellek alanının tamamı hem kod hem de veriler için kullanılabilir.
- **Devasa**: 64K'dan büyük dizilere erişime izin vermek için derleyici tarafından oluşturulan ek aritmetik ile büyük modelle aynıdır.

Geliştiriciler, bir exe dosyası oluştururken hangi modelin seçilmesi gerektiğine karar vermelidir.

### Taşınabilir EXE Dosya Biçimi

Taşınabilir yürütülebilir dosya formatı (PE) bir dizi bilgi başlığı içerir, başlıkların listesi aşağıdadır:

- **DOS üstbilgisi**: MS-DOS üstbilgisi, geriye dönük uyumluluğu veya yeni dosya türlerinin kademeli olarak düşürülmesini sağlar.
- **PE Başlığı**: DOS başlığının başlangıcından itibaren 60 (0x3C) ofsetinde PE Dosyası başlığına bir işaretçidir
- **COFF Başlığı**: COFF başlığı, bir yürütülebilir dosya için yararlı olan bazı bilgilere ve bir nesne dosyası için daha yararlı olan bazı bilgilere sahiptir.
- **PE İsteğe Bağlı Başlık**: PE İsteğe Bağlı Üstbilgi, doğrudan COFF başlığından sonra gelir ve hatta bazı kaynaklar iki başlığı aynı yapının parçası olarak gösterir.
- **Bölüm Tablosu**: PE İsteğe Bağlı Başlıktan hemen sonra bir bölüm tablosu buluruz. Bölüm tablosu, bir dizi IMAGE_SECTION_HEADER yapısından oluşur.
- **Eşlenebilir Bölümler**: Bir kitaplığın kodunu birden fazla işlemle eşleyerek bellekte yer kazandırabilir.

## Mac'te bir EXE dosyası çalıştırabilir misiniz?

Exe dosyaları, Mac OS'de yürütülebilir dosya olarak kullanılmaz. Ancak Mac OS üzerinde bir exe dosyası çalıştırmak isterseniz aşağıdaki yöntemler kullanılabilir.

1. **Şarap** - Şarap, PC uygulamalarını Mac sistemlerinde kullanmak isteyenler için mükemmel bir çözümdür. Bu, "Şarap Bir Öykünücü Değildir" anlamına gelen bir kısaltmadır. Wine, Microsoft tarafından kullanılanla aynı dizin ortamını oluşturur, böylece onu kullanarak Windows uygulamanızı çalıştırabilirsiniz.
2. **Sanal Makineler** - Parallel Desktop veya VM Virtual Box kullanarak bir Windows Sanal Makinesi oluşturun ve uygulamanızı sanal makine içinde çalıştırın.
3. **Boot Camp** - Mac OS'de Windows Boot Camp'i yüklemek ve yapılandırmak, Windows OS'yi Mac makinesinde çalıştırmanıza olanak tanır.

## Referanslar

* [.exe- Wikipewdia tarafından](https://en.wikipedia.org/wiki/.exe)
* [x86 Disassembly/Windows Yürütülebilir Dosyalar](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)

