{
  "date" : "2019-10-11",
  "keywords" :[ "AVI", "Komprimerad ljudvideo", "Fil", "Extension", "Filformat", "Multimedia Container", "XVid", "DivX", "Codecs", "Resource Interchange File Format", "RIFF "],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AVI-filformat - en ljudvideointerfolieringsfil",
  "description":"Läs mer om AVI-filformat och API:er som kan skapa och öppna AVI-filer.",
  "linktitle" : "AVI",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-04-23"
}

## Vad är en AVI-fil? ##

Filformatet **AVI** är ett multimediacontainerformat för ljudvideo som introducerades av Microsoft. Den innehåller ljud- och videodata som skapats och komprimerats med hjälp av flera codecs (Coders/Decoders) som **XVid** och **DivX**. Eftersom olika codecs kan användas för att koda AVI-innehållet, bör de hämtande programmen, dvs. AVI-spelare, endast kunna öppna dessa om de har de nödvändiga codecs installerade med vilka AVI-innehållet skapades. Formatet stöds som standard på alla **Microsoft Windows**-plattformar såväl som på nästan alla andra större plattformar. Flera applikationer och API:er ger möjlighet att skapa/spara, läsa och konvertera AVI till andra populära format som MP4, MOV, WMV, etc.

## AVI-filformat ##

En fil med filtillägget .avi är en AVI-fil. Det är ett underformat till Resource Interchange File Format (RIFF). RIFF organiserar data i block, eller "bitar", som identifieras med en FourCC-tagg. En AVI-fil är helt enkelt en "bit" i en RIFF-formaterad fil.

I den första underdelen identifieras filens rubrik av "hdrl"-taggen; dess innehåll inkluderar videons bredd, höjd och bildhastighet. I den andra underdelen representerar rörelsetaggen videons bildhastighet. AVI-videon består av de faktiska audio/visuella data i denna bit. Det finns också en tredje valfri subchunk med taggen "idx1", som indikerar positionen i filen för de individuella databitarna som tillhör filen.

### Begränsningar ###

* Information om bildförhållande kan inte kodas i den ursprungliga AVI-specifikationen, även om den senare OpenDML-specifikationen (AVI 2.0) erbjuder en standardiserad metod
* Även om AVI-filer används i stor utsträckning i film- och tv-postproduktion, konkurrerar olika metoder för att lägga till en tidskod till dem, vilket påverkar formatets användbarhet.
* En videofil kodad i AVI kan inte använda en komprimeringsteknik som kräver framtida ramdata utöver ramen som kodas (B-frame)
* Det är problematiskt att använda AVI-filer med variabel bithastighet (VBR) (som MP3-ljud vid samplingshastigheter under 32 kHz)
* En AVI-fil som kodar spelfilmer med standardupplösning som normalt används kommer sannolikt att medföra omkostnader på cirka 5 MB per timme, beroende på hur filen används
* Undertexter måste hårdkodas i videoströmmen eller distribueras i en separat fil om AVI-filer inte kan ta emot bilagor som typsnitt och undertexter

## Kortfattad bakgrund ##

AVI introducerades av Microsoft 1992 med syftet att tillhandahålla ett mer robust och avancerat ljud- och videofilformat. Formatet blev snabbt populärt med användningen av internet, vilket gjorde det möjligt för individer att dela videofiler direkt och indirekt via molnbaserad medielagring.

## Referenser ##

* [AVI - av Wikipedia](https://en.wikipedia.org/wiki/Audio_Video_Interleave)

