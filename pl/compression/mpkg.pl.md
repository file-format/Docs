{
  "date" : "2019-10-11",
  "keywords" :[ "plik mpkg", "format pliku mpkg", "co to jest plik mpkg", "plik", "przykład mpkg", "rozszerzenie pliku mpkg", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku MPKG - plik metapakietu",
  "description":"Poznaj format pliku MPKG i interfejsy API, które mogą tworzyć i otwierać pliki MPKG.",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Czym jest plik MPKG?

Plik z rozszerzeniem .mpkg to plik instalatora archiwum, najczęściej spotykany w systemach operacyjnych MacOS. Zawiera wszystkie wymagane pliki instalacyjne aplikacji bez konieczności osobnego przechowywania powiązanych plików. Pojedynczy plik MPKG może zawierać pliki pakietu [PKG](/pl/compression/pkg/) jako jeden z plików instalacyjnych oprócz innych plików. Plików MPKG nie można otwierać za pomocą żadnego ogólnego oprogramowania i są one uruchamiane automatycznie w systemie MacOS przy użyciu Apple Installer.

## Format pliku MPKG

Plik MPKG zawiera różne typy plików, które są wymagane do instalacji wielu zawartych w nim pakietów. Można to zobaczyć na poniższym obrazku, który przedstawia strukturę drzewa przykładowego pliku MPKG. Ta struktura drzewa jest eksportowana za pomocą polecenia `tree` na terminalu MacOS.

{{< figure src="../mpkg.png" alt="Format pliku MPKG" >}}

Opis różnych elementów obrazu jest następujący.

`Katalog pakietów` - przechowuje listę plików pkg, czyli listę podpakietów
`Resources Directory` - przechowuje zasoby używane przez pkg, takie jak zlokalizowane zasoby i obrazy, dokumenty Rtf, dokumenty pdf itp.
`Distribution.dist file` — dokument xml zawierający informacje, takie jak podpakiety do zainstalowania i skrypty uruchomieniowe

Przykładowy plik XML dla pliku MPKG może wyglądać następująco w zależności od powiązanych podpakietów.

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
  if(!(/pl/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
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
`app.pkg` - to podpakiet do zainstalowania. Jest to katalog struktury Bundle w formacie pkg. Zawiera podkatalog Contents.

## Bibliografia

* [Płaskie pakiety OSX](https://matthew-brett.github.io/docosx/flat_packages.html)
* [Menedżer pakietów C++ MPKG](https://github.com/puellavulnerata/mpkg)

