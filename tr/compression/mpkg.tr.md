{
  "date" : "2019-10-11",
  "keywords" :[ "mpkg dosyası", "mpkg dosya biçimi", "mpkg dosyası nedir", "dosya", "mpkg örneği", "mpkg dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPKG Dosya Biçimi - Meta Paket Dosyası",
  "description":"MPKG dosya formatı ve MPKG dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## MPKG dosyası nedir?

.mpkg uzantılı bir dosya, çoğunlukla MacOS İşletim Sistemlerinde bulunan bir arşiv yükleyici dosyasıdır. İlişkili dosyaları ayrı tutmaya gerek kalmadan uygulamanın tüm gerekli kurulum dosyalarını içerir. Tek bir MPKG dosyası, diğer dosyalara ek olarak kurulum dosyalarından biri olarak [PKG](/tr/compression/pkg/) paket dosyalarını içerebilir. MPKG dosyaları herhangi bir genel yazılımla açılamaz ve Apple Installer kullanılarak MacOS'ta otomatik olarak yürütülür.

## MPKG Dosya Biçimi

Bir MPKG dosyası, içerdiği birden fazla paketin kurulumu için gerekli olan farklı dosya türlerini içerir. Bu, örnek bir MPKG dosyasının ağaç yapısı olan aşağıdaki görüntüden görülebilir. Bu ağaç yapısı, MacOS terminalinde `tree` komutu kullanılarak dışa aktarılır.

{{< figure src="../mpkg.png" alt="MPKG Dosya Biçimi" >}}

Görüntüdeki farklı öğelerin açıklaması aşağıdaki gibidir.

`Paket Dizini` - pkg dosyalarının bir listesini, yani alt Paketlerin bir listesini saklar
"Kaynaklar Dizini" - yerelleştirilmiş kaynaklar ve resimler, Rtf belgeleri, pdf belgeleri vb. gibi pkg tarafından kullanılan kaynakları depolar.
"Distribution.dist dosyası" - Yüklenecek alt paketler ve çalışma zamanı komut dosyaları gibi bilgileri içeren bir xml belgesi

Bir MPKG dosyası için örnek XML dosyası, ilişkili alt paketlere bağlı olarak aşağıdaki gibi görünebilir.

```
<?xml version="1.0" encoding="utf-8" standalone="no"?>
<installer-script minSpecVersion="1.000000" authoringTool="com.apple.PackageMaker" authoringToolVersion="3.0.6" authoringToolBuild="201">
    <title>myframework installer</title>
    <options customize="never" allow-external-scripts="no" rootVolumeOnly="false"/>
    <installation-check script="pm_install_check();"/>
    <volume-check script="pm_volume_check();"/>
    <script>function pm_volume_check() {
  if(!(my.target.systemVersion &amp;&amp; /* &gt;= */ system.compareVersions(my.target.systemVersion.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}

function pm_install_check() {
  if(!(/tr/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}
</script>
    <choices-outline>
        <line choice="choice0"/>
    </choices-outline>
    <choice id="choice0" title="app">
        <pkg-ref id="com.macbook.myframeworkInstaller.pkg"/>
    </choice>
    <pkg-ref id="com.macbook.myframeworkInstaller.pkg" installKBytes="108" version="1.0" auth="Root">file:./Contents/Packages/app.pkg</pkg-ref>
</installer-script>
```
`app.pkg` - kurulacak alt pakettir. Bundle yapısının pkg formatındaki bir dizinidir. Bir İçindekiler alt dizini içerir.

## Referanslar

* [OSX Düz Paketleri](https://matthew-brett.github.io/docosx/flat_packages.html)
* [C++ MPKG Paket Yöneticisi](https://github.com/puellavulnerata/mpkg)

