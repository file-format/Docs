{
  "date" : "2019-10-11",
  "keywords" :[ "AVI", "Compressed Audio Video", "File", "Extension", "File Format", "Multimedia Container", "XVid", "DivX", "Codecs", "Resource Interchange File Format", "RIFF "],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AVI-bestandsindeling - een audio-video-interleave-bestand",
  "description":"Meer informatie over AVI-bestandsindelingen en API's die AVI-bestanden kunnen maken en openen.",
  "linktitle" : "AVI",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-04-23"
}

## Wat is een AVI-bestand? ##

Het **AVI**-bestandsformaat is een audio/video-multimedia-containerbestandsformaat dat werd geïntroduceerd door Microsoft. Het bevat de audio- en videogegevens die zijn gemaakt en gecomprimeerd met behulp van verschillende codecs (Coders/Decoders) zoals **XVid** en **DivX**. Aangezien verschillende codecs kunnen worden gebruikt om de AVI-inhoud te coderen, zouden de ophalende toepassingen, dwz AVI-spelers, deze alleen moeten kunnen openen als ze de vereiste codecs hebben geïnstalleerd waarmee de AVI-inhoud is gemaakt. Het formaat wordt standaard ondersteund op alle **Microsoft Windows**-platforms en op bijna alle andere grote platforms. Verschillende applicaties en API's bieden de mogelijkheid om AVI te maken/op te slaan, te lezen en te converteren naar andere populaire formaten zoals MP4, MOV, WMV, enz.

## AVI-bestandsindeling ##

Een bestand met de extensie .avi is een AVI-bestand. Het is een subformaat van het Resource Interchange File Format (RIFF). RIFF organiseert gegevens in blokken, of "chunks", die worden geïdentificeerd met een FourCC-tag. Een AVI-bestand is gewoon een "chunk" in een RIFF-geformatteerd bestand.

In de eerste sub-chunk wordt de kop van het bestand geïdentificeerd door de tag "hdrl"; de inhoud omvat de breedte, hoogte en framesnelheid van de video. In de tweede sub-chunk vertegenwoordigt de motion tag de framesnelheid van de video. De AVI-video bestaat uit de daadwerkelijke audio/visuele gegevens in dit stuk. Er is ook een derde optionele subchunk met de "idx1" tag, die de positie binnen het bestand aangeeft van de individuele data chunks die bij het bestand horen.

### Beperkingen ###

* Informatie over de hoogte-breedteverhouding kan niet worden gecodeerd in de oorspronkelijke AVI-specificatie, hoewel de latere OpenDML-specificatie (AVI 2.0) een gestandaardiseerde methode biedt
* Hoewel AVI-bestanden veel worden gebruikt in de postproductie van films en televisie, concurreren verschillende benaderingen om er een tijdcode aan toe te voegen, met elkaar in strijd, wat de bruikbaarheid van het formaat beïnvloedt.
* Een videobestand gecodeerd in AVI kan geen compressietechniek gebruiken die toekomstige framegegevens vereist buiten het frame dat wordt gecodeerd (B-frame)
* Het is problematisch om AVI-bestanden te gebruiken met variabele bitrates (VBR) (zoals MP3-audio met samplefrequenties onder 32 kHz)
* Een AVI-bestand dat speelfilms met standaarddefinitie codeert zoals normaal gebruikt, zal waarschijnlijk ongeveer 5 MB per uur aan overheadkosten veroorzaken, afhankelijk van hoe het bestand wordt gebruikt
* Ondertitels moeten hard gecodeerd zijn in de videostream of gedistribueerd worden in een apart bestand voor het geval AVI-bestanden geen bijlagen zoals lettertypen en ondertitels kunnen bevatten

## Korte geschiedenis ##

AVI werd in 1992 door Microsoft geïntroduceerd met als doel een robuuster en geavanceerder audio- en videobestandsformaat te bieden. Het formaat werd snel populair bij het gebruik van internet, waardoor individuen videobestanden direct en indirect konden delen via cloudgebaseerde media-opslag.

## Referenties ##

* [AVI - Door Wikipedia](https://en.wikipedia.org/wiki/Audio_Video_Interleave)

