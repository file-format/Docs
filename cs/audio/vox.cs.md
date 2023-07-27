{
  "date" : "2021-08-11",
  "keywords" :[ "vox", "soubor", "přípona", "formát", "audio", "ADPCM", "Dialogic ADPCM", "Xentec VOX Studio","přípona vox", "soubory vox"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů VOX a rozhraních API, která mohou vytvářet a otevírat soubory VOX.",
  "title" :"VOX - Audio File Format",
  "linktitle" : "VOX",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-11"
}

## Co je soubor VOX? ##

Při nízké vzorkovací frekvenci jsou soubory VOX určeny pro ukládání digitalizovaných hlasových dat. Jedná se o zvukové soubory, které se běžně používají v aplikacích určených pro telefonickou komunikaci. Tento typ formátu souboru používá algoritmus ztrátové komprese, který má optimalizaci pro hlas.

Soubory VOX, které se běžně používají v řečových aplikacích, obsahují předem nahrané hlasové výzvy. Tento typ formátu souboru se také převádí do dalších populárnějších formátů. Ty lze použít v operačním systému Windows a macOS.

Většinou se používá pro znělé nahrávky a kompresi. V tomto formátu nelze ukládat polyfonní data, protože podporuje pouze homofobní data.



## Stručná historie ##

Soubory VOX jsou spojeny s mediálními deskami nazývanými DMV a JCT společnosti Dialogic. Patří k VoxWare a mnoha dalším softwarům. Dříve byl považován za zastaralý formát.

Jako zastaralý formát se poté nepoužíval. Podobně jako ostatní formáty ADPCM byl komprimován do 4 bitů. Vlastnosti těchto souborů jsou dostatečně blízké specifikacím souborů [WAV](/cs/audio/wav/).


## Specifikace formátu ##

Tento typ formátu souboru je kompatibilní s programy OS Windows, jako je Xentec Vox Studio. Má specifické vlastnosti, které se používají ke stimulaci řeči lidí. Arkádové hry většinou používají tento formát. Přípona souboru VOX má 32bajtové záhlaví spolu s 10bajtovými indexy a snímky. Vlastní hlasová data jsou uložena v rámečcích ve formě segmentů v jediném souboru. V každém rámci je různá forma několika bajtů podle typu kódování.

Čistota hlasu je udržována při nízké vzorkovací frekvenci, která je u většiny zvukových formátů vzácná. Algoritmus použitý v těchto byl matematický.

Tento soubor je zakódován pomocí ADPCM. Zkracuje 16bitová zvuková data a 4bitovou kompresi. Výhodou je tedy ukládání větších zvukových informací v kompaktní podobě pomocí souborů VOX.


## Reference ##

* [VOX – z Wikipedie](https://en.wikipedia.org/wiki/Dialogic_ADPCM)

