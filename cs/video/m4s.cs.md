{
  "date" : "2022-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor M4S - Co je soubor M4S?",
  "description":"Další informace o formátu souboru M4S a rozhraních API, která mohou vytvářet a otevírat soubory M4S.",
  "linktitle" : "M4S",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-18"
}

## Co je soubor M4S?

Soubor M4S je malý segment videa, který je streamován přes internet pomocí techniky streamování **MPEG-DASH**. Obsahuje video segment ve formě binárních dat. Přijímající aplikace (obvykle webový prohlížeč nebo přehrávače médií) přehraje tyto segmenty v pořadí, v jakém byly přijaty. První segment M4S je identifikován inicializačními daty, která obsahuje. V **shrnutí** jsou soubory M4S malé jednotlivé mediální segmenty celého souboru.

## Formát souboru M4S

Soubory M4S jsou založeny na [formátu ISO Base Media File (ISOBMFF)](https://www.w3.org/TR/mse-byte-stream-format-isobmff/). Tyto malé segmenty velkého souboru lze stáhnout nezávisle přes HTTP. Pokud tedy máte velký filmový soubor [MP4](/cs/video/mp4/), lze jej streamovat pomocí techniky MPEG-DASH (Dynamic Adaptive Streaming over HTTP) jeho segmentací jako soubory segmentů M4S. Pokud je tento velký filmový soubor stažen na disk jako M4S, stáhne se více souborů M4S. Pokud jsou všechny tyto segmenty .m4s zřetězeny, vznikne kompletní hratelný soubor. Přehrávače médií nemohou soubor přehrát, pokud není u souboru k dispozici také první inicializační segment.

## O streamování MPEG-DASH

MPEG-DASH využívá techniku streamování s adaptivní bitovou rychlostí, která umožňuje streamovat vysoce kvalitní mediální obsah přes internet. To se provádí rozdělením obsahu do sekvence malých segmentů, které jsou streamovány přes HTTP. Tímto způsobem lze streamovat velké mediální soubory, jako jsou filmy, podcasty nebo živé vysílání sportovních událostí. Tyto segmenty jsou kódovány různými přenosovými rychlostmi. Přehrávače médií s podporou MPEG-DASH automaticky vyberou segment s nejvyšší bitovou rychlostí pomocí adaptačního algoritmu bitové rychlosti. Tím se zabrání zastavení nebo opětovnému ukládání událostí do vyrovnávací paměti při přehrávání.

### Open-Source API pro soubory M4S

K dispozici jsou open source API, která lze použít ke čtení a převodu souborů M4S.

* [libdash](https://github.com/bitmovin/libdash) – .NET API pro soubory M4S
* [dash.js](https://github.com/Dash-Industry-Forum/dash.js) – Javascriptový klient pro soubor M4S
* [Go Library pro vytváření souborů Dash](https://github.com/zencoder/go-dash)

### Open-Source API pro převod M4S na MP4

* [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## Reference ###

* [Formát ISO Base Media File (ISOBMFF)](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* [Dynamic Adaptive Streaming over HTTP – MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)

