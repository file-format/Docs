{
  "date" : "2019-10-11",
  "keywords" :[ "potx dosyası", "potx dosya biçimi", "potx dosyası nedir", "dosya", "potx örneği", "potx dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"POTX - Microsoft PowerPoint Sunum Şablonu",
  "description":"POTX dosya formatı ve POTX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "POTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## POTX dosyası nedir?

.POTX uzantılı dosyalar, Microsoft PowerPoint 2007 ve üzeri ile oluşturulan Microsoft PowerPoint şablon sunumlarını temsil eder. Bu biçim, ikili dosya biçimini temel alan ve PowerPoint 97-2003 tarafından desteklenen [POT](/tr/sunum/pot/) dosya biçimini değiştirmek için oluşturulmuştur. Oluşturulan dosyalar, aynı düzene ve yeni dosyalara uygulanması gereken diğer ayarlara sahip sunumlar oluşturmak için kullanılabilir. Bu ayarlar stilleri, arka planları, renk paletini, yazı tiplerini ve varsayılanları içerebilir. Bu tür dosyalar, resmi kullanım için kullanıma hazır şablon dosyaları oluşturmak için oluşturulur.

## Kısa Tarih ##

Microsoft, **Office Açık XML** standardına uymak için değişikliğe gitmeye karar verdiğinde 2000 yılının başlarındaydı. Bu yeni Standart kapsamındaki farklı türdeki belgeler, uzantılarına "X" eklenerek tanımlandı; burada "X" XML içindir. 2007 yılına gelindiğinde, bu yeni dosya biçimi Office 2007'nin bir parçası oldu ve Microsoft Office'in yeni sürümlerinde de sürdürülüyor. Yeni dosya türü, küçük dosya boyutları, daha az bozulma değişikliği ve iyi biçimlendirilmiş görüntülerin temsili gibi avantajlar ekledi.

## Dosya Biçimi Özellikleri ##

Ofis Açık XML dosya biçimiyle oluşturulan dosyalar, tüm kurucu dosyalar arasında bağlantılar sağlayan diğer dosyalarla birlikte bir XML dosyaları koleksiyonudur. Bu koleksiyon aslında içeriğini görüntülemek için çıkarılabilen sıkıştırılmış bir arşivdir. Bunu yapmak için, POTX dosya uzantısını zip ile yeniden adlandırın ve içeriğini gözlemlemek için ayıklayın.

Aşağıdaki bölümler, bunların her birine biraz ışık tutmaktadır.

### [Content_Types].xml ###

Bu, zip çıkarıldığında temel düzeyde bulunan tek dosyadır. Paket içindeki parçalar için içerik türlerini listeler. Pakete dahil edilen XML dosyalarına yapılan tüm referanslara bu XML dosyasında atıfta bulunulur. Slayt bölümü için içerik türü aşağıdadır:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Pakete yeni parçaların eklenmesi gerekiyorsa, bu, yeni parça eklenerek ve .rels dosyalarındaki tüm ilişkiler güncellenerek yapılabilir. Böyle bir değişiklik için Content_Types.xml dosyasının da güncellenmesi gerektiği unutulmamalıdır.

### \_rels (Klasör) ###

Diğer parçalar ile paketin dışındaki kaynaklar arasındaki ilişkiler, ilişkiler bölümü tarafından sürdürülür. İlişkiler klasörü, paket düzeyindeki ilişkileri depolayan tek bir XML dosyası içerir. PPTX dosyalarının önemli bölümlerine bağlantılar bu dosyada URI'ler olarak bulunur. Bu URI'ler, her bir anahtar parçanın paketle olan ilişkisinin türünü tanımlar. Bu, ppt/sunum.xml olarak bulunan birincil ofis belgesiyle ve çekirdek ve genişletilmiş özellikler olarak docProps içindeki diğer parçalarla olan ilişkiyi içerir.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Bir veya daha fazla ilişkinin kaynağı olan belgenin her bir parçası, kendi ilişkiler bölümüne sahip olacaktır; bu tür her bir ilişki parçası, parçanın bir \_rels alt klasöründe bulunur ve adın sonuna '.rels' eklenerek adlandırılır. Bölüm. Ana içerik bölümü (sunum.xml) kendi ilişkiler bölümüne (sunum.xml.rels) sahiptir. Dış bağlantılar için URI'lerin yanı sıra slideMaster1.xml, noteMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml gibi içeriğin diğer bölümleriyle ilişkileri içerir.

#### Açık İlişki ####

Açık bir ilişki için, bir kaynağın Id özniteliği kullanılarak bir kaynağa başvurulur.<Relationship> öğe. Yani, kaynaktaki Kimlik, hedefe açık bir referansla doğrudan bir ilişki öğesinin Kimliği ile eşlenir.

Örneğin, bir slayt aşağıdaki gibi bir köprü içerebilir:
```
<a:hlinkClick r:id#"rId2">
```
r:id#"rId2", slaydın (slide1.xml.rels) ilişkiler bölümünde aşağıdaki ilişkiye atıfta bulunur.
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Örtük İlişki ####

Örtülü bir ilişki için, bir `a böyle doğrudan bir referans yoktur.<Relationship> kimliği. Bunun yerine, referans anlaşılır.

### ppt Klasörü ###

Bu, Sunum içeriğiyle ilgili tüm detayları içeren ana klasördür. Varsayılan olarak, aşağıdaki klasörlere sahiptir:

* \_rels
* tema
* slaytlar
* slayt Düzenleri
* SlideMaster'lar

ve aşağıdaki xml dosyaları:

* sunum.xml
*presProps.xml
* tabloStyles.xml
* viewProps.xml

## Referanslar ##

* [[MS-PPTX] - PPTX Dosya Biçimi](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

