{
  "date" : "2021-10-20",
  "keywords" :[ "bns dosyası", "bns dosya biçimi", "bns dosyası nedir", "dosya", "bns örneği", "Portal Bonus Map Script dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Oral Bonus Map Script BNS dosya formatı ve BNS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"BNS - Portal Bonus Haritası Komut Dosyası",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## .BNS dosyası nedir?

.bns uzantılı bir dosya, Valve tarafından geliştirilen Portal Haritası bulmaca çözme oyunu ile oluşturulan bir oyun komut dosyasıdır. .bsp dosyası olarak saklanan bir Portal haritası hakkında bilgi tanımlamak için metin komut dosyası içerir. BNS dosyaları, bu gerçek harita dosyasına referans olarak kullanılır ve tamamlanması gereken zorlukların bir listesini içerir. Ayrıca harita adını, harita hakkında yorumları ve küçük resim dosyası referanslarını içerir. Bir BNS dosyası, Notepad++, textEdit ve Notepad gibi herhangi bir metin düzenleyicide açılabilir.

## BNS Dosya Biçimi

BNS dosyaları, insan tarafından okunabilen düz metin dosyaları olarak kaydedilir. Bunlar metin editörlerinde açılabilir ve düzenlenebilir. Ancak, komut dosyasında herhangi bir hata oluşmasını önlemek için bunlar dikkatlice düzenlenmelidir.

## BNS Dosya Biçimi Örneği

Bir BNS dosyası, Notepad++ gibi bir metin düzenleyicide açıldığında aşağıdaki gibi görünebilir.

```
"#Bonus_Map_Challenges"
{
	"map"		"testchmb_a_08"
	"chapter"	"chapter5.cfg"	[$X360]
	"image"		"bonusmaps/testchmb_a_08_challenges"
	"comment"	"#Bonus_Map_ChallengesComment"
	"lock"		"0"

	"challenges"
	{
		"#Bonus_Map_ChallengePortals"
		{
			"comment"	"#Bonus_Map_LeastPortalsComment"

			"bronze"	"9"
			"silver"	"5"
			"gold"		"4"
		}
		"#Bonus_Map_ChallengeSteps"
		{
			"comment"	"#Bonus_Map_LeastStepsComment"

			"bronze"	"30"
			"silver"	"20"
			"gold"		"10"
		}
		"#Bonus_Map_ChallengeTime"
		{
			"comment"	"#Bonus_Map_LeastTimeComment"

			"bronze"	"40"
			"silver"	"30"
			"gold"		"19"
		}
	}
}
```

## BNS Dosyasının Parçaları

Yukarıdaki örnekte,

* `#Bonus_Map_Challenges` - Haritanın adını temsil eder.
* `map` - Oyunun haritalar klasörüne konulacak haritanın adını temsil eder
* `bölüm` - Haritanın ait olduğu bölümü temsil eder. Tüm bölüm dosyaları, haritanın adını 'map your_map_name' biçiminde ekleyerek VPK dosyasında bulunur.
* `Resim` - Haritanın küçük resmini içerir ve steam\steamapps\common\portal\portal\materials\VGUI kök yolunda saklanır.
* `Yorum` - Oluşturulan harita hakkında açıklayıcı metin.

## Referanslar

* [Portal Mücadelesi Komut Dosyası](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

