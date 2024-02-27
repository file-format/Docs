{
  "date": "2019-10-11",
  "keywords": [
"AVI",
"Komprimeret lydvideo",
"Fil",
"Udvidelse",
"Filformat",
"Multimediebeholder",
"XVid",
"DivX",
"Codecs",
"Ressourceudvekslingsfilformat",
"RIFF"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "AVI-filformat - En lydvideo-interleave-fil",
  "description": "Lær om AVI-filformater og API'er, der kan oprette og åbne AVI-filer.",
  "linktitle": "AVI",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-av-dai"
}
},
  "lastmod": "2021-04-23"
}

## Hvad er en AVI fil? ##

**AVI**-filformatet er et Audio Video multimedie-container-filformat, der blev introduceret af Microsoft. Den indeholder de lyd- og videodata, der er oprettet og komprimeret ved hjælp af flere codecs (Coders/Decodere), såsom **XVid** og **DivX**. Da forskellige codecs kan bruges til at kode AVI-indholdet, bør de hentende applikationer, dvs. AVI-afspillere, kun kunne åbne disse, hvis de har de nødvendige codecs installeret, som AVI-indholdet blev oprettet med. Formatet understøttes som standard på alle **Microsoft Windows**-platforme såvel som på næsten alle andre større platforme. Adskillige applikationer og API'er giver mulighed for at oprette/gemme, læse og konvertere AVI til andre populære formater såsom MP4, MOV, WMV osv.

## AVI-filformat ##

En fil med filtypenavnet .avi er en AVI-fil. Det er et underformat til Resource Interchange File Format (RIFF). RIFF organiserer data i blokke eller chunks, der er identificeret med en FourCC-tag. En AVI-fil er simpelthen en klump i en RIFF-formateret fil.

I den første underdel identificeres filens header af hdrl-tagget; dens indhold inkluderer videoens bredde, højde og billedhastighed. I den anden underdel repræsenterer bevægelsesmærket videoens billedhastighed. AVI-videoen består af de faktiske audio/visuelle data i denne del. Der er også en tredje valgfri underchunk med tagget idx1, som angiver positionen i filen af de individuelle datastykker, der hører til filen.

### Begrænsninger ###

* Oplysninger om billedformat kan ikke kodes i den originale AVI-specifikation, selvom den senere OpenDML-specifikation (AVI 2.0) tilbyder en standardiseret metode

* Selvom AVI-filer er meget brugt i film- og tv-postproduktion, konkurrerer forskellige metoder til at tilføje en tidskode til dem, hvilket påvirker formatets anvendelighed.

* En videofil kodet i AVI kan ikke bruge en komprimeringsteknik, der kræver fremtidige frames-data ud over den ramme, der kodes (B-frame)

* Det er problematisk at bruge AVI-filer med variable bitrates (VBR) (såsom MP3-lyd ved samplingshastigheder under 32 kHz)

* En AVI-fil, der koder spillefilm med standardopløsning, som normalt bruges, vil sandsynligvis medføre overhead på omkring 5 MB i timen, afhængigt af hvordan filen bruges

* Undertekster skal hardkodes i videostrømmen eller distribueres i en separat fil, hvis AVI-filer ikke kan rumme vedhæftede filer såsom skrifttyper og undertekster


## Kort historie ##

AVI blev introduceret af Microsoft i 1992 med det formål at give et mere robust og avanceret lyd- og videofilformat. Formatet blev hurtigt populært med brugen af internettet, hvilket gjorde det muligt for enkeltpersoner at dele videofiler direkte og indirekte via cloud-baseret medielagring.

## Referencer ##

* [AVI - af Wikipedia](https://en.wikipedia.org/wiki/Audio_Video_Interleave)


