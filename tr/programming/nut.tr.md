{
  "date" : "2021-09-23", 
  "keywords" :[ "NUT", "dosya", "uzantı", "dosya biçimi", "NUT programlama dili", "Programlama Kılavuzu", "NUT örneği", "NUT dosya biçimi", "sincap dili", ".nut uzantı dosyası ", "NUT dosyaları" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUT - Sincap Dil Dosyası",
  "description":"NUT dosya formatı ve NUT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "NUT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-23"
}

## .nut dosyası nedir?

NUT, NUT Açık Konteyner Biçimi dosyasına atıfta bulunur. Bu NUT dosya formatı, Squirrel olarak bilinen programlama diline aittir. Daha çok gömülü sistemlerde ve video oyunlarında kullanılan, nesne yönelimli, üst düzey ve zorunlu bir programlama dilidir.

Sincap dili, boyut ve bant genişliğine göre kolayca ayarlanabilen hafif bir betik dili olarak kabul edilir. Otomatik referans sayımı ve bellekteki çöplerin yönetimi avantajını içerir.

Sincap dilinin sözdizimi, C benzeri olması ve betik dili özelliği içermesi nedeniyle geliştiricilerin ilgisini çekmektedir. Ancak yine de, bu amaç için daha popüler olan diğer programlama dillerine kıyasla oldukça az avantajı vardır.



## Kısa Tarih ##

2003 yılında Alberto Demichelis tarafından tasarlanmıştır. Ancak bu dilin kararlı sürümü 2016 yılında yayınlanmıştır. Zlib/libpng lisansı altında tasarlanmıştır. 2010 yılında lisansı değiştirilerek MİT'e devredilmiştir. Bu dil, [LUA](/tr/programming/lua/) (Programlama dili)'nin esinlenilmiş bir versiyonu olarak kabul edilir. Alberto'nun daha avantajlı hale getirmek için tasarladığı web sitesinde eski dil için bir öneri listesi var.


## Teknik özellik ##

Sincap dilinin özelliği ve özellikleri birden fazladır. Dinamik yazma kolaylığı, delegasyon özelliği, sınıfların ve arayüzlerin çeşitli kullanımlarını sağlar. Bu dilin sentaksı C dilinin sentaksı ile benzerlik göstermektedir. Enduro/X (küme uygulama sunucusu) gibi uygulamalar bu dili kullanır. Sincap video oyunları için de kullanıldığından, bunlardan bazıları OpenTTD, GTA IV vb.

Dilin kararlı sürümü 3.0.7'dir. MirthKit olarak bilinen bir araç seti, iki boyutlu oyunlar için açık kaynak ve çapraz platform sağlamak üzere Squirrel programlama dilini kullanır. Bu dilin doğası dinamiktir ve özelliklerin çoğu [Python](/tr/programming/py/), LUA vb. ile benzerdir. Ayrıca kayıt tabanlı VM'nin uygulanmasını da içerir. Squirrel'ın performansı LUA'ya kıyasla daha yavaştır.

Başka bir ".nut" uzantılı dosya türü daha vardır, bu nedenle hangi NUT dosyasına sahip olduğunuzu bulmak için dosyanın boyutuna bakmalısınız. Sincap komut dosyası NUT dosyalarının boyutu çoğunlukla 1 MB'den küçüktür, video NUT dosyalarının boyutu ise genellikle 1 MB'tan büyüktür.


## NUT Dosya Biçimi Örneği ##

```
function factorial(x)
  {
    if (x == 0) {
      return 1;
}
    else {
      return x * factorial(x-1);
}
  }
```

```

class BaseVector {
    constructor(...)
    {
      if(vargv.len() >= 3) {
        x = vargv[0];
        y = vargv[1];
        z = vargv[2];
  }
}
    x = 0;
    y = 0;
    z = 0;
  }

  class Vector3 extends BaseVector {
    function _add(other)
    {
      if(other instanceof ::Vector3)
        return ::Vector3(x+other.x,y+other.y,z+other.z);
      else
        throw "wrong parameter";
}
    function Print()
    {
      ::print(x+","+y+","+z+"\n");
}
  }

  local v0 = Vector3(1,2,3)
  local v1 = Vector3(11,12,13)
  local v2 = v0 + v1;
  v2.Print();

```

## Referans ##

* [NUT - Wikipedia'dan](https://en.wikipedia.org/wiki/Squirrel_(programming_language))



