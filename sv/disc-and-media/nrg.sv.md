{
  "date" : "2021-08-16",
  "keywords" :[ "nrg fil", "nrg filformat", "vad är en nrg fil", "fil", "nrg exempel", "nrg filtillägg", "tillägg", "format", "nrg sidfot", "fil format av nrg", "Nero Burning Rom", "Nero AG" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Läs mer om NRG-filformat och API:er som kan skapa och öppna NRG-filer.",
  "title" :"NRG - Disk Image File Format",
  "linktitle" : "NRG",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-16"
}

## Vad är NRG fil?

Ett bildfilformat som skapas med hjälp av en optisk skiva anses vara ett NRG-filformat. Det här formatet är specifikt skapat av Nero för verktyget Nero Burning Rom. För lagring av skivbilder anses detta format användas eftersom det är lämpligt för dessa specifika filer. Dessa filer kan vara i form av en exakt kopia av en CD eller DVD eller kan ha flera filer som kan monteras som en disk. Andra mer populära filformat som [ISO](/sv/compression/iso/) filformat är de som dessa filer kan konverteras till några grundläggande verktyg. Oftast används NRG-filerna för att skapa säkerhetskopior eller kopior av vissa viktiga data eller skivor.

## NRG-filformat ##

Detta filformat har utvecklats av Nero AG som ett diskavbildningsformat. Den hade den specifika egenskapen hos verktyget Nero Burning Rom eftersom det utvecklades för att lagra skivbilder. Dess första version specificerades för att lagra värden som 32-bitars heltal. Dess andra version lanserades dock och innehöll stöd för 64-bitars heltal.

## Teknisk specifikation ##

I början av filen lagrar inte detta format dess data som en rubrik. Som en sidfot bifogas den i slutet av filen. I form av bitar av IFF lagras bildens information. Förskjutningen av den första biten kan erhållas genom att läsa NRG-sidfoten vid de sista 8 byte till 12 byte av filen. I alla versioner av NRG-filformat finns det bitar, DAOI, CD-text, medietyp för sessionsinformation, skivinformation, Relo och kedjans slut. Byteordningen är big-endian och alla heltalsvärden är osignerade vid tidpunkten för lagring.

### Huvudklumpar ###

#### Cue Sheet ####

Detta cue sheet är lätt tillgängligt i alla versioner av NRG-filformat. Biten av **CUEX** betyder blocken med sammanlänkning av fast storlek och var och en av dessa representerar referenspunkten.

#### DAO-information ####

Denna information finns också i alla versioner av NRG-format. Bitarna av **DAOI** lagrar relevant specifik information i 2 delar. Den första delen består endast av sessionsspecifika data. Dess andra del upprepar bara den grå informationen relaterad till spårning och den är bara en gång för varje spår.

#### CD-text ####

Denna finns i NRG:s andra version. Biten av **CDTX** består av CD-textpaketets råsammansättning som har 18 byte för varje.

#### Utökad spårinformation ####

Detta är tillgängligt i alla versioner av filformatet för NRG. Dessa bitar används för att lagra spårningsinformationen för spåret med samtidigt sessioner. Denna data upprepas endast en gång för varje spår.

#### Sessionsinformation ####

Detta är också tillgängligt i alla versioner av filformatet för NRG. Informationen om sessionsbitar måste användas för att snabbt skanna sessionens bild och sedan spåra antalet.

#### Kedjeände ####

The chunk of end innebär signalerna om att det nu inte finns några fler bitar som behöver läsas och detta finns även i NRG:s alla versioner.


## Referenser ##

* [NRG - av Wikipedia](https://en.wikipedia.org/wiki/NRG_(file_format))


