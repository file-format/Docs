{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "dosya", "uzantı", "dosya formatı", "Visual C++ Projesi", "Programlama Kılavuzu"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ",
  "description":"VCXPROJ dosya formatı ve VCXPROJ dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## VCXPROJ dosyası nedir?

.vcxproj uzantılı bir dosya, [C++](/tr/programming/cpp/) proje bilgilerini depolayan bir Microsoft Visual C++ proje dosyasıdır. Son çıktıyı derlemek ve oluşturmak için MSBuild proje sistemi tarafından kullanılan bilgileri içerir. Visual C++ projelerinin VCXPROJ'u, .NET projeleri için [CSPROJ](/tr/programming/csproj/) ile aynıdır. VCXPROJ dosyaları herhangi bir kod içermez, ancak projeyi oluşturmak için proje için tanımlanan tüm sınıfları, hedefleri ve özellikleri ifade eder. Bunlar düz metin editörlerinde veya tercihen Microsoft Visual Studio IDE'de açılabilir.


## VCXPROJ Dosya Biçimi - Daha Fazla Bilgi

VCXPROJ dosyaları, [XML](/tr/web/xml/) dosya biçiminde oluşturulan metin dosyalarıdır. Bunlar herhangi bir metin düzenleyicide açılabilir ancak bu dosyaları açmak ve düzenlemek için Microsoft Visual Studio IDE kullanılması önemle tavsiye edilir. Bunlar manuel düzenleme için tasarlanmamıştır. Hatalar, IDE'nin çökmesine veya beklenmedik şekillerde davranmasına neden olabilir.

Örnek bir VCXPROJ dosyasının içeriği aşağıdaki gibidir.

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### VCXPROJ Dosya Öğeleri

Tipik bir VCXPROJ dosyası, yukarıdaki örnek XML'de görülebileceği gibi bir dizi öğe içerir. Microsoft'un [VCXPROJ yapısı](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) her dosya öğesini ayrıntılı olarak açıklar ve başvurulabilir geliştiricinin bakış açısından.

#### Proje Elemanı

Bu, VCXPROJ dosyasının kök düğümüdür. MSBuild derleme sürümünü ve varsayılan hedefi okumak için bu öğeyi kullanır.

#### Proje Yapılandırmaları ItemGroup Öğesi

Derleme yöntemini (Hata Ayıklama veya Sürüm), 32 veya 64 bit derlemeyi, optimizasyon seçeneklerini ve diğerlerini içerebilen proje yapılandırma bilgilerini içerir. Bu gruptaki bilgiler, projeyi yüklemek için IDE tarafından kullanılır.

#### Proje Yapılandırma Öğeleri

Bir VCXPROJ dosyasındaki ProjectConfiguration öğeleri, projenin yüklendiği yapı ve platform hakkında bilgi içerir. Adı, `$(Yapılandırma)|$(Platform)` biçiminde olmalıdır.

#### Globals PropertyGroup Öğesi

Bu bölüm, aşağıdakiler gibi proje düzeyi için bilgi sağlayan ayarları içerir:

* Proje Rehberi
* RootNamespace
* ApplicationType veya ApplicationTypeRevision


## Referanslar

* [VCXPROJ Yapısı - MSDN](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [C++ Proje Dosyaları](https://learn.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

