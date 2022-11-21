{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "amf dosyası", "amf dosya biçimi", "dosya biçimi", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"AMF dosya formatı ve AMF dosyalarını açıp oluşturabilen API'ler hakkında bilgi edinin.",
  "title" :"AMF - Eklemeli İmalat Dosyası",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Bir AMF dosyası nedir?
Bir AMF dosyası, Katmanlı Üretim süreçlerinde kullanılmak üzere nesnelerin tanımına yönelik yönergelerden oluşur. Bir açılış içerir<amf> XML etiketi ve bir ile biter</amf> eleman. Bunun öncesinde, dosyanın XML sürümünü ve kodlamasını belirten bir XML bildirim satırı bulunur. Beyannameler ölçü birimi bilgilerini içerebilir ve bu tür bilgilerin olmaması durumunda varsayılan birim olarak milimetre kullanılır.


## AMF Dosya Biçimi

Eklemeli Üretim dosya formatı (**AMF**), 3B Yazdırma gibi eklemeli üretim süreçlerinde kullanılmak üzere nesne açıklaması için açık standartlar tanımlar. CAD programları, nesnelerin geometri, renk ve malzeme gibi bilgilerinden yararlanarak AMF dosya formatını kullanır. AMF, yanal renk, malzeme, kafes ve takımyıldızları desteklemediği için STL formatından farklıdır.

### Bir AMF Dosyasının Öğeleri

ile tanımlanan beş üst düzey öğe<AMF> etiketler aşağıda ayrıntılı olarak verilmiştir. Tek bir nesne öğesinin varlığı, tamamen işlevsel bir AMF dosyası için şarttır.

`<object> ` - Nesne öğesi, her biri yazdırma için bir malzeme kimliğiyle ilişkilendirilmiş bir malzeme hacmini veya hacimlerini tanımlar. Dosyada en az bir nesne öğesi bulunmalıdır. Ek nesneler isteğe bağlıdır.

`<material> ` - İsteğe bağlı malzeme öğesi, ilişkili bir malzeme kimliğiyle yazdırılacak bir veya daha fazla malzemeyi tanımlar. Hiçbir malzeme unsuru dahil edilmezse, tek bir varsayılan malzeme olduğu varsayılır.

`<texture> ` - İsteğe bağlı doku öğesi, renk veya doku eşleme için her biri ilişkili bir doku kimliğine sahip bir veya daha fazla görüntü veya doku tanımlar.

`<constellation> ` - İsteğe bağlı takımyıldız öğesi, nesneleri ve diğer takımyıldızları yazdırmak için göreli bir modelde hiyerarşik olarak birleştirir.

`<metadata> ` - İsteğe bağlı meta veri öğesi, dosyada bulunan nesne(ler) ve öğeler hakkında ek bilgileri belirtir.

## AMF Örneği

Aşağıda, bir [text](/tr/word-processing/txt/) dosyasına kopyalanabilen ve açmak için sıkıştırılmış [zip](/tr/compression/zip/) dosyası olarak kaydedilebilen bir AMF dosyası örneği verilmiştir.
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## Referanslar

* [AMF - Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [ISO'da AMF özellikleri](https://www.iso.org/standard/67472.html)

