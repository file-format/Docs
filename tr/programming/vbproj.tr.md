{
  "date" : "2019-10-11",
  "keywords" :[ "vbproj", "dosya", "uzantı", "dosya formatı", "VB Proje Dosyası", "Programlama Kılavuzu"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBPROJ",
  "description":"VBPROJ dosya formatı ve VBPROJ dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "VBPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## VBPROJ dosyası nedir?

.vbproj uzantılı bir dosya, Microsoft'un MSBuild motoru tarafından bir Visual Studio çözümü içindeki projeleri oluşturmak için kullanılan bir Microsoft Visual Basic proje dosyasıdır. [C#](/tr/programming/cs/) ile yazılmış .NET projeleri için [CSPROJ](/tr/programming/csproj/) dosyasına benzer. MSBuild altyapısı, VBPROJ dosyalarından farklı gruplarda bulunan bilgileri okur ve çıktı dosyasını oluşturur. Bir VBPROJ dosyası, projeyi tanımlayan genel tanımlayıcılar, sınıflar ve özelliklerle ilgili bilgileri içerebilir. VBPROJ dosyaları, Microsoft Visual Studio ve Windows ve MacOS İşletim Sistemlerinde Not Defteri gibi herhangi bir yaygın metin düzenleyici kullanılarak açılabilir ve düzenlenebilir.

## VBPROJ Dosya Biçimi - Daha Fazla Bilgi

VBPROJ dosyaları, [MSBuild XML Şeması](https://docs.microsoft.com/en-us/visualstudio/msbuild/msbuild-) temelinde [XML](/tr/web/xml/) dosya biçiminde yazılmış metin dosyalarıdır. proje-dosya-şema referansı?view=vs-2019). Bir VBPROJ dosyası, belirli bir ayar grubuyla ilgili bilgileri tanımlayan XML etiketleri biçiminde bilgiler içerir. Bu ayar dosyalarının Microsoft Visual Studio IDE'de açılması ve düzenlenmesi önemle tavsiye edilir.

### VBPROJ Öğeleri

Bir VB Settings dosyasını oluşturan öğeler aşağıdaki görüntüde gösterildiği gibidir.

{{< figure src="../vbproj.png" alt="VBPROJ Dosya Biçimi" >}}

Aşağıdaki tabloda bu öğelerin kısa bir açıklaması verilmektedir.

|Öğe|Açıklama|
---|---|
|Proje| Her proje dosyasının kök öğesidir ve proje dosyası için tanımlayıcı XML şemasına ek olarak oluşturma işlemi için giriş noktalarını belirtmek için öznitelikler içerebilir|
|Özellikler ve Koşullar| Özellikler, Anahtar/değer çiftlerinden oluşur ve bir PropertyGroup öğesi içinde tanımlanır. Özellik öğesi adı, özellik anahtarını temsil eder ve öğenin içeriği, özellik değerini tanımlar.|
|Öğeler ve ÖğeGrupları|Bir proje dosyasındaki öğeler, dosya-kod dosyaları, yapılandırma dosyaları, komut dosyaları ve oluşturma sürecinin bir parçası olarak gerekli olan diğerleri gibi derleme sürecinin girdileridir. Öğeler, bir ItemGroup öğesi içinde tanımlanır ve tanımlanmalıdır.|
|Hedefler ve Görevler| Görev öğesi, bireysel bir yapı talimatını (veya görevini) temsil eder. MSBuild, Copy, CSC, VBC, Exec gibi çok sayıda önceden tanımlanmış görev içerir. Görevler her zaman sırayla yürütülen bir veya daha fazla görev kümesi olan bir "Hedef" Öğesinde yer almalıdır ve bir proje dosyası birden çok hedef içerebilir.|

## Referanslar

* [Proje Dosyasını Anlama](https://docs.Microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)
* [MSBuild Şema Öğeleri](https://docs.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)

