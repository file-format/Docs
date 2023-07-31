{
  "date" : "2019-10-11",
  "keywords" :[ "vsdx dosyası", "vsdx dosya biçimi", "vsdx dosyası nedir", "dosya", "vsdx örneği", "vsdx dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDX",
  "description":"VSDX dosya formatı ve VSDX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "VSDX",
  "menu" : {
    "docs" : {
	"identifier":"visio-vsdx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## VSDX dosyası nedir?

.vsdx uzantılı dosyalar, Microsoft Office 2013'ten itibaren kullanıma sunulan Microsoft Visio dosya biçimini temsil eder. Microsoft Visio'nun önceki sürümleri tarafından desteklenen ikili dosya biçimi [.VSD](/tr/image/vsd/)'nin yerini almak üzere geliştirilmiştir. Ayrıca Microsoft SharePoint Server 2013'teki Visio Hizmetlerinde desteklenir ve SharePoint Server'da yayınlamak için bir aracı dosya formatı gerektirmez. Visio dosyaları, görsel nesneler, akış şemaları, UML diyagramı, bilgi akışı, organizasyon şemaları, yazılım diyagramları, ağ düzeni, veritabanı modelleri, nesne eşleme ve benzeri bilgileri içeren çizimler oluşturmak için kullanılır. Visio kullanılarak oluşturulan dosyalar, [PNG](/tr/image/png/), [BMP](/tr/image/bmp/), [PDF](/tr/pdf/) ve diğerleri gibi farklı dosya biçimlerine de aktarılabilir.

## Dosya formatı ##

VSDX dosyaları, Açık Paketleme Kurallarına ve XML'e dayalıdır ve geliştiriciler, bu dosyalarla programlı olarak nasıl çalışacaklarını öğrenerek bu biçimden yararlanabilirler. Biçim, parçalarıyla aynı XML yapılarının çoğunu Visio XML Çizim dosya biçiminden (.vdx) devralır. Visio dosyalarıyla birlikte çalışabilirlik, üçüncü taraf yazılımlar Visio dosyalarını dosya formatı düzeyinde işleyebildiğinden büyük ölçüde artar.

Visio 2013 dosya biçimini oluşturan diğer bazı dosya türleri şunları içerir:

* .vsdm (Visio makro özellikli çizim)
* .vssx (Visio kalıbı)
* .vssm (Visio makro özellikli şablon)
* .vstx (Visio şablonu)
* .vstm (Visio makro özellikli şablon)

Görünüşte, Visio 2013 dosya formatı, uygulama verilerini ilgili kaynaklarla birlikte [ZIP](/tr/compression/zip/) gibi bir arşivde depolamak için yapılandırılmış bir araç kullanır. ZIP dosyası, diğer dosya türlerini de içeren herhangi bir standart çıkarma yardımcı programı kullanılarak çıkarılabilir. VSDX dosyasının içeriğini görmek için Windows explore'da .vsdx dosya uzantısını .zip ile değiştirebilirsiniz.

Her Visio dosyası, diğer dosyaları veya parçaları tutan paket olarak adlandırılır. Bir paket parçası, bir XML dosyası, bir görüntü veya hatta bir VBA çözümü olabilir. Paket içindeki parçalar, "belge" ve "ilişki" bölümlerine ayrılabilir.

### Belge ###

Belge bölümleri, dosya adı, ilk sayfa ve içerdiği tüm şekiller ve hatta şekiller için veri bağlantıları gibi Visio dosyasının gerçek içeriğini ve meta verilerini içerir. Paket içindeki resimler ve metin dosyaları, belge parçaları olarak kabul edilir.

### ilişkiler ###

Bir Visio dosyasının ilişki bölümleri "\_rels" klasöründe saklanır ve paket içindeki bölümlerin birbiriyle nasıl ilişkili olduğunu açıklar. Ayrıca dosyanın yapısını da sağlar. Bağımsız bir XML belgesi, varlıkların birbiriyle ilişkisini belirlemek için öğelerin üst/alt ilişkisini kullanır. Geçerli bir Visio 2013 dosya biçimi, doğru parça kümesini içerir ve paket, parçalar arasındaki ilişkileri içerir.

İlişki bölümleri, paket içindeki farklı belge bölümleri arasındaki ilişkileri açıklayan XML belgeleridir. İki öğe arasında bir ilişki tanımlarlar: belirli bir kaynak (ilişki dosyasının adı ve konumu ile tanımlanır) ve belirtilen bir hedef belge parçası. Örneğin, ilişki bölümleri dosyayla hangi şekil kalıplarının ilişkilendirildiğini, sayfaların dosyayla ve birbirleriyle nasıl ilişkili olduğunu veya görüntülerin ve nesnelerin belirli bir sayfayla nasıl ilişkili olduğunu açıklamak için kullanılır.

## Referanslar ##

* [Visio Dosya Biçimine Giriş](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

