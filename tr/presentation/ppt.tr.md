{
  "date" : "2019-12-13",
  "keywords" :[ "ppt dosyası", "ppt dosya formatı", "ppt dosyası nedir", "dosya", "ppt örneği", "ppt dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"PPT dosya formatı ve PPT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"PPT - PowerPoint Dosya Biçimi",
  "linktitle" : "PPT",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## PPT dosyası nedir?

PPT uzantılı bir dosya, SlideShow olarak görüntülemek için bir slayt koleksiyonundan oluşan PowerPoint dosyasını temsil eder. Microsoft PowerPoint 97-2003 tarafından kullanılan İkili Dosya Biçimini belirtir. Bir PPT dosyası, metin, madde işaretleri, resimler, multimedya ve diğer katıştırılmış OLE nesneleri gibi birkaç farklı türde bilgi içerebilir. Microsoft, 2007'den itibaren PowerPoint için [PPTX](/tr/presentation/pptx/) olarak bilinen, Office OpenXML tabanlı ve bu ikili dosya biçiminden farklı olan daha yeni bir dosya biçimi geliştirdi. OpenOffice Impress ve Apple Keynote gibi diğer bazı uygulama programları da PPT dosyaları oluşturabilir.

## Kısa Tarih ##

Microsoft, 1987'de PowerPoint'in piyasaya sürülmesiyle PPT dosya biçimini tanıttı. Kararlı ikili biçim, Windows için PowerPoint 97-2003'te varsayılan olarak paylaşıldı. İkili dosya formatı, PowerPoint 2016 da dahil olmak üzere PowerPoint'in en son sürümleri tarafından okuma ve yazma için desteklenir.

## Dosya Biçimi Özellikleri ##

Tanıtılmasından bu yana, PPT dosya formatı, yeni özelliklerin ve geliştirmelerin eklenmesi için çeşitli revizyonlardan geçti. Mevcut en son sürüm spesifikasyonları, Microsoft artık bu format için değişiklik sağlamadığından, Ağustos 2018'de yayınlanan ve PPT dosya formatının gerçek ürün numarasıyla karıştırılmaması gereken revizyon 6.0'a aittir.

### Dosya Biçimine Genel Bakış ###

Bir PPT dosya biçiminin temel bileşenlerinden bazıları şunlardır:

#### Slaytlar ####

Şekiller, metin, animasyonlar ve medya gibi kullanıcı verileri bir Slayt içindeki bir sunuya eklenir. Bir sunum, bir sunum çalıştırıldığında slayt gösterisi olarak görüntülenen bir veya daha fazla slayt içerebilir. Bir sunum, sunum slaytlarının ortak görsel özellikleri için şablon görevi gören ana slaytlar ve ana başlık slaytları içerir. Ayrıca, benzer bir amaca hizmet eden ve tüm not slaytları ve tüm basılı dinleyici notları için ortak görsel özellikler sağlayan bir asıl not slaydı ve genel dinleyici notu ana slaydı vardır.

#### Şekiller ####

Şekiller, kullanıcıların bir slayda yer tutucu şekiller, resimler ve grafikler biçiminde çeşitli içerikler eklemesine olanak tanıyan nesnelerdir. Ana slayttaki şekiller, şekil grupları için ortak verileri tanımlar.

#### Yer Tutucu Şekilleri ####

Bunlar, çeşitli nesneler için kap görevi gören özel yer tutuculardır. Tablolar veya grafikler gibi belirli şekil türlerini eklemek için ipuçları sağlamak üzere farklı yer tutucu şekiller kullanılabilir. Bir slaydın içinde, bir yer tutucu şekil ana ana slayttan, ana başlık slaydından veya notlar ana slaydından görsel özelliklere uyarlanır.

#### Harici Nesneler ####

Gömülü ve bağlantılı ses, bağlantılı video, gömülü ve bağlantılı OLE nesneleri ve köprüler gibi harici nesneler bir slayda gömülebilir. Bu nesneler, bir slayt gösterisi sırasında harici kaynaklara erişim için bağlantılı nesneleri etkinleştirmek için kullanılabilir.

### Dosya Biçimi Yapıları ###

PowerPoint ikili dosya formatları, genel belge yapısını ve verileri temsil eden aşağıdaki akışlardan oluşur.

* Mevcut Kullanıcı Akışı
* PowerPoint Belge Akışı
* Resim Akışı
* Özet Bilgi ve Belge Özet Bilgisi (Opsiyonel)

DOC dosya formatının tüm belirtimleri [Microsoft](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx) tarafından sağlanan şekilde bulunabilir ve bunlara başvurulmalıdır. aşağıdaki ayrıntılarda belirtilen bölümlere referansla.

#### Mevcut Kullanıcı Akışı ####

Dokümanı açan son kullanıcının kaydını tutar ve adı "Mevcut Kullanıcı" olmalıdır.

#### PowerPoint Belge Akışı ####

Bir PowerPoint sunumuyla ilgili tüm bilgilerin kaydını tutar ve düzenini ve içeriğini açıklar. Adı "PowerPoint Belgesi" OLMALIDIR, gerekli bir akıştır. Bu akışın içeriği, bir dizi üst düzey kayıt tarafından belirlenir. Kayıt dizisi üzerindeki kısmi sıralama kısıtlamaları, PersistDirectoryAtom ve UserEditAtom kayıtlarında belirtilir.

Container kayıtları olarak, DocumentContainer, MainMasterContainer (bölüm 2.5.3), HandoutContainer (bölüm 2.5.8), SlideContainer (bölüm 2.5.1) ve NotesContainer (bölüm 2.5.6) kayıtlarının her biri, kapsayıcı kayıtları ağacının köküdür ve atom kayıtları. Herhangi bir kapsayıcı kaydının içinde, açıkça alt kayıtlar olarak listelenmeyen başka kayıtlar bulunabilir. RecordHeader yapısının (bölüm 2.3.1) recType alanı, RecordType numaralandırması (bölüm 2.13.24) tarafından belirtilmeyen bir değer içerdiğinde, bilinmeyen kayıtlar tanımlanır. Bu bilinmeyen kayıtlarla karşılaşılırsa göz ardı edilmeli ve MUTLAKA <1> korunmalıdır. RecordHeader yapısının sonundan ileri recLen baytları aranarak bilinmeyen kayıtlar yok sayılabilir.

Bu akış her yazıldığında, yeni üst düzey kayıtlar, bir kullanıcı düzenlemesi mevcut akışa eklenebilir veya tüm akış içeriği, güncellenmiş bir üst düzey kayıt dizisiyle değiştirilebilir. Akışın tamamı değiştirilmezse, önceki herhangi bir kullanıcı düzenlemesini içeren önceden var olan herhangi bir üst düzey kayıt, geçerli kullanıcı düzenlemesini içeren sonradan eklenen üst düzey kayıtlar tarafından geçersiz kılınabilir.

#### Resim Akışı ####

Bu, bir PowerPoint sunumunda yer alan resimlerle ilgili verileri içeren isteğe bağlı bir akıştır. Adı "Resimler" OLMALIDIR. Bu akışın içeriği, [MS-ODRAW] bölüm 2.2.21'de belirtildiği gibi OfficeArtBStoreDelay kaydı tarafından belirtilir.

#### Özet Bilgi Akışı ####

Belge ile ilgili istatistikleri Microsoft Office standardına göre tutar. Özet Bilgi Akışının adı "\005SummaryInformation" olmalıdır; burada \005, "\005" dize değişmez değeri değil, 0x0005 değerine sahip karakterdir. Bu akış, şifrelenmiş belgeler için çıkarılmalıdır *ÖNERİLİ*. Bu akışın içeriği [MS-OSHARED] bölüm 2.3.3.2.1'de belirtilmiştir.

#### Belge Özeti Bilgi Akışı ####

Adı "\005DocumentSummaryInformation" OLMALIDIR, burada \005 0x0005 değerine sahip karakterdir, "\005" dizesi değil, isteğe bağlı bir akış. Bu akış <2> şifreli belgeler için atlanabilir. Bu akışın içeriği [MS-OSHARED] bölüm 2.3.3.2.2'de belirtilmiştir.

#### Şifreli Özet Bilgi Akışı ####

Adı "EncryptedSummary" OLMALIDIR, isteğe bağlı bir akış. Bu akış yalnızca şifrelenmiş bir belgede bulunur. Bu akışın içeriği [MS-OFFCRYPTO] bölüm 2.3.5.4'te belirtilmiştir.

#### Dijital İmza Depolama ####

Adı "_xmlsignatures" OLMALIDIR, isteğe bağlı bir depolama. İhmal edilebilir ve dikkate alınmayabilir. Bu depolamanın içeriği [MS-OFFCRYPTO] bölüm 2.5.2'de belirtilmiştir.

#### Özel XML Veri Depolama ####

Adı "MsoDataStore" OLMALIDIR, isteğe bağlı bir depolama. Depolamanın içeriği [MS-OSHARED] bölüm 2.3.6'da belirtilmiştir.

#### İmza Akışı ####

Adı "_signatures" OLMALI OLAN isteğe bağlı bir akış. İHMAL EDİLMESİ GEREKİR ve dikkate alınmayabilir. Bu akışın içeriği [MS-OFFCRYPTO] bölüm 2.5.1'de belirtilmiştir.

## Referanslar ##

* [PPT Dosya Biçimi özellikleri](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED]: Office Ortak Veri Türleri ve Nesne Yapıları](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] - Office Belge Şifreleme Yapısı](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [PowerPoint Dosya Biçimleri](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)

