{
  "date" : "2019-10-11",
  "keywords" :[ "vstx dosyası", "vstx dosya biçimi", "vstx dosyası nedir", "dosya", "vstx örneği", "vstx dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTX - Microsoft Visio Dosya Biçimi",
  "description":"VSTX dosya formatı ve VSTX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "VSTX",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## VSTX dosyası nedir?

.vstx uzantılı dosyalar, Microsoft Visio 2013 ve üzeri ile oluşturulan çizim şablon dosyalarıdır. Bu VSTX dosyaları, varsayılan düzen ve ayarlarla [.VSDX](/tr/image/vsdx/) dosyaları olarak kaydedilen Visio çizimleri oluşturmak için başlangıç noktası sağlar. Genel olarak Visio dosyaları, görsel nesneler, akış şemaları, UML diyagramı, bilgi akışı, organizasyon şemaları, yazılım diyagramları, ağ düzeni, veritabanı modelleri, nesne eşleme ve benzeri bilgileri içeren çizimler oluşturmak için kullanılır. Visio kullanılarak oluşturulan dosyalar, [PNG](/tr/Image/PNG/), [BMP](/tr/image/bmp/), [PDF](/tr/pdf/) ve diğerleri gibi farklı dosya biçimlerine de aktarılabilir. VSTX dosyalarını açan programlar, bu dosyaları görüntülemek ve düzenlemek için açmanıza izin veren Windows ve Mac için Microsoft Visio'yu içerir. Ayrıca Visio dosya biçimlerinin bir dizi başka biçime dönüştürülmesine de olanak tanır.

# VSTX Dosya Biçimi #

Dosya uzantısındaki "X", Microsoft tarafından daha önce desteklenen ikili dosya biçimlerinin yerine [ZIP](/tr/compression/zip/) arşiv dosyası biçimi olarak sunulan OpenOffice dosya biçimini ifade eder. Bu nedenle VSTX dosyaları, ikili biçimdeki [.VST](/tr/image/vst/) dosya biçiminin aksine OpenOffice belirtimlerinin XML dosya biçimini temel alır.

VSDX dosyaları, Açık Paketleme Kurallarına ve XML'e dayalıdır ve geliştiriciler, bu dosyalarla programlı olarak nasıl çalışacaklarını öğrenerek bu biçimden yararlanabilirler. Biçim, parçalarıyla aynı XML yapılarının birçoğunu Visio XML Çizim dosya biçiminden (.vdx) devralır. Visio dosyalarıyla birlikte çalışabilirlik, üçüncü taraf yazılımlar Visio dosyalarını dosya formatı düzeyinde işleyebildiğinden büyük ölçüde artar.

Visio 2013 dosya biçimini oluşturan diğer bazı dosya türleri şunları içerir:

* .vsdm (Visio makro özellikli çizim)
* .vssx (Visio kalıbı)
* .vssm (Visio makro özellikli şablon)
* .vstx (Visio şablonu)
* .vstm (Visio makro özellikli şablon)

Görünüşte, Visio 2013 dosya formatı, uygulama verilerini ilgili kaynaklarla birlikte [ZIP](/tr/compression/zip/) gibi bir arşivde depolamak için yapılandırılmış bir araç kullanır. ZIP dosyası, diğer dosya türlerini de içeren herhangi bir standart çıkarma yardımcı programı kullanılarak çıkarılabilir. VSTX dosyasının içeriğini görmek için Windows explore'da .VSTX dosya uzantısını .ZIP ile değiştirebilirsiniz.

Her Visio dosyası, diğer dosyaları veya parçaları tutan paket olarak adlandırılır. Bir paket parçası, bir XML dosyası, bir görüntü veya hatta bir VBA çözümü olabilir. Paket içindeki parçalar, "doküman" ve "ilişki" bölümlerine ayrılabilir.

### Belge ###

Belge bölümleri, dosya adı, ilk sayfa ve içerdiği tüm şekiller ve hatta şekiller için veri bağlantıları gibi Visio dosyasının gerçek içeriğini ve meta verilerini içerir. Paket içindeki resimler ve metin dosyaları, belge parçaları olarak kabul edilir.

### ilişkiler ###

Bir Visio dosyasının ilişki bölümleri "_rels" klasöründe saklanır ve paket içindeki bölümlerin birbiriyle nasıl ilişkili olduğunu açıklar. Ayrıca dosyanın yapısını da sağlar. Bağımsız bir XML belgesi, varlıkların birbiriyle ilişkisini belirlemek için öğelerin üst/alt ilişkisini kullanır. Geçerli bir Visio 2013 dosya biçimi, doğru parça kümesini içerir ve paket, parçalar arasındaki ilişkileri içerir.

İlişki bölümleri, paket içindeki farklı belge bölümleri arasındaki ilişkileri açıklayan XML belgeleridir. İki öğe arasında bir ilişki tanımlarlar: belirli bir kaynak (ilişki dosyasının adı ve konumu ile tanımlanır) ve belirtilen bir hedef belge parçası. Örneğin, ilişki bölümleri dosyayla hangi şekil kalıplarının ilişkilendirildiğini, sayfaların dosyayla ve birbirleriyle nasıl ilişkili olduğunu veya görüntülerin ve nesnelerin belirli bir sayfayla nasıl ilişkili olduğunu açıklamak için kullanılır.

## Referanslar ##

* [Visio Dosya Biçimine Giriş](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

