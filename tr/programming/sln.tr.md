{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"SLN dosya formatı ve SLN dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## SLN dosyası nedir?
.SLN uzantılı bir dosya, projelerin organizasyonuyla ilgili bilgileri bir çözüm dosyasında tutan bir **Visual Studio çözümü** dosyasını temsil eder. Böyle bir çözüm dosyasının içeriği, dosyanın içinde düz metin olarak yazılır ve dosya herhangi bir metin düzenleyicide açılarak gözlemlenebilir/düzenlenebilir. Bir çözüm dosyasında yer alan bilgiler kalıcı kalır ve [projeler ](/tr/programming/csproj/) gibi çözümle ilişkili bilgileri ve diğer gerekli bilgileri yüklemek için kullanılır. Çözüm dosyası tarafından başvurulan proje dosyaları, ortamın bu projenin öğeleriyle hiyerarşiyi doldurmasını sağlamak için ek bilgiler içerir. .sln dosyasında hiçbir veri saklanmaz, ancak gerekirse proje bilgileri .sln dosyasına yazılabilir.

## **SLN Sürüm Geçmişi** ##

Çözüm biçimi sürümü, her bir Microsoft Visual Studio çözümüyle birlikte zaman geçtikçe gelişmiştir. Bunlarla ilgili detaylar aşağıdaki gibidir.


|Visual Studio Sürümü|Çözüm Biçimi Sürümü
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Çözüm Dosyasının İçeriği** ###

Bir çözüm dosyası, projeyi yüklemek için ortam tarafından okunan birkaç bölümden oluşur. Örnek bir .sln dosyası içeriği aşağıda gösterildiği gibidir.

```
Project("{F184B08F-C81C-45F6-A57F-5ABD9991F28F}") # "Project1", "Project1.vbproj", "{8CDD8387-B905-44A8-B5D5-07BB50E05BEA}"  
EndProject  
Global  
  GlobalSection(SolutionNotes) # postSolution  
  EndGlobalSection  
  GlobalSection(SolutionConfiguration) # preSolution  
       ConfigName.0 # Debug  
       ConfigName.1 # Release  
  EndGlobalSection  
  GlobalSection(ProjectDependencies) # postSolution  
  EndGlobalSection  
  GlobalSection(ProjectConfiguration) # postSolution  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.ActiveCfg # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.Build.0 # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.ActiveCfg # Release|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.Build.0 # Release|x86  
  EndGlobalSection  
  GlobalSection(ExtensibilityGlobals) # postSolution  
  EndGlobalSection  
  GlobalSection(ExtensibilityAddIns) # postSolution  
  EndGlobalSection  
EndGlobal
```

### **Proje Beyanı** ###

Bir çözüm dosyası birden fazla proje bildirimi ve farklı proje türleri içerebilir. Örneğin, tek bir çözüm dosyası bir CSharp'ın yanı sıra bir VB.NET projesi içerebilir. Bu türler, [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs) kullanılarak bir çözümde ayırt edilir. Yukarıdaki proje beyanı, daha iyi anlaşılması için aşağıdaki gibi genelleştirilebilir.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Project-Type-GUID, farklı proje türleri için benzersizdir ve çözüm okuyucusu tarafından proje türünü belirlemek için kullanılır. Bu durumda F184B08F-C81C-45F6-A57F-5ABD9991F28F, bunun bir VB.NET projesi olduğunu gösterir.

`Proje GUID'i:` Projenin onu çözümdeki diğer projelerden ayıran benzersiz GUID'i. Çözümdeki bir projenin benzersiz kimliği, çözümdeki diğer projelerin ona erişmesini mümkün kılar.

.sln dosyasının proje bölümünde yer alan bilgilere bağlı olarak, ortam her bir proje dosyasını yükler. Projenin kendisi, proje hiyerarşisini doldurmaktan ve iç içe geçmiş projeleri yüklemekten sorumludur. Çözümde yapılan tüm değişiklikler, proje kaydedildiğinde veya kapatıldığında çözüm dosyasına geri kaydedilir.

## Visual Studio çözümü VS projesi

**Proje:** Mantıksal olarak, Visual Studio'yu kullanarak bir uygulama veya yazılım oluşturmaya başladığınızda yeni bir proje başlatmış olursunuz. Bir proje, çalıştırılabilir bir uygulama, web sitesi veya kitaplık olarak derlenecek kaynak kodu, simgeler, resimler, veri dosyaları ve daha fazlası gibi gerekli tüm dosyaları içerir.

**Çözüm:** Çözüm, bir veya daha fazla proje içerir. Dolayısıyla çözüm, Visual Studio projeleri için bir kapsayıcı gibidir. Mantıksal olarak, birisinin işi için bir web sitesi, masaüstü uygulaması, dinlendirici hizmet ve mobil uygulama dahil olmak üzere eksiksiz bir çözüm almak istediğini söyleyebiliriz.

### **Referanslar** ###

* [Çözüm Dosyası - MSDN Tarafından](https://learn.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [Proje Türü GUID'leri](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

