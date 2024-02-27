{
   "date":"2023-10-11",
   "keywords":[
"m2v",
"m2v fil",
"m2v mpeg-2 videofil",
"hvordan man åbner en m2v fil",
"fil",
"m2v filtypenavn",
"udvidelse",
"fil"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"M2V filformat - MPEG-2 video",
   "description":"Lær om M2V MPEG-2 Video-filformat og API'er, der kan oprette og åbne M2V-filer.",
   "linktitle":"M2V",
   "menu":{
      "docs":{
         "identifier":"video-m2v-da",
         "parent":"video"
}
},
   "lastmod":"2023-10-11"
}

## Hvad er en M2V fil?

M2V-filformatet er en filtypenavn, der almindeligvis forbindes med **MPEG-2 Video**. MPEG-2 er en udbredt videokomprimeringsstandard, der ofte bruges til dvd'er, digital tv-udsendelse og andre videodistributionsmetoder. M2V-formatet indeholder specifikt kun videodata, hvilket betyder, at det ikke inkluderer lyd eller andre multimediekomponenter. Det er i det væsentlige rå eller elementær stream af video.

M2V-filer kan bruges til forskellige formål, herunder oprettelse af dvd'er eller oprettelse af videoindhold til udsendelse. Når du for eksempel opretter dvd'er, parres M2V-videostream typisk med en separat lydfil i formater som [AC3](/audio/ac3/) eller LPCM for at skabe en komplet dvd-video.

For at bruge M2V-filer i videoredigerings- eller redigeringssoftware skal du muligvis kombinere dem med en passende lydfil, oprette menuer og strukturere dit indhold til DVD-forfatter eller et andet distributionsformat.

M2V-filer er generelt ikke beregnet til direkte afspilning på de fleste medieafspillere eller videoredigeringssoftware, fordi de mangler lyd og andre nødvendige komponenter til komplet videooplevelse. I stedet er de en del af et større multimedieprojekt eller distributionspakke.

## M2V egenskaber

M2V-filer, der er en del af MPEG-2-videostandarden, har nogle vigtige egenskaber og overvejelser:

1.  **Video Codec**: M2V-filer bruger MPEG-2 video-codec, som er bredt accepteret og veletableret komprimeringsstandard. MPEG-2 tilbyder god videokvalitet og komprimeringseffektivitet, hvilket gør den velegnet til forskellige applikationer, herunder dvd'er og digital udsendelse.
    
2.  **Ingen lyd**: M2V-filer indeholder kun videokomponenter, så de mangler lyddata. For at skabe en komplet videofil parres M2V-filer ofte med separate lydfiler, typisk i formater som AC3 (Dolby Digital) eller LPCM (Linear Pulse Code Modulation).
    
3.  **Videokvalitet**: Kvaliteten af video i en M2V-fil kan variere baseret på faktorer som bitrate og opløsningsindstillinger, der bruges under kodning. Højere bithastigheder og opløsninger resulterer i bedre videokvalitet, men også større filstørrelser.
       
4.  **DVD Authoring**: M2V files are commonly used in authoring of DVDs. DVD authoring software combines M2V video streams with separate audio tracks, menus and navigation features to create complete DVD video.
    
5.  **Bitrate Control**: Bithastigheden af videostream i en M2V-fil er en vigtig overvejelse. Det påvirker både videokvaliteten og mængden af krævet lagerplads. Højere bithastigheder resulterer i bedre kvalitet, men større filstørrelser.
    
6.  **Billedforhold**: M2V-filer kan understøtte forskellige billedformater, såsom 4:3 (standard) eller 16:9 (widescreen), afhængigt af det tiltænkte visningsformat.
    
7.  **Opløsning**: Opløsningen af video i en M2V-fil kan variere, idet almindelige opløsninger er 720x480 (standardopløsning) og 1920x1080 (høj opløsning).
    
8.  **Billedhastighed**: MPEG-2-video kan kodes ved forskellige billedhastigheder, men almindelige billedhastigheder inkluderer 29,97 fps for NTSC (nordamerikansk) video og 25 fps for PAL (europæisk) video.
    
9.  **Redigering**: M2V-filer kan redigeres med kompatibel videoredigeringssoftware, men du skal muligvis rekombinere dem med lydspor og andre multimedieelementer for at skabe den endelige, komplet video.

## M2V relation med multimedieformater

M2V files, as MPEG-2 video streams, are related to several other multimedia formats and components within context of video authoring, playback and distribution. Here are some of key relationships:

1.  **Lydformater (AC3, LPCM osv.)**: For at skabe en komplet videofil parres M2V-filer typisk med separate lydfiler i formater som AC3 (Dolby Digital) eller LPCM (Linear Pulse Code Modulation). Disse lydformater leverer lydkomponenter til multimedieindhold.
    
2.  **DVD Format (VOB)**: When authoring DVDs, M2V files, along with audio and other assets, are often combined into Video Object (VOB) format. VOB files contain video, audio, subtitles and menu information for DVD video discs.
    
3.  **Transport Stream (TS)**: I digital udsendelse er MPEG-2-video ofte pakket ind i Transport Stream (TS). Dette format inkluderer video, lyd og metadata til udsendelse af digitalt tv og bruges i tjenester som DVB (Digital Video Broadcasting) og ATSC (Advanced Television Systems Committee).
    
4.  **Program Stream (PS)**: Program Stream-formatet (PS) er en anden beholder, der bruges til lagring af MPEG-2 video, lyd og andre data. Det bruges ofte til videodistribution og -lagring.
    
5.  **MPG (MPEG)-format**: Filtypenavnet .MPG bruges almindeligvis til at betegne MPEG-2-videofiler, som kan indeholde både video og lyd. M2V-filer er undersæt af bredere MPEG-format, der specifikt fokuserer på video uden lyd.
    
6.  **VOB (Video Object)-filer**: VOB-filer, som en del af DVD-video, kan indeholde M2V-videostreams. Når du opretter DVD, består videoindhold i VOB-filer ofte af M2V-video og tilhørende lyd.
    
7.  **Videoredigeringssoftware**: Videoredigeringssoftware, såsom Adobe Premiere Pro, Final Cut Pro eller Sony Vegas, kan arbejde med M2V-filer til redigeringsformål. Redaktører kombinerer M2V-videostreams med lyd og andre aktiver for at skabe komplette videoprojekter.
    
8.  **Medieafspillere**: Medieafspillere, såsom VLC eller Windows Media Player, er typisk ikke egnede til direkte afspilning af M2V-filer, fordi de mangler lyd. Disse afspillere er designet til at håndtere mere almindelige multimedieformater, såsom AVI, MP4 eller MKV, som inkluderer både video og lyd.
    
9.  **Blu-ray-format (M2TS)**: Selvom det ikke er direkte relateret til M2V, bruges M2TS-formatet almindeligvis til high-definition-video på Blu-ray-diske. M2TS-filer kan indeholde MPEG-2-videostreams såvel som H.264- eller VC-1-videostreams sammen med forskellige lydformater.
    
10.  **Videokomprimeringsstandarder**: MPEG-2-video, som brugt i M2V-filer, er relateret til andre videokomprimeringsstandarder, såsom MPEG-4 (inklusive H.264 og H.265) og VP9, som tilbyder forbedret komprimeringseffektivitet og videokvalitet. Disse standarder bruges til digital streaming, online video og nyere optiske diskformater som Blu-ray.

## Hvordan åbner jeg filen M2V?

Programmer, der åbner M2V filer inkluderer

- VLC medieafspiller (cross-platform)
- Apple QuickTime Player (Mac)
- Nullsoft Winamp
- CyberLink PowerDVD 21
- Windows Media Player (Windows)
- Media Player Classic (Windows)

## Referencer
* [Videofilformat](https://en.wikipedia.org/wiki/Video_file_format)


