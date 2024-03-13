{
  "date": "2019-10-11",
  "keywords": [
"mpkg faylı",
"mpkg fayl formatı",
"mpkg faylı nədir",
"fayl",
"mpkg nümunəsi",
"mpkg fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MPKG Fayl Format - Meta Paket Faylı",
  "description": "MPKG faylları yarada və aça bilən MPKG fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "MPKG",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-mpk-azg"
}
},
  "lastmod": "2021-04-02"
}

## MPKG faylı nədir?

.mpkg uzantılı fayl, əsasən MacOS Əməliyyat Sistemlərində tapılan arxiv quraşdırıcı fayldır. Bu, əlaqəli faylları ayrıca saxlamağa ehtiyac olmadan tətbiqin bütün tələb olunan quraşdırma fayllarını ehtiva edir. Tək MPKG faylı digər fayllara əlavə olaraq quraşdırma fayllarından biri kimi [PKG](/compression/pkg/) paket fayllarını ehtiva edə bilər. MPKG faylları heç bir ümumi proqram təminatı ilə açıla bilməz və Apple Installer istifadə edərək MacOS-da avtomatik olaraq icra olunur.

## MPKG fayl formatı

MPKG faylı tərkibində olan çoxsaylı paketlərin quraşdırılması üçün tələb olunan müxtəlif növ faylları ehtiva edir. Bu, nümunə MPKG faylının ağac quruluşu olan aşağıdakı şəkildən görünə bilər. Bu ağac strukturu MacOS terminalında ağac” əmrindən istifadə etməklə ixrac edilir.

{{< figure src="../mpkg.png" alt="MPKG fayl formatı" >}}

The description of different elements in the image is as follow.

`Paketlər kataloqu` - pkg fayllarının siyahısını, yəni alt paketlərin siyahısını saxlayır.
`Resources Directory` - pkg tərəfindən istifadə olunan resursları, məsələn, lokallaşdırılmış resurslar və şəkillər, RTF sənədləri, pdf sənədləri və s.
`Distribution.dist faylı` - Quraşdırılacaq alt paketlər və icra müddəti skriptləri kimi məlumatları ehtiva edən xml sənədi

MPKG faylı üçün nümunə XML faylı əlaqəli alt paketlərdən asılı olaraq aşağıdakı kimi görünə bilər.

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
  if(!(/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
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
`app.pkg` - quraşdırılacaq alt paketdir. Bu, Bundle strukturunun pkg formatında kataloqudur. O, Məzmun alt kataloqunu ehtiva edir.

## İstinadlar

* [OSX Flat Paketləri](https://matthew-brett.github.io/docosx/flat_packages.html)

* [C++ MPKG Paket Meneceri](https://github.com/puellavulnerata/mpkg)


