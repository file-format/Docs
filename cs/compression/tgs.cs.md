{
  "date" : "2019-10-11",
  "keywords" :[ "soubor tgs", "formát souboru tgs", "co je soubor tgs", "soubor", "příklad tgs", "přípona souboru tgs", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGS - Telegram Animated Sticker File Format",
  "description":"Další informace o formátu souborů TGS a rozhraních API, která mohou vytvářet a otevírat soubory TGS.",
  "linktitle" : "TGS",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Co je soubor TGS?

Soubor s příponou .tgs je soubor animované nálepky, který byl představen službou pro zasílání zpráv napříč platformami, [Telegram](https://core.telegram.org/animated_stickers). Animované nálepky používají uživatelé aplikací pro zasílání zpráv k odesílání vylepšeného a živějšího obsahu ve zprávách na rozdíl od statické grafiky, kterou jsou statické obrázky. Telegram zpočátku používal formát souboru [WEBP](/cs/image/webp/) pro nálepky statických obrázků. Formát souboru TGS může ukládat data animace ve vyšším rozlišení a menší velikosti souboru ve srovnání se statickými nálepkami WEBP. Soubory TGS lze otevřít pomocí aplikací, jako je Telegram, 7-zip, Apple Archive Utility a Corel WinZip.

## Formát souboru TGS

Telegram představil formát souboru TGS již v červenci 2019 na základě knihovny Lottie. Soubor TGS se skládá z textu [JSON](/cs/web/json/), který je exportován z animace v Adobe After Effects. Exportovaný text JSON je komprimován pomocí komprese gzip, která snižuje velikost souboru. Informace JSON o textovém souboru jsou uloženy v textovém souboru, který se stává základem vysokých kompresních poměrů.

### Specifikace samolepek TGS

Formát souboru TGS ukládá určitá omezení při vytváření animovaných nálepek TGS. Animovaný soubor TGS:

* Velikost nálepky/plátna musí být 512 × 512 pixelů.
* Nálepkové předměty nesmí opustit plátno.
* Délka animace nesmí přesáhnout 3 sekundy.
* Všechny animace musí být ve smyčce.
* Velikost nálepky po vykreslení v Bodymovin nesmí přesáhnout 64 kB.
* Všechny animace musí běžet rychlostí 60 snímků za sekundu.

### Ukázkový text TGS JSON

Ukázková animovaná nálepka po rozbalení obsahuje následující textový obsah JSON.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## Reference ##

* [TGS](https://core.telegram.org/animated_stickers)
* [gzip – Wikipedia](https://en.wikipedia.org/wiki/Gzip)

