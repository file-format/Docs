{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MP Dosyası - LaTeX MetaPost Dosyası",
  "description":"MP dosya formatı ve MP dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## .mp dosyası nedir?

Bir MP dosyası, resimler oluşturmak için MetaPost programlama dili tarafından oluşturulan bir vektör görüntü dosyasıdır. MP dosya biçimi kullanılarak oluşturulan vektör görüntüler, [EPS](/tr/image/eps/) (Encapsulated PostScript) dosyaları olarak kaydedilir. Ayrıca MetaPost, TeX ve Metafont çerçeveleri ile dağıtılmış olarak gelir ve bu uygulamalar tarafından kullanılan TEX ve LTX dosyalarının içinden MP dosyaları üretilebilir. MP dosyaları, çıktı EPS dosyasını işlemek için çizim ifadeleri ve matematiksel algoritmik çizim içerir. PDFTex motoru, doğrudan [PDF](/tr/pdf/) dosyaları oluşturmak için oluşturulan EPS'yi kullanabilir.

## MP Dosya Biçimi

MP dosyaları diske ikili dosyalar olarak kaydedilir ve çıktı vektör görüntü dosyası biçiminde dışa aktarıldığında EPS çıktısı oluşturur. MetaPost kullanılarak oluşturulan çizimler, teknik belgelerde ve LaTex ile oluşturulan dergi yayınlarında biçimlendirilmiş biçimde bulunur.

### MetaPost MP Dosyası Örneği

Aşağıda, [Berkeley Eductational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)'dan referans alınan ve ekranın hemen ortasının üzerinde bir ok ve "A" harfi içeren bir örnek verilmiştir. ok.

```
outputtemplate:="%j%c.mps";
beginfig(1);

z1=(0,0);
z2=(10mm,10mm);

drawarrow(z1--z2);
label.ulft(btex $A$ etex, .5[z1,z2]);

endfig;

bye
```
## Referanslar ##

* [Wikipedia'dan MetaPost](https://en.wikipedia.org/wiki/MetaPost)
* [Berkeley Eğitim Wiki'sinden lateks örnek Metapost](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

