{
"date": "2023-07-12",
  "keywords": [
"mpeg",
"mpeg-fil",
"vad är en mpeg-fil",
"hur man öppnar mpeg-fil",
"fil",
"mpeg filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "MPEG-filformat - MPEG-video",
  "description":"Läs mer om MPEG-format och API:er som kan skapa och öppna MPEG-filer.",
  "linktitle": "MPEG",
  "menu": {
    "docs": {
      "identifier": "video-mpeg",
      "parent": "video"
}
},
"lastmod": "2023-07-12"
}

## Vad är en MPEG-fil?

En MPEG-fil, även känd som en MPEG-videofil, är ett digitalt videofilformat som använder MPEG-standarder (Moving Picture Experts Group) för videokomprimering. MPEG är ett allmänt använt format för att lagra och överföra videodata.

MPEG-formatet använder förlustkomprimering, vilket innebär att viss information kasseras för att minska filstorleken. Denna komprimeringsteknik möjliggör effektiv lagring och streaming av videoinnehåll samtidigt som den bibehåller rimlig videokvalitet. Det finns flera versioner av MPEG-standarden, inklusive MPEG-1, MPEG-2, MPEG-4 och MPEG-7, var och en med olika nivåer av komprimering och kvalitet.

MPEG-filer har vanligtvis filtillägget ".mpeg" eller ".mpg." De kan innehålla både video- och ljuddata, ofta kombinerade till en enda fil. MPEG-filer är kompatibla med ett brett utbud av mediaspelare och videoredigeringsprogram, vilket gör dem till ett populärt val för att dela och distribuera videoinnehåll.

## Hur öppnar man en MPEG-fil?

Det finns många program tillgängliga som kan öppna och spela MPEG-filer. Här är några populära alternativ:

- VLC Media Player
- Windows mediaspelare
- QuickTime Player
- MPC-HC
- GOM-spelare
- MPlayer
- PotPlayer
- Kodi

## Hur konverterar man en MPEG-fil?

Det finns ett antal videoapplikationer inklusive VideoLAN VLC-mediaspelare, HandBrake och Apple QuickTime Player, som kan konvertera MPEG-filer till andra format. Till exempel kan VLC konvertera MPEG-filer till dessa format

- MP4
- AVI
- MKV
- MOV
- WMV
- FLV

## Översikt över MPEG-filers interna struktur

Den interna strukturen för MPEG-filer består av olika komponenter och datastrukturer som organiserar och lagrar video, ljud och annan relaterad information. Här är en översikt över nyckelelementen i den interna strukturen för MPEG-filer:

- **Systemlager:**

Systemlagret definierar MPEG-filens övergripande struktur. Den innehåller rubriker, programströmmar och annan systemrelaterad data som behövs för avkodning och uppspelning. Systemlagret är ansvarigt för att hantera synkronisering och multiplexering av elementära strömmar.

- **Elementära strömmar:**

MPEG-filer innehåller separata elementära strömmar för video, ljud och andra datatyper. Varje elementär ström bär komprimerad data som är specifik för sin typ. Till exempel innehåller den elementära videoströmmen komprimerade videoramar, och den elementära ljudströmmen innehåller komprimerade ljudsampel.

- **Videokomprimering:**

MPEG-videokomprimeringstekniker, såsom intra-frame och inter-frame-komprimering, används för att minska filstorleken samtidigt som videokvaliteten bibehålls. De komprimerade videoramarna är organiserade i grupper av bilder (GOP), som består av intrakodade (I), predikterade (P) och dubbelriktade (B) ramar.

- **Ljudkomprimering:**

MPEG-filer stöder olika ljudkomprimeringscodecs, som MP3, AAC eller MPEG-1 Audio Layer II. Ljudsamplen komprimeras med dessa codecs, vilket möjliggör effektiv lagring och överföring av ljuddata.

- **Synkronisering och timing:**

MPEG-filer använder tidsstämplar och synkroniseringsinformation för att säkerställa korrekt anpassning mellan video- och ljudströmmar under uppspelning. Dessa tidsstämplar hjälper till att upprätthålla synkronisering och ger korrekt timing för avkodning och rendering av ljud- och videoramar.

- **Metadata:**

MPEG-filer kan innehålla metadata som ger ytterligare information om video- och ljudinnehållet. Denna metadata kan innehålla detaljer som titel, författare, datum för skapande och annan beskrivande information.

- **Paket och packhuvuden:**

MPEG-filer organiserar data i paket. Varje paket innehåller ett pakethuvud som ger information om paketets innehåll, såsom strömtyp, paketstorlek och tidsinformation.

- **Programspecifik information (PSI):**

PSI är ett avsnitt i MPEG-filer som innehåller ytterligare information om programströmmarna, såsom program- och strömidentifierare, strömtyp och beskrivningar. PSI hjälper till att avkoda och demultiplexera de elementära strömmarna i filen.

- **Transportström:**

I MPEG-2 finns det ett specifikt transportströmformat som används för att sända och överföra videoinnehåll. Transportströmmen multiplexerar flera program till en enda ström, vilket möjliggör effektiv överföring och synkronisering av ljud, video och andra data över nätverk.

## MPEG-filformat - Mer information

Här är några viktiga saker att veta om MPEG-filformatet:

- **Kompression:**

MPEG-filer använder förlustkompressionstekniker för att minska filstorleken samtidigt som en rimlig videokvalitet bibehålls. Mängden komprimering kan variera beroende på MPEG-version och inställningar som används.

- **Video och ljud:**

MPEG-filer kan innehålla både video- och ljuddata. Videodata komprimeras med hjälp av MPEG-standarder, medan ljudet kan komprimeras med hjälp av olika ljudkodekar som MP3 eller AAC.

- **MPEG-versioner:**

Det finns olika versioner av MPEG-standarden, inklusive MPEG-1, MPEG-2, MPEG-4 och MPEG-7. Varje version har sina egna specifikationer, möjligheter och komprimeringsnivåer. MPEG-1 används vanligtvis för VCD-skivor (Video-CD-skivor), medan MPEG-2 används för DVD-skivor och TV-sändningar. MPEG-4 används i stor utsträckning för videostreaming online, och MPEG-7 fokuserar på beskrivning av multimediainnehåll och metadata.

- **Filtillägg:**

MPEG-filer har vanligtvis filtilläggen ".mpeg" eller ".mpg". Det kan dock finnas olika varianter och tillägg, till exempel ".mp4" för MPEG-4-filer eller ".mp3" för MPEG-1 Audio Layer 3-filer.

- **Tvärplattformskompatibilitet:**

MPEG-filer stöds brett av olika mediaspelare, operativsystem och enheter. De kan spelas på Windows-, Mac- och Linux-system, såväl som på smartphones, surfplattor och smarta TV-apparater.

- **Redigering:**

MPEG-filer kan redigeras med videoredigeringsprogram. Men eftersom MPEG använder förlustkomprimering kan upprepad redigering och omkodning av filen resultera i en kvalitetsförsämring. Det rekommenderas ofta att arbeta med förlustfria format eller göra säkerhetskopior innan omfattande redigering.

- **Strömning:**

MPEG-filer används ofta för att strömma videoinnehåll över internet. MPEG-4, i synnerhet, är populärt för onlinevideoplattformar och videodelningswebbplatser på grund av dess effektiva komprimering och goda förhållande mellan kvalitet och storlek.

- **Underbara standarder:**

MPEG-standarderna fortsätter att utvecklas för att hålla jämna steg med tekniska framsteg. Nyare versioner och varianter, som MPEG-4 Part 10 (även känd som H.264 eller AVC) och MPEG-4 Part 14 (MP4), erbjuder förbättrad komprimeringseffektivitet och stöd för avancerade funktioner som högupplöst video och 3D-innehåll.

- **Multimediaapplikationer:**

MPEG-filer hittar applikationer inom olika områden, inklusive digital-tv, streamingtjänster, videokonferenser, videoövervakning, multimediapresentationer och mer.

## MPEG vs andra format

När man jämför MPEG-filformatet med andra videoformat spelar flera faktorer in, inklusive komprimeringseffektivitet, kompatibilitet, funktioner och support. Här är en jämförelse av MPEG med några populära videoformat:

### MPEG vs. AVI (Audio Video Interleave)

- **Kompression:**
   

MPEG-filer erbjuder generellt högre komprimeringseffektivitet jämfört med AVI, vilket resulterar i mindre filstorlekar.

- **Kompatibilitet:**

AVI-filer stöds brett av olika mediaspelare, men MPEG-filer har bredare kompatibilitet mellan enheter och plattformar.

- **Funktioner:**

MPEG-filer stöder ofta mer avancerade funktioner, såsom flera ljudspår, undertexter och kapitel, medan AVI har begränsat stöd för sådana funktioner.

- **Videokvalitét:**

Beroende på komprimeringsinställningarna kan MPEG och AVI uppnå liknande videokvalitet, men MPEG ger ofta bättre kvalitet vid lägre bithastigheter på grund av avancerade komprimeringstekniker.

### MPEG vs. WMV (Windows Media Video):

- **Kompression:**

WMV-filer erbjuder generellt bättre komprimeringseffektivitet jämfört med MPEG, vilket resulterar i mindre filstorlekar med bibehållen god videokvalitet.

- **Kompatibilitet:**

MPEG-filer har bredare kompatibilitet över olika enheter och plattformar, medan WMV-filer främst är associerade med Windows-baserade system.

- **Funktioner:**

Båda formaten stöder en rad funktioner, inklusive flera ljudspår och undertexter, men MPEG ger ofta mer mångsidighet och bredare stöd för avancerade funktioner.

- **Videokvalitét:**

Med liknande komprimeringsinställningar kan MPEG och WMV uppnå jämförbar videokvalitet, men WMV kan prestera bättre i vissa scenarier på grund av dess avancerade komprimeringstekniker.

### MPEG vs. MP4 (MPEG-4 del 14):

- **Kompression:**

Både MPEG och MP4 använder liknande komprimeringstekniker, och komprimeringseffektiviteten kan vara jämförbar. Men MPEG-4 Part 10 (H.264/AVC) inom MP4 ger ofta bättre komprimering än äldre MPEG-format.

- **Kompatibilitet:**

Både MPEG och MP4 har utbredd kompatibilitet över enheter och plattformar. MP4 har vunnit betydande popularitet de senaste åren på grund av dess breda stöd och adoption.

- **Funktioner:**

MP4 erbjuder mer avancerade funktioner och möjligheter, inklusive stöd för undertexter, kapitel, interaktiva menyer och avancerade videocodecs som H.264 och HEVC (H.265). MPEG-4 Part 2 (DivX, Xvid) inom MP4 stöder även avancerade funktioner.

- **Videokvalitét:**

MPEG och MP4 kan uppnå liknande videokvalitet när du använder jämförbara komprimeringsinställningar. Men MP4:s stöd för mer avancerade video-codecs möjliggör bättre kvalitet vid lägre bithastigheter.

## Referenser
* [MPEG-1](https://en.wikipedia.org/wiki/MPEG-1)

