{
  "date" : "2021-03-08",
  "keywords" :["PML", "eOkuyucu", "uzantı", "biçim", "eKitap", "Palm İşaretleme Dili"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"PML dosya formatı, Palm İşaretleme Dili ve PML dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"PML - Palm İşaretleme Dili Dosyası",
  "linktitle" : "PML",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## PML dosyası nedir?

Palm Inc, Palm İşaretleme Dili Dosyası anlamına gelen PML dosya formatını tanıttı. Amacı, tablet bilgisayara benzer bir e-Kitap okuma cihazı olan eOkuyucu için dokümanlar oluşturmaktır. PML dosyası, Palm Aygıtında görüntülenmesi için bir [PDB](/tr/ebook/pdb/) dosyasına (çeşitli veri dosyalarını içerir) yerleşimi verir.

## PML Dosyalarının teknik detayları

PML dosyalarının yapısı, paragraflar, başlıklar, girintiler ve referanslar dahil olmak üzere bir e-Kitap kurulumu oluşturmaya yönelik etiketlerden oluşur. Ayrıca Kalın, Küçük Büyük Harfler ve Üst Simge gibi biçimlendirme etiketlerine de izin verir. Geliştiriciler ayrıca e-Kitaplara resimler ekleyebilir.

### Palm İşaretleme Dili
Aşağıdaki tablo PML komutlarını belirtir:

|Komut|Açıklama|
---|---|
| \p | Yeni sayfa |
| \x | Yeni bölüm; ayrıca yeni bir sayfanın kesilmesine neden olur. Bölüm başlığını (ve herhangi bir stil kodunu) \x ve \x |
| \Xn | Yeni bölüm, Bölüm iletişim kutusunda girintili n seviye (0 ve 4 dahil n); sayfa kırılmasına neden olmaz. Bölüm başlığını (ve herhangi bir stil kodunu) \Xn ve \Xn |
| \Cn="Bölüm başlığı" | "Bölüm başlığı"nı bölüm listesine n düzeyinde (\Xn gibi) ekleyin. Metin sayfada gösterilmez ve sayfanın kesilmesine neden olmaz. Bu bazen, örneğin bir bölümün girişinin başına bir bölüm işareti eklemek için yararlı olabilir. |
| \c | Bu metin bloğunu ortalayın; satırın başında \c ile kapat |
| \r | Metin bloğunu sağa yasla; satırın başında \r ile kapat |
| \i | İtalik blok; \i | ile kapat
| \ u | Altı çizili blok; \u | ile kapat
| \ o | Aşırı blok; \o | ile kapat
| \v | Görünmez metin; \v ile kapat (yorumlar için kullanılabilir) |
| \t | Girinti bloğu. Satır başında başlayın, satırın sonunda \t |
| \T="%50" | Ekran genişliğinin belirtilen yüzdesini girintiler, bu durumda %50. Geçerli çizim konumu zaten belirtilen ekran konumunu geçmişse, bu etiket dikkate alınmaz. |
| \w="%50" | Ekranın belirli bir yüzde genişliğine (bu durumda %50) yatay bir kural yerleştirin. Bu etiket, kendisinden önce ve sonra satır kesilmesine neden olur. Kural merkezlidir. Yüzde işareti zorunludur. |
| \n | Kullanıcı tarafından belirlenen "normal" yazı tipine geçin |
| \s | stdFont'a geçin; normal yazı tipine dönmek için \s ile kapatın |
| \b | boldFont'a geçin; normal yazı tipine dönmek için \b ile kapatın (kullanımdan kaldırıldı; bunun yerine \B kullanın) |
| \ l | largeFont'a geçin; normal yazı tipine dönmek için \l ile kapatın |
| \B | Metni kalın olarak işaretleyin. \b etiketinin aksine, \B yazı tipini değiştirmez, bu nedenle büyük kalın metinlere sahip olabilirsiniz. \b ve \B'yi aynı PML dosyasında karıştıramazsınız. |
| \Sp | Metni üst simge olarak işaretleyin. Kalın, italik vb. diğer stillerle karıştırılmamalıdır. Üst simgeli metni \Sp ile çevreleyin. |
| \Sb | Metni alt simge olarak işaretleyin. Kalın, italik vb. diğer stillerle karıştırılmamalıdır. İndisli metni \Sb ile çevreleyin. |
| \ k | Kapalı metni küçük büyük harflere dönüştürün; \k ile kapatın. \k etiketlerinin içine alınmış tüm karakterler (aksanlı olanlar dahil) büyük harf yapılır ve normal bir büyük harf karakterden daha küçük punto boyutunda işlenir. |
| \\ | Tek bir ters eğik çizgiyi temsil eder |
| \aXXX | Windows-1252 kodu ondalık XXX olan ASCII olmayan bir karakter girin. Ayrıntılar için PML karakter tablosuna bakın. |
| \UXXXX | Unicode kodu onaltılık XXXX olan ASCII olmayan bir karakter girin. Ayrıntılar için Genişletilmiş PML karakter tablosuna bakın. |
| \m="görüntüadı.png" | Adlandırılmış görüntüyü ekleyin. Aşağıdaki Görseller bölümüne bakın. |
| \q="#linkanchor"Biraz metin\q | Belgede başka bir noktada bulunan bir bağlantı bağlantısına başvurun. Bağlantı belirtiminden sonraki ve sonundaki \q'dan önceki dizenin altı çizilir veya belge görüntülenirken bir bağlantı olarak gösterilir. |
| \Q="bağlantı" | Belgede bir bağlantı çapası belirtin. |
| \- | Yumuşak bir tire ekleyin. Yumuşak bir tire, yalnızca bir sözcüğü bir satır boyunca bölmek gerektiğinde görünür. |
| \Fn="footnote1"1\Fn | "1"i, adı dipnot1 olan ve PML belgesinin sonunda etiketlenmiş bir dipnota bağlayın. Aşağıdaki Dipnotlar ve Kenar Çubukları bölümüne bakın. |
| \Sd="kenar çubuğu1"Kenar Çubuğu\Sd | "Kenar Çubuğu" metnini, adı kenar çubuğu1 olan ve PML belgesinin sonunda etiketlenmiş bir kenar çubuğuna bağlayın. Aşağıdaki Dipnotlar ve Kenar Çubukları bölümüne bakın. |
| \ben | Referans dizin öğesi olarak işaretleyin. Dizin öğesini (ve tüm stil kodlarını) \I ve \I ile çevreleyin.|
 


## Referanslar

* [Palm İşaretleme Dili - MobileRead Tarafından](https://wiki.mobileread.com/wiki/EReader)
* [E-Okuyucu - MobileRead Tarafından](https://en.wikipedia.org/wiki/E-reader)

