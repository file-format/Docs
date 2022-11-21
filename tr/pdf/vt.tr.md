{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDF/VT Dosya Biçimi",
  "description":"PDF/VT dosya formatı ve PDF/VT dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "PDF/VT",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# PDF/VT nedir? #

Ağustos 2010'da [ISO 16612-2](https://www.iso.org/standard/46428.html) olarak standart olarak yayınlanan PDF/VT, çeşitli formatlarda değişken belge yazdırmayı (VDP) etkinleştirmek için tasarlanmıştır. ortamlar. Standart, Standardın temeli olarak Değişken bilgileri ve İşlemsel yazdırmayı yapar. Değişken veri yazdırma, içeriğin her alıcısı için bilgilerin bir kısmının farklı olduğu durumlarda kullanılır. İşlemsel yazdırma, fatura bilgilerini pazarlama bilgileriyle birleştiren faturaları, hesap özetlerini ve diğer belgeleri içerir. Bu, görüntülerin, metnin ve diğer içerik türlerinin gelişmiş bir şekilde işlenmesiyle sonuçlanır. PDF/VT, belge parçası meta verileri (DPM) kavramını kullanarak Yüksek Hacimli İşlem Çıktısı (HVTO) yazdırma verileri için sayfaların güvenilir ve dinamik yönetimini sağlar. PDF/VT dosyaları, başka herhangi bir bileşen eklemeye gerek kalmadan Adobe Acrobat görüntüleyicide açılabilir.

## Belge Bölümü Hiyerarşisi ##

Belge Bölümü (DPart) Hiyerarşisi, belgedeki tüm sayfaları temel alan belge parçası düğümlerinden oluşan bir ağaç yapısı gibidir. Bu ağacın öğelerine DPart düğümleri denir. Her iç düğüm, diğer DPart düğümlerini içerir ve her yaprak düğüm, bir alıcı için bir veya daha fazla sayfa belirtir. Temel olarak, DPart hiyerarşisi, bir PDF/VT dosyasındaki belgelerin sırasını ve ilişkisini veya belge parçalarını belirtir. DPart düğümlerinin ağaç yapısı, birçok alıcı için alt belgeler içerebileceğinden ve her bir belge parçası tek bir alıcının sayfalarına karşılık geldiğinden, bir PDF/VT belgesinin dahili içeriğini kolayca temsil eder. DPart hiyerarşisi, PDF/VT dosyalarında gereklidir.

## Belge Parçası Meta Verileri (DPM) ##

Belge Bölümü Meta Verisi (DPM), belge bölümü hiyerarşisindeki her bir düğümle ilişkilendirilir ve belirli bir alıcının alt belgesi ve onun bölümleri hakkında bilgi iletmek için kullanılabilir. Özellikle DPM, özellikler hakkında bilgi veya kodlanmış bir biçimde alıcılar hakkında bilgi içerebilir.

## Uygunluk Düzeyleri ##

PDF/VT, aşağıdaki üç uygunluk düzeyine göre verilir. Bunların tümü [PDF](/tr/pdf/) 1.6'ya dayanmaktadır.

* `PDF/VT-1` - PDF/X-4 tabanlıdır ve bir PDF belgesini işlemek için gereken tüm kaynakları içerir.
* `PDF/VT-2` - Çoklu dosya alışverişi için tasarlanan PDF/VT-2 belgeleri, harici çıktı amaçlarına, harici içeriklere veya her ikisine birden atıfta bulunabilir. Bir PDF/VT belgesi ve onun referans verilen tüm PDF dosyaları ve harici çıktı amaçları toplu olarak PDF/VT-2 dosya seti olarak adlandırılır. Acrobat 9 ve bu özelliği destekleyin.
* `PDF/VT-2s` - PDF/VT-2 canlı akışını destekler. Bu, verilerin bölümlere ayrılmış bölümlerinin işlenmesine izin verir.

## Referanslar ##

* [PDF/VT - Wikipedia'dan](https://en.wikipedia.org/wiki/PDF/VT)
* [ISO 16612-2 Grafik Teknolojisi](https://www.iso.org/standard/46428.html)

