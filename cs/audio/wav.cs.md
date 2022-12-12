{
  "date" : "2019-12-13",
  "keywords" :[ "WAV", "soubor", "přípona", "formát", "formát souboru pro výměnu zvuku", "hudba" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů WAV a rozhraních API, která mohou vytvářet a otevírat soubory WAV.",
  "title" :"WAV - Waveform Audio File Format",
  "linktitle" : "WAV",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2019-12-13"
}

## Co je soubor WAV?

WAV, známý jako WAVE (Waveform Audio File Format), je podmnožinou specifikace RIFF (Resource Interchange File Format) společnosti Microsoft pro ukládání digitálních zvukových souborů. Formát neaplikuje žádnou kompresi na bitový tok a ukládá zvukové záznamy s různými vzorkovacími frekvencemi a bitovými toky. Byl a je jedním ze standardních formátů pro audio CD. Soubory Wave mají větší velikost ve srovnání s novými formáty zvukových souborů, jako je [MP3](/cs/audio/mp3/), který využívá ztrátovou kompresi ke zmenšení velikosti souboru při zachování stejné kvality zvuku. Soubory WAV však lze komprimovat pomocí kodeků Audio Compression Manager (ACM). Existuje několik dostupných rozhraní API a aplikací, které mohou převádět soubory WAV do jiných populárních formátů zvukových souborů.

**Věděl jsi?**
Můžete se stát přispěvatelem na FileFormat.com a udržovat komunitu formátů souborů aktuální s vašimi zjištěními. Pokud se chcete podělit o cokoli o formátech souborů WAV nebo Audio, můžete svá zjištění zveřejnit v sekci [Zprávy o formátu zvukových souborů](https://news.fileformat.com/t/audio), aby lidé měli aktuální informace.

## Formát souboru WAV ##

Formát souboru WAVE, který je podmnožinou specifikace RIFF společnosti Microsoft, začíná záhlavím souboru následovaným sekvencí datových bloků. Soubor WAVE má jeden „WAVE“ blok, který se skládá ze dvou dílčích bloků:

* blok "fmt" - určuje formát dat
* "data" chunk - obsahuje aktuální ukázková data

### Záhlaví souboru WAV ###

Záhlaví souboru WAV (RIFF) je dlouhé 44 bajtů a má následující formát:


|Pozice|Ukázková hodnota|Popis
---|---|---|
|1 - 4|"RIFF"|Označí soubor jako soubor riff. Každý znak je dlouhý 1 bajt.
|5 - 8|Velikost souboru (celé číslo)|Velikost celého souboru - 8 bajtů, v bajtech (32bitové celé číslo). Obvykle byste to vyplnili po vytvoření.
|9 -12|"WAVE"|Záhlaví typu souboru. Pro naše účely se vždy rovná "VLNĚ".
|13-16|"fmt "|Formátovat značku bloku. Zahrnuje koncovou hodnotu null
|17-20|16|Délka dat formátu, jak je uvedeno výše
|21-22|1|Typ formátu (1 je PCM) – 2bajtové celé číslo
|23-24|2|Počet kanálů – 2bajtové celé číslo
|25-28|44100|Vzorkovací frekvence – 32 bajtové celé číslo. Běžné hodnoty jsou 44100 (CD), 48000 (DAT). Vzorkovací frekvence = Počet vzorků za sekundu neboli Hertz.
|29-32|176400|(vzorkovací frekvence * bity za vzorek * kanály) / 8.
|33-34|4|(BitsPerSample * Kanály) / 8.1 - 8 bitů mono2 - 8 bitů stereo/16 bitů mono4 - 16 bitů stereo
|35-36|16|Bitů na vzorek
|37-40|"data"|"data" hlavička bloku. Označuje začátek datové části.
|41-44|Velikost souboru (data)|Velikost datové části.
|Ukázkové hodnoty jsou uvedeny výše pro 16bitový stereofonní zdroj.

## Reference ##

* [WAV – podle Wikipedie](https://en.wikipedia.org/wiki/WAV)

