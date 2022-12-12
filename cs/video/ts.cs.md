{
  "date" : "2021-12-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru TS - soubor přenosového toku videa",
  "keywords" :[ "ts", "flie", "extension", "extension", ".ts", "format" ],
  "description":"Zjistěte, co je soubor TS a rozhraní API, která mohou vytvářet a otevírat soubory TS.",
  "linktitle" : "TS",
  "menu" : {
    "docs" : {
      "identifier":"video-ts",
      "parent" : "video"
}
},
  "lastmod" : "2021-12-16"
}

## Co je soubor TS?

Soubor s příponou .ts je video stream, který ukládá data na disky DVD. Používá kompresní algoritmus MPEG-2 ([.mpeg](/cs/video/mpg/)) k dosažení maximální účinnosti a kompatibility napříč různými typy médií, jako je internetové streamování a vysílání. Formát souboru TS byl vytvořen, aby jej bylo možné přehrávat na zařízeních se špatným internetovým připojením, jako je chytrá televize.

## Formát souboru TS – Další informace

Data v souboru TS jsou podobná souboru [MP4](/cs/video/mp4/), ale jsou rozdělena na malé kousky. Každý blok se skládá z malého kousku videa, za kterým následuje ting bit zvuku a volitelný titulek. Jeden soubor TS se skládá z mnoha takových částí. Kromě videa, zvuku a titulků obsahuje každý blok také některá další data pro detekci chyb v bloku. Díky tomu jsou soubory TS poněkud větší.

### Proč používat formát souboru TS?

Pokud jsou tedy soubory TS poněkud velké, jakou výhodu nabízí jejich použití namísto jiných formátů souborů? Ve vysílání lze malé kousky videa a zvuku posílat komunikačními médii (drátovými nebo rádiem) v reálném čase. Extra data v blocích používá přijímač k přeskočení chunků náchylných k chybám.

Kromě toho se používají soubory TS, protože vysílací systém nepotřebuje k přehrání celý stream. Přenos lze zachytit a použít v reálném čase sestavením zvuku a videa.

## Jak přehrávat soubory TS?

Soubory TS lze otevřít a přehrát v populárním [VideoLAN VLC media player] (https://www.videolan.org/vlc/features.html), který je volně dostupný ke stažení.

## Reference ##

* [MPEG Transport Stream – Wikipedie](https://en.wikipedia.org/wiki/MPEG_transport_stream)

