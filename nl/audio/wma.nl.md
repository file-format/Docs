{
  "date" : "2021-02-20",
  "keywords" :[ "WMA", "bestand", "extensie", "format", "audio-uitwisselingsbestandsformaat", "muziek"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over WMA-bestandsindelingen en API's die WMA-bestanden kunnen maken en openen.",
  "title" :"WMA - Windows Media-audiobestand",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## Wat is een WMA-bestand?

Een bestand met de extensie .wma vertegenwoordigt een audiobestand dat is opgeslagen in de indeling Advanced Systems Format (ASF). ASF is het eigen formaat van Microsoft dat bitstreams bevat die zijn gecodeerd door Windows Media Audio 9. Naast de audio-inhoud bevat een WMA-bestand ook metadata-objecten zoals titel, album, artiest en genre van de track. WMA-bestanden worden voornamelijk gebruikt voor streaming via internet, vergelijkbaar met [.mp3](/nl/audio/mp3/)-bestanden.

## WMA-bestandsindeling

Een WMA-bestand is een binair bestandsformaat en is opgenomen in het ASF-bestandsformaat. Het specificeert de codering van metadata over het bestand vergelijkbaar met de ID3-tags die door de MP3-bestanden worden gebruikt. De WMA-codec wordt sinds 2008 door Microsoft gebruikt in zijn Protected Interoperable File Format (PIFF). Het is echter niet verklaard als gestandaardiseerde audiocodec door de gerelateerde industriestandaarden zoals DECE UltraViolet en MPEG-DASH.

### WMA-type specifieke gegevens

De typespecifieke informatie voor de Windows Media Audio-codec wordt opgeslagen in de volgende indeling als onderdeel van de typespecifieke gegevens van het Stream Properties-object.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Referenties

* [ASF-overzicht - Microsoft](https://docs.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format?redirectedfrom=MSDN)

