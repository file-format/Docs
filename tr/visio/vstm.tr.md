{
  "date" : "2019-10-11",
  "keywords" :[ "vstm dosyası", "vstm dosya biçimi", "vstm dosyası nedir", "dosya", "vstm örneği", "vstm dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTM - Microsoft Visio Şablon Dosya Biçimi",
  "description":"VSTM dosya formatı ve VSTM dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "VSTM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## VSTM dosyası nedir?

VSTM uzantılı dosyalar, makroları destekleyen Microsoft Visio ile oluşturulan şablon dosyalarıdır. VSDX dosyalarının aksine, VSTM şablonlarından oluşturulan dosyalar, Visual Basic for Applications (VBA) kodunda geliştirilen makroları çalıştırabilir. Bu ayarlarla daha fazla belge oluşturmak için kullanılabilecek belgenin temel ayarlarını sağlamak için bir şablon dosyası oluşturulabilir. Visio dosyaları, görsel nesneler, akış şemaları, UML diyagramı, bilgi akışı, organizasyon şemaları, yazılım diyagramları, ağ düzeni, veritabanı modelleri, nesne eşleme ve benzeri bilgileri içeren çizimler oluşturmak için kullanılır. Visio kullanılarak oluşturulan dosyalar PNG, BMP, PDF ve diğerleri gibi farklı dosya biçimlerine de aktarılabilir.

## Dosya formatı ##

VSTM dosyaları, Açık Paketleme Kurallarına ve XML'e dayalıdır ve geliştiriciler, bu dosyalarla programlı olarak nasıl çalışacaklarını öğrenerek bu biçimden yararlanabilirler. Biçim, parçalarıyla aynı XML yapılarının birçoğunu Visio XML Çizim dosya biçiminden (.vdx) devralır. Visio dosyalarıyla birlikte çalışabilirlik, üçüncü taraf yazılımlar Visio dosyalarını dosya formatı düzeyinde işleyebildiğinden büyük ölçüde artar.

Her Visio dosyası, diğer dosyaları veya parçaları tutan paket olarak adlandırılır. Bir paket parçası, bir XML dosyası, bir görüntü veya hatta bir VBA çözümü olabilir. Paket içindeki parçalar, "doküman" ve "ilişki" bölümlerine ayrılabilir.

### Belge ###

Belge bölümleri, dosya adı, ilk sayfa ve içerdiği tüm şekiller ve hatta şekiller için veri bağlantıları gibi Visio dosyasının gerçek içeriğini ve meta verilerini içerir. Paket içindeki resimler ve metin dosyaları, belge parçaları olarak kabul edilir.

### ilişkiler ###

Bir Visio dosyasının ilişki bölümleri "_rels" klasöründe saklanır ve paket içindeki bölümlerin birbiriyle nasıl ilişkili olduğunu açıklar. Ayrıca dosyanın yapısını da sağlar. Bağımsız bir XML belgesi, varlıkların birbiriyle ilişkisini belirlemek için öğelerin üst/alt ilişkisini kullanır. Geçerli bir Visio 2013 dosya biçimi, doğru parça kümesini içerir ve paket, parçalar arasındaki ilişkileri içerir.

İlişki bölümleri, paket içindeki farklı belge bölümleri arasındaki ilişkileri tanımlayan XML belgeleridir. İki öğe arasında bir ilişki tanımlarlar: belirli bir kaynak (ilişki dosyasının adı ve konumu ile tanımlanır) ve belirtilen bir hedef belge parçası. Örneğin, ilişki bölümleri dosyayla hangi şekil kalıplarının ilişkilendirildiğini, sayfaların dosyayla ve birbirleriyle nasıl ilişkili olduğunu veya görüntülerin ve nesnelerin belirli bir sayfayla nasıl ilişkili olduğunu açıklamak için kullanılır.

## Referanslar ##

* [Visio Dosya Biçimine Giriş](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

