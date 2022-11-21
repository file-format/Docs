{
  "date" : "2019-10-11",
  "keywords": [ "csproj file", "csproj", "extension", "format", "What is a csproj file", "csproj file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSPROJ",
  "description":"CSPROJ dosya formatı ve CSPROJ dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CSPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## CSProj dosyası nedir?
CSPROJ uzantılı dosyalar, sistem derlemelerine yapılan başvurularla birlikte bir projeye dahil edilen dosyaların listesini içeren bir C# proje dosyasını temsil eder. Microsoft VIiual Studio'da yeni bir proje başlatıldığında, ana çözüm ([.sln](/tr/programming/sln/)) dosyasıyla birlikte bir .csproj dosyası alırsınız. Bir projede birden fazla derleme varsa, .sln dosyasının projenin bir parçası olarak hepsini birbirine bağladığı yerde eşit sayıda proje dosyası olacaktır. Bu dosyanın içeriği, dahil edilecek içerik, platform gereksinimleri, sürüm bilgileri, web sunucusu veya veritabanı sunucusu ayarları ve gerçekleştirilmesi gereken görevler gibi projeyi oluşturmak için gerekli tüm gereksinimleri tanımlar. Bir proje dosyasının içeriği, XML dosya biçiminde düzenlenir ve hem düzenleme hem de görüntüleme için herhangi bir metin düzenleyicide açılabilir. Ayrıca, uygun düzenleme için proje dosyalarına mantıklı bir görünüm verir.

## CSPROJ Dosya Biçimi #

Geliştiriciler [MSBuild XML Şemasını](https://msdn.microsoft.com/library/5dy88c2e.aspx) dikkate alarak proje dosyalarını kendileri oluşturabilirler. Proje dosyalarının açık ve şeffaf yapısı, uygulama geliştiricilerin projelerin nasıl oluşturulduğu ve konuşlandırıldığı üzerinde gelişmiş ve ince ayarlı kontroller uygulamalarını sağlar. Böyle bir proje dosyasının içerikleri arasında çok net bir ilişki vardır. Aşağıdaki şekil, böyle bir proje dosyası için temel öğeleri ve bunlar arasındaki ilişkiyi göstermektedir.

![](https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

Aşağıdaki bölümler, bir proje dosyası için dosya formatı öğelerini detaylandırır.

### Proje Elemanı ###

[Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) öğesi, her proje dosyasının kök öğesidir. Proje dosyası için XML şemasını tanımlar ve oluşturma işlemi için giriş noktalarını belirtmek üzere nitelikler içerebilir.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### Özellikler ve Koşullar

Özellikler, bir proje oluşturmak için gereken gerekli bilgileri temsil eder. Bu tür özellikler bir [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx) öğesi içinde tanımlanır. Bu özellikler, özellik öğesi adının özellik anahtarını tanımladığı ve öğenin içeriğinin özellik değerini tanımladığı anahtar-değer çiftlerinden oluşur. Örneğin, statik bir sunucu adı ve bağlantı dizesi depolamak için ServerName ve ConnectionString adlı özellikleri tanımlayabilirsiniz.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

Öğeyi değerlendirme kriterlerini belirtmek için koşullar öğeler aracılığıyla belirtilebilir. Bu, özelliği aşağıda gösterildiği gibi tanımlarken Koşul kelimesi ile belirtilir:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

MSBuild bu özellik tanımını işlerken, önce bir **$(OutputRoot)** özellik değerinin kullanılabilir olup olmadığını kontrol eder. Özellik değeri boşsa, başka bir deyişle kullanıcı bu özellik için bir değer sağlamadıysa, koşul **true** olarak değerlendirilir ve özellik değeri **..\Publish\Out.** olarak ayarlanır.

### Öğeler ve Öğe Grupları

Bir proje dosyası, aslında farklı dosya türleri olan oluşturma işlemine yönelik girdileri tanımlar. MSBuild terminolojisinde bu girdiler, Öğe öğeleri tarafından temsil edilir ve bir [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx) öğesi içinde tanımlanır. **Property** öğelerinde olduğu gibi, bir **Item** öğesini de istediğiniz gibi adlandırabilirsiniz. Ancak, öğenin temsil ettiği dosyayı veya joker karakteri tanımlamak için bir **Include** özniteliği belirtmeniz gerekir.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### Hedefler ve Görevler

Bir [Görev](https://msdn.microsoft.com/library/77f2hx1s.aspx) öğesi, ayrı bir oluşturma talimatını (veya görevini) temsil eder. MSBuild çok sayıda önceden tanımlanmış görev içerir. Örneğin:

* **Kopyala** görevi, dosyaları yeni bir konuma kopyalar.
* **Csc** görevi, Visual C# derleyicisini çağırır.
* **Vbc** görevi, Visual Basic derleyicisini çağırır.
* **Yürütme** görevi belirli bir programı çalıştırır.
* **Mesaj** görevi, bir günlükçüye bir mesaj yazar.

Görevler her zaman [Target](https://msdn.microsoft.com/library/t50z2hka.aspx) öğeleri içinde yer almalıdır. **Target** öğesi, sırayla yürütülen bir veya daha fazla görev kümesidir ve bir proje dosyası birden çok hedef içerebilir.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## Referanslar

* [Proje Dosyasını Anlama - MSDN](https://docs.Microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project- dosya)

