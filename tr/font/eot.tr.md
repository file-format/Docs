{
  "date" : "2020-08-20",
  "keywords" :[ "eot dosyası", "eot dosya biçimi", "eot dosyası nedir", "dosya", "eot örneği", "eot dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - TrueType Yazı Tipi Dosya Biçimi",
  "description":"EOT Dosya Biçimi ve EOT dosyaları oluşturmak ve açmak için API'ler hakkında bilgi edinin.",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## .eot dosyası nedir?

.eot uzantılı bir dosya, belgeye katıştırılmış bir OpenType yazı tipidir. Bunlar çoğunlukla Web sayfası gibi web dosyalarında kullanılır. Microsoft tarafından oluşturulmuştur ve PowerPoint sunum [.pps](/tr/presentation/pps/) dosyası dahil olmak üzere Microsoft Ürünleri tarafından desteklenmektedir. Dosya birincil kullanım değildir ve ana belge veya web sayfasıyla birlikte bir tür eşlik eden belgedir. OTF yazı tiplerine benzer şekilde EOT, glifler için hem Postscript hem de TrueType ana hatlarını destekler. EOT dosyalarının boyutu, LZ sıkıştırması kullanılarak sıkıştırılmaları nedeniyle daha küçüktür. EOT, mevcut TTF/OTF yazı tiplerinden bir yazı tipi oluşturmak için bir Microsoft aracı kullanır.

## Kısa Tarihçe

EOT yazı tipi, 2007 yılında CSS3'ün bir parçası olarak W3C'ye sunuldu, ancak uzak sisteme kalıcı olarak yüklenmesi gereklilikleri nedeniyle reddedilmesine neden oldu. Mart 2008'de yeniden gönderildi, ancak W3C sonunda o zaman standartlaştırılmış olan [Web Yazı Tipi Formatını](/tr/font/woff/) (WOFF) seçti.

## EOT Dosya Biçimi

EOT dosya formatı ayrıntıları [W3 gönderim sayfasında](https://www.w3.org/Submission/EOT/#FileFormat) bulunabilir ve bu yazı tipi formatı tarafından kullanılan yapı ayrıntılı olarak açıklanır. EOT, hte yazı tipi adı ve desteklenen karakterler hakkında yeterli temel bilgi sağlayan tek bir EMBEDDEDFONT yapısından oluşur. Bu bilgilerin paketlenmesi, Kullanıcı Aracılarının, makinede zaten mevcutsa yazı tipini paketinden çıkarmaktan, sıkıştırılmış dosyayı açmaktan veya yüklemekten kaçınmasını sağlar.

### EMBEDDEDFONT Yapısı
EMBEDDEDFONT yapısı, her revizyonda yapının sonuna ek veriler eklenerek üç revizyondan geçmiştir. EMBEDDEDFONT yapısının son revizyonu aşağıda gösterildiği gibidir.

|Veri Türü|Giriş Adı|Açıklama|
---|---|---|
|unsigned long|EOTSize|Bayt cinsinden toplam yapı uzunluğu (dize ve yazı tipi verileri dahil)|
|unsigned long|FontDataSize|OpenType yazı tipinin (FontData) bayt cinsinden uzunluğu|
|unsigned long|Sürüm|Bu biçimin sürüm numarası - 0x00020002|
|unsigned long|Bayraklar|İşleme İşaretleri|
|bayt[10]|FontPANOSE|Bu yazı tipi için PANOSE değeri - Bkz. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#pan|
|bayt|Karakter Kümesi|Windows'ta bu TEXTMETRIC.tmCharSet'ten türetilmiştir. Bu değer, yazı tipinin karakter kümesini belirtir. DEFAULT_CHARSET (0x01) tercih olmadığını gösterir. - Bakınız https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|bayt|İtalik|ITALIC için bit OS/2.fsSelection'da ayarlanmışsa, değer 0x01 olacaktır - Bkz. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fss|
|unsigned long|Ağırlık|Bu yazı tipi için ağırlık değeri - Bkz. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#wtc|
|unsigned short|fsType|Gömme izinleri hakkında bilgi sağlayan tip bayrakları - Bkz. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fst|
|unsigned short|MagicNumber|EOT dosyası için sihirli sayı - 0x504C. Veri bozulmasını kontrol etmek için kullanılır.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (bit 0-31) - Bkz. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (bit 32-63) - Bkz. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (bit 64-95) - Bkz. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (bit 96-127) - Bkz. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|CodePageRange1|CodePageRange1 (bit 0-31) - Bkz. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (bit 32-63) - Bkz. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment - Bkz. https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|işaretsiz uzun|Ayrılmış1|Ayrılmış - 0 olmalıdır|
|unsigned long|Ayrılmış2|Ayrılmış - 0 olmalıdır|
|işaretsiz uzun|Ayrılmış3|Ayrılmış - 0 olmalıdır|
|işaretsiz uzun|Ayrılmış4|Ayrılmış - 0 olmalıdır|
|unsigned short|Padding1|Uzun hizalamayı korumak için dolgu. Dolgu değeri her zaman 0x0000 olarak ayarlanmalıdır.|
|unsigned short|FamilyNameSize|FamilyName dizisi tarafından kullanılan bayt sayısı|
|bayt|AileAdı[AileAdıBoyutu]|AileAdıBoyutu bayt uzunluğunda UTF-16 karakter dizisi. Bu, yazı tipinin ad tablosunda bulunan İngilizce Yazı Tipi Ailesi dizesidir (ad kimliği = 1) - Bkz. https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding2|Padding değeri her zaman 0x0000 olarak ayarlanmalıdır.|
|unsigned short|StyleNameSize|StilAdı tarafından kullanılan bayt sayısı|
|byte|StyleName[StyleNameSize]|StyleNameSize bayt uzunluğunda UTF-16 karakter dizisi. Bu, yazı tipinin ad tablosunda bulunan İngilizce Yazı Tipi Alt Ailesi dizesidir (ad kimliği = 2) - Bkz. https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding3|Padding değeri her zaman 0x0000 olarak ayarlanmalıdır.|
|unsigned short|SürümAdıSize|SürümAdı tarafından kullanılan bayt sayısı|
|bayt|SürümAdı[SürümAdıBoyutu]|VersiyonAdıBoyutu bayt uzunluğunda UTF-16 karakter dizisi. Bu, yazı tipinin ad tablosunda bulunan İngilizce sürüm dizesidir (ad kimliği = 5) - Bkz. https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding4|Padding değeri her zaman 0x0000 olarak ayarlanmalıdır.|
|unsigned short|FullNameSize|FullName tarafından kullanılan bayt sayısı|
|bayt|TamAdı[TamAdıBoyutu]|TamAdıBoyutu bayt uzunluğunda UTF-16 karakter dizisi. Bu, yazı tipinin ad tablosunda bulunan İngilizce tam ad dizesidir (ad kimliği = 4) - Bkz. https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding5|Padding değeri her zaman 0x0000 olarak ayarlanmalıdır.|
|unsigned short|RootStringSize|RootString dizisi tarafından kullanılan bayt sayısı|
|byte|RootString[RootStringSize]|RootStringSize bayt uzunluğunda UTF-16 karakter dizisi.|
|unsigned long|RootStringCheckSum|RootString CheckSum değeri. Aşağıdaki RootStringChecksum'u işlemek için algoritmaya bakın.|
|unsigned long|EUDCCodePage|EUDC yazı tipi desteği için kod sayfası değeri gerekiyor.|
|unsigned short|Padding6|Padding değeri her zaman 0x0000 olarak ayarlanmalıdır.|
|unsigned short|SignatureSize|Signature dizisi tarafından kullanılan bayt sayısı. Şu anda rezerve edilmiştir ve 0x0000 olarak ayarlanmalıdır.|
|bayt|İmza[İmzaBoyutu]|Şu anda rezerve edilmiştir. SignatureSize 0x0000 ise, bu dizinin uzunluğu yoktur.|
|unsigned long|EUDCFlags|EUDC yazı tipi için işaretler işleniyor. Tipik değerler TTEMBED_XORENCRYPTDATA ve TTEMBED_TTCOMPRESSED olabilir.|
|unsigned long|EUDCFontSize|Signature dizisi tarafından kullanılan bayt sayısı.|
|bayt|EUDCFontData[EUDCFontSize]|EUDC yazı tipi verileri için kullanılan bayt sayısı. EUDCFontSize 0x00000000 ise, bu dizinin uzunluğu yoktur.|
|bayt|FontData[FontDataSize]|Bu EOT dosyası için yazı tipi verileri. Veriler, işleme bayraklarının gösterdiği şekilde sıkıştırılabilir veya XOR ile şifrelenebilir.|

## Referanslar

* [EOT Dosya Biçimi](https://www.w3.org/Submission/EOT/)
* [Gömülü OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [Yazı Tipi Gömme](https://en.wikipedia.org/wiki/Font_embedding)

