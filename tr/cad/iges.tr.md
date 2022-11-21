{
  "date" : "2020-03-16",
  "keywords" :[ "IGES Dosyası", "Dosya Biçimi", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"IGES dosya formatı ve IGES dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"IGES Dosya Biçimi",
  "linktitle" : "IGES",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## IGES dosyası nedir?

Bilgisayar destekli tasarım (CAD) uygulamaları arasında tasarım bilgisi alışverişinde bulunmak için .iges uzantılı bir dosya kullanılır. IGES, İlk Grafik Değişim Spesifikasyonları anlamına gelir. IGES kullanılarak değiş tokuş edilen bilgiler arasında devre şeması, tel kafes, serbest biçimli yüzey veya katı modelleme temsilleri bulunur. IGES, uygulamalarını geleneksel mühendislik çizimlerinde, model analizinde ve üretim işlevlerinde bulur. Format, CAD programları arasında hem 2D hem de 3D tasarım bilgilerini değiştirebilir. IGES dosyaları, Autodesk ve CADSoftTools ABViewer gibi çeşitli CAD uygulamalarıyla açılabilir. IGES dosyalarını programlı olarak açmak ve dönüştürmek için kullanılabilen çeşitli API'ler de vardır.

## IGES Dosya Biçimi

IGES dosyaları ASCII metin biçimindedir ve dosyanın içeriğini görüntülemek için herhangi bir metin düzenleyicide açılabilir. Bir IGES dosyasındaki metinsel bilgiler "Hollerith" biçiminde temsil edilir. Ortak bir IGES dosyası, bu formata göre değiştirilebilen 2B veya 3B bilgileri temsil eden binlerce satır içerebilir. Bir IGES dosyası, 73. sütundaki özel büyük harfle gösterilen beş bölüme ayrılmıştır. Bu bölümler, 'Başlat' (S), 'Global' (G), 'Veri Girişi' (D), 'Parametre Verileri' (P) ve 'Sonlandır' (T) bölümleridir. Veri Girişi ve Parametre Verileri bölümleri genellikle sırasıyla DE ve PD olarak kısaltılır.

### IGES Dosya Başlığı

Başlangıç ve Genel bölümleri aşağıdakiler hakkında temel bilgiler içerir:
* Dosyanın adı ve kaynağı
* Parametre Verileri bölümü için sınırlayıcılar
* Dosyanın yazarı ve diğer genel bilgiler.

Wikipedia'daki örnek belgeden Başlangıç ve Genel bölümleri aşağıdaki gibidir.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
Görülebileceği gibi, başlangıç alanı dosyanın insan tarafından okunabilir açıklamalarını içerir ve satır bölüm başlığı ve bölüm satır numarası ile biten 1-72 sütunlarında herhangi bir karaktere sahiptir. Başlat bölümünde en az 1 satır olmalıdır. Genel bölüm, önişlemci verilerini içerir. Ayrıca dosyada bulunmalı ve G000000# formatıyla bitmelidir.

### Veri Girişi (DE) ve Parametre Verileri (PD) Bölümü

#### Veri Girişi Bölümü
Bir IGES dosyası, IGES dosya formatının temel verileri hakkında bilgi içeren birkaç varlıktan oluşur. Bir varlık, bir IGES veri formatının farklı öğeleri hakkında bilgi içerir ve çizim için kullanılır. Daha yaygın olarak kullanılan varlıklar şunları içerir:
* Dairesel Yay
* Kompozit Eğri
* Konik Yay
* Uçak
* Astar

Bunlar sadece birkaçı ve İGES'te yaklaşık 150 farklı varlık var. Her varlık, aşağıdaki gibi bir Tip numarası ile tanımlanır:
* DAİRESEL YAY(Tip 100)
* HAT (Tip 110)

##### Varlık Özellikleri

Bildirilen her varlık aşağıdaki özelliklere sahiptir.

|Alan Adı|Açıklama|
---|---|
|Varlık Tipi |Bu, açıklanan varlık tipidir. Örneğin, 116 bir Nokta varlığını tanımlar.|
|PD işaretçisi |Bu, Parametre Verileri bölümündeki bu varlık verilerinin konumunu verir. Bu konum, basitçe, bu varlık verilerinin ilk satırını içeren PD bölümünün içindeki satır numarasıdır.|
|Yapı |Sıfır veya tanım varlığına işaretçi. Çoğu kuruluş için geçerli değil|
|Çizgi Yazı Kalıbı| Satır yazı tipi deseni varlığına sayı veya işaretçi. Sayının anlamı: * 0 Desen belirtilmedi (varsayılan) * 1 Düz * 2 Kesikli * 3 Hayali * 4 Merkez Çizgisi * 5 Noktalı|
|Seviye| Bu varlıkla ilişkilendirilecek seviyeleri belirtir. Varlığın birden fazla seviyede görünmesine izin verir |
|Görünüm| Görüntüleme seçeneklerini belirtir. Bunlar: 0 Tüm görünümlerde eşit görünürlüğü ve özellikleri belirtir. Görünüm varlığına (Tip 410), Referans Görünüm Görünür İlişkilendirme varlığından (Tip 402, Form 3) görüntülenebileceğini gösteren Varsayılan İşaretçi
|Dönüşüm Matrisi işaretçisi| Bir dönüştürme matrisi varlığına başvurur (Tip 124) veya varsayılan olarak sıfırdır (dönüşüm yok)|
|Etiket Görünümü İlişkilendirme| Varlık etiketinin nasıl görüneceğini tanımlayan bir Etiket Görüntüleme İlişkilendirmesine (Tip 402, Form 5) başvurur.|
|Durum Numarası| İki sayının dört bölümünü içerir. 1-2: Boş durumu. Normal için 00 veya boş için 01. 3-4: Alt varlık anahtarı: bağımsız için 00, fiziksel olarak bağımlı için 01, mantıksal olarak bağımlı için 02 ve her ikisi için 03'tür. 5-6: Varlık Kullanım bayrağı: Geometri için 00, açıklama için 01, tanım için 02, Diğer için 03, Mantıksal için 04, 2B parametrik için 05 ve Yapı geometrisi için 06'dır. Son olarak, 7-8 hiyerarşidir; burada 00, genel yukarıdan aşağıya (bu varlığın özelliklerini kullanın), 01 genel ertelemeyi (bu varlığın özelliklerini kullanmayın) ve 02, hiyerarşi özelliğini kullanın (Hiyerarşi Varlığını kullanın (Tip 406, Form) 10)hiyerarşik gruplamanın özelliklerini belirlemek.|
|Sıra Numarası| D# tarafından belirtilir, burada # bu bölüm için satır numarasıdır (dosyanın en üstünden değil). Bu aynı zamanda bu Veri Girişi varlığına işaret etmek için kullanılır.|
|Varlık Türü| varlık listesi başına iki kez belirtilir|
|Hat Kalınlığı Sayısı| Varlık görüntülenirken kalınlığı belirtir. En küçük 1, 0 varsayılandır|
|Renk Numarası| Varlık rengini belirtir. İzin verilen tamsayı değerleri şunlardır: 0 Renk yok (varsayılan) 1 Siyah 2 Kırmızı 3 Yeşil 4 Mavi 5 Sarı 6 Macenta 7 Camgöbeği 8 Beyaz|
|Parametre Satırı Sayısı| Bu varlığın Parametre Verileri Bölümünde kapladığı satır sayısını belirtir |
|Form Numarası| Bu varlığın biçimini veya temsilini belirtir. Parametre verilerinin nasıl yorumlandığını değiştirir. Varsayılan 0|
|Ayrılmış Alan| Kullanılmıyor|
|Ayrılmış Alan| Kullanılmıyor|
|Varlık Etiketi| Uygulama belirtilen tanımlayıcı- sağa dayalı|
|Alt Simge Numarası| Varlık etiketi için sayısal niteleyici. İkisi birlikte varlık için benzersiz bir tanımlayıcı oluşturur |
|Sıra Numarası Yukarıya bakınız. |Her varlık iki satırda belirtildiği için bu D#+1 olacaktır.|

#### Parametre Veri Bölümü
Veri Girişleri bölümünü Parametre Verileri bölümü takip eder. İlgili her giriş için verileri listeler ve Global bölümünde belirtilen sınırlayıcılara dayalı olarak varlık için parametreleri listeler (genellikle parametreleri ayırmak için virgüller ve listeyi bitirmek için noktalı virgül).


## Referanslar
* [WikiPedia'dan IGES](https://en.wikipedia.org/wiki/IGES)

