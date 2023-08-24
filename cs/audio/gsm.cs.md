{
  "date" : "2021-08-05",
  "keywords" :[ "gsm", "soubor", "přípona", "formát", "Audio", "Globální systém pro mobilní zvuk", "přípona gsm", "soubory gsm"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů GSM a rozhraních API, která mohou vytvářet a otevírat soubory GSM.",
  "title" :"GSM - Globální systém pro mobilní formát audio souborů",
  "linktitle" : "GSM",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-05"
}

## Co je soubor GSM?

GSM je přípona souboru, která je spojena s Global System for Mobile Audio Format Files. Soubory obsahující GSM přípony lze otevřít na platformách Linux, Windows a Mac OS. Formát souboru GSM patří do kategorie audio souborů.

GSM soubor je zakódován ztrátovým kodekem pro kompresi zvuku CBR (Constant bitrate). Vzorkovací frekvence v GSM audio souboru je 8000 vzorků za sekundu, zatímco datová rychlost je přibližně 13 kbps. Datový tok v rámci souborů GSM zajišťuje kvalitu při nahrávání hlasu. Kromě toho je formát souboru GSM také známý jako globální standardní formát pro použití v mobilních telefonech a soubory WAV lze také snadno kódovat pomocí formátu souborů GSM. Jakékoli problémy s GSM souborem může uživatel snadno vyřešit sám, aniž by šel za odborníkem.

Uživatelé mohou také převádět GSM soubory do formátů [MP3](/cs/audio/mp3/) a [MP4](/cs/video/mp4/).

## Stručná historie formátu souborů GSM

GSM je formát audio souborů, který byl vytvořen pro internetovou telefonii v Evropě. Byl vyvinut Evropským institutem pro telekomunikační standardy (ETSI) pro použití jako 2G digitální mobilní telefon používaný v mobilních telefonech a tabletech. Dnes slouží k ukládání nahrávek telefonních hovorů a hlasových zpráv.

## Specifikace formátu souboru GSM ##

GSM funguje na strukturované síti, která se skládá z následujících částí:

- **Modulace**: Jedná se o proces transformace vstupních dat do formátu, který lze snadno přenášet. Přenášená data jsou demodulována na přijímací straně
- **Přenosová rychlost**: GSM je digitální systém, který má přenosovou rychlost vyšší než 270 kbps
- **Frekvenční rozsah uplink**: 933-960 MHz
- **Downlink frekvenční rozsah**: 890 – 915 MHz
- **Channel Spacing**: Znamená vzdálenost mezi sousedními bariérami, která by měla být asi 200 kHz
- **Duplexní vzdálenost**: Je to prostor mezi frekvencemi vzestupného a sestupného spoje, který by měl být 80 MHz
- **Kódování řeči**: GSM používá lineární prediktivní kódování (LPC). LPC komprimuje přenosovou rychlost. Když zvukový signál prochází filtrem a napodobuje vokální trakt. GSM kóduje řeč rychlostí 13 kbps

| Formát komprese zvuku | Algoritmus | Vzorkovací frekvence | Transformace bitové rychlosti | Latence | CBR | VBR | Stereo | Vícekanálový |
| ------------------------- | --------- | ----------- | ------------------- | -------- | --- | --- | ------ | ------------ |
| |
| GSM-HR | VŠELP | 8 kHz | 5,6 kbit/s | 25 ms | Ano | Ne | Ne | Ne |
| GSM-FR | RPE-LTP | 8 kHz | 13 kbit/s | 20–30 ms | Ano | Ne | Ne | Ne |
| GSM-EFR | ACELP | 8 kHz | 12,2 kbit/s | 20–30 ms | Ano | Ne | Ne | Ne |

## Reference ##

* [GSM – z Wikipedie](https://en.wikipedia.org/wiki/Comparison_of_audio_coding_formats)

