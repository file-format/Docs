{
  "date": "2019-10-11",
  "keywords": [
"amf",
"amf faylı",
"amf fayl formatı",
"fayl formatı",
"3d"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "AMF fayl formatı və AMF fayllarını aça və yarada bilən API-lər haqqında məlumat əldə edin.",
  "title": "AMF - Əlavə İstehsalat Faylı",
  "linktitle": "AMF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-am-azf"
}
},
  "lastmod": "2019-09-10"
}

## AMF faylı nədir?
An AMF file consists of guidelines for objects description in order to be used by Additive Manufacturing processes. It contains an opening <amf> XML tag and ends with a </amf> element. This is preceded by an XML declaration line specifying the XML version and encoding of the file. The declarations can include measurement units information and, in the absence of such information, millimetres are used as default unit.


## AMF fayl formatı

Additive Manufacturing file format (**AMF**) defines open standards for objects description in order to be utilized by additive manufacturing processes such as 3D Printing. CAD programs use the AMF file format by making use of the information such as geometry, color and material of the objects. AMF is different than STL format as the lateral does not support color, materials, lattices, and constellations.

### AMF faylının elementləri

ilə müəyyən edilmiş beş üst səviyyə element<AMF> etiketlər aşağıda ətraflı şəkildə göstərilmişdir. Tam funksional AMF faylı üçün tək obyekt elementinin olması şərtdir.

`<object> ` - Obyekt elementi materialın həcmini və ya həcmlərini müəyyən edir, onların hər biri çap üçün material identifikatoru ilə əlaqələndirilir. Faylda ən azı bir obyekt elementi olmalıdır. Əlavə obyektlər isteğe bağlıdır.

`<material> ` - Əlavə material elementi əlaqəli material ID ilə çap üçün bir və ya bir neçə materialı müəyyən edir. Heç bir maddi element daxil edilməyibsə, tək standart material nəzərdə tutulur.

`<texture> ` - İsteğe bağlı tekstura elementi rəng və ya faktura xəritələşdirilməsi üçün bir və ya bir neçə şəkil və ya tekstura müəyyən edir, hər biri əlaqəli tekstura ID-si ilə.

`<constellation> ` - Əlavə bürc elementi iyerarxik olaraq obyektləri və digər bürcləri çap üçün nisbi nümunədə birləşdirir.

`<metadata> ` - Əlavə metadata elementi faylda olan obyekt(lər) və elementlər haqqında əlavə məlumatı təyin edir.

## AMF nümunəsi

Aşağıda [text](/word-processing/txt/) faylına kopyalana bilən və açmaq üçün sıxılmış [zip](/compression/zip/) faylı kimi yadda saxlanıla bilən AMF faylı nümunəsidir.
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
## İstinadlar

 * [AMF - Vikipediya](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
 * [ISO-da AMF spesifikasiyalar](https://www.iso.org/standard/67472.html)

