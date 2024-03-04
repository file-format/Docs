{
   "date":"2023-10-11",
   "keywords":[
"m2v",
"m2v failą",
"m2v mpeg-2 vaizdo failas",
"Kaip atidaryti m2v failą",
"failą",
"m2v failo plėtinys",
"pratęsimas",
"failą"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"M2V failo formatas – MPEG-2 vaizdo įrašas",
   "description":"Sužinokite apie M2V MPEG-2 vaizdo failų formatą ir API, kurios gali kurti ir atidaryti M2V failus.",
   "linktitle":"M2V",
   "menu":{
      "docs":{
         "identifier":"video-m2v-lt",
         "parent":"video"
}
},
   "lastmod":"2023-10-11"
}

## Kas yra M2V failas?

M2V failo formatas yra failo plėtinys, paprastai siejamas su **MPEG-2 Video**. MPEG-2 yra plačiai naudojamas vaizdo glaudinimo standartas, dažnai naudojamas DVD, skaitmeninės televizijos transliavimui ir kitiems vaizdo platinimo būdams. M2V formate yra tik vaizdo duomenys, o tai reiškia, kad jame nėra garso ar kitų daugialypės terpės komponentų. Iš esmės tai yra neapdorotas arba elementarus vaizdo įrašo srautas.

M2V failai gali būti naudojami įvairiems tikslams, įskaitant DVD kūrimą arba vaizdo turinio kūrimą transliacijai. Pavyzdžiui, kuriant DVD, M2V vaizdo srautas paprastai suporuojamas su atskiru garso failu tokiais formatais kaip [AC3](/audio/ac3/) arba LPCM, kad būtų sukurtas visas DVD vaizdo įrašas.

Jei norite naudoti M2V failus vaizdo įrašų redagavimo ar kūrimo programinėje įrangoje, gali tekti juos sujungti su atitinkamu garso failu, sukurti meniu ir struktūrizuoti turinį, skirtą DVD kūrimui ar kitam platinimo formatui.

M2V failai paprastai nėra skirti tiesioginiam atkūrimui daugelyje daugialypės terpės grotuvų ar vaizdo redagavimo programinės įrangos, nes jiems trūksta garso ir kitų būtinų komponentų, kad būtų galima visapusiškai mėgautis vaizdo įrašais. Vietoj to, jie yra didesnio daugialypės terpės projekto arba platinimo paketo dalis.

## M2V charakteristikos

M2V failai, kurie yra MPEG-2 vaizdo standarto dalis, turi keletą svarbių savybių ir aspektų:

1.  **Vaizdo kodekas**: M2V failuose naudojamas MPEG-2 vaizdo kodekas, kuris yra plačiai priimtas ir nusistovėjęs glaudinimo standartas. MPEG-2 siūlo gerą vaizdo kokybę ir glaudinimo efektyvumą, todėl tinka įvairioms programoms, įskaitant DVD ir skaitmeninį transliavimą.
    
2.  **Nėra garso**: M2V failuose yra tik vaizdo komponentas, todėl jiems trūksta garso duomenų. Norint sukurti visą vaizdo failą, M2V failai dažnai suporuojami su atskirais garso failais, paprastai tokiais formatais kaip AC3 (Dolby Digital) arba LPCM (linijinio impulso kodo moduliacija).
    
3.  **Vaizdo įrašo kokybė**: M2V failo vaizdo kokybė gali skirtis atsižvelgiant į tokius veiksnius kaip bitų spartos ir raiškos nustatymai, naudojami koduojant. Didesnis pralaidumas ir raiška užtikrina geresnę vaizdo kokybę, bet ir didesnius failų dydžius.
       
4.  **DVD Authoring**: M2V files are commonly used in authoring of DVDs. DVD authoring software combines M2V video streams with separate audio tracks, menus and navigation features to create complete DVD video.
    
5.  **Bitrate Control**: M2V failo vaizdo srauto pralaidumas yra svarbus veiksnys. Tai turi įtakos ir vaizdo kokybei, ir reikalingos saugyklos kiekiui. Didesnis pralaidumas užtikrina geresnę kokybę, bet didesnį failo dydį.
    
6.  **Krašto santykis**: M2V failai gali palaikyti skirtingus formato santykius, pvz., 4:3 (standartinis) arba 16:9 (plačiaekranis), atsižvelgiant į numatomą rodymo formatą.
    
7.  **Skyra**: vaizdo įrašo skiriamoji geba M2V faile gali skirtis. Įprasta skiriamoji geba yra 720 x 480 (standartinė raiška) ir 1920 x 1080 (didelė raiška).
    
8.  **Kadrų dažnis**: MPEG-2 vaizdo įrašą galima koduoti įvairiais kadrų dažniais, tačiau įprastas kadrų dažnis yra 29,97 kadrų per sekundę NTSC (Šiaurės Amerikos) vaizdo įrašams ir 25 kadrai per sekundę PAL (Europos) vaizdo įrašams.
    
9.  **Redagavimas**: M2V failus galima redaguoti naudojant suderinamą vaizdo redagavimo programinę įrangą, tačiau gali tekti iš naujo sujungti juos su garso takeliais ir kitais daugialypės terpės elementais, kad būtų sukurtas galutinis, išsamus vaizdo įrašas.

## M2V ryšys su daugialypės terpės formatais

M2V files, as MPEG-2 video streams, are related to several other multimedia formats and components within context of video authoring, playback and distribution. Here are some of key relationships:

1.  **Garso formatai (AC3, LPCM ir kt.)**: norint sukurti pilną vaizdo failą, M2V failai paprastai suporuojami su atskirais garso failais tokiais formatais kaip AC3 (Dolby Digital) arba LPCM (linijinio impulso kodo moduliacija). Šie garso formatai suteikia garso komponentą daugialypės terpės turiniui.
    
2.  **DVD Format (VOB)**: When authoring DVDs, M2V files, along with audio and other assets, are often combined into Video Object (VOB) format. VOB files contain video, audio, subtitles and menu information for DVD video discs.
    
3.  **Transport Stream (TS)**: Skaitmeninio transliavimo metu MPEG-2 vaizdo įrašas dažnai apvyniojamas transporto sraute (TS). Šis formatas apima vaizdo, garso ir metaduomenis, skirtus skaitmeninei televizijai transliuoti, ir naudojamas tokiose paslaugose kaip DVB (skaitmeninis vaizdo transliavimas) ir ATSC (pažangių televizijos sistemų komitetas).
    
4.  **Programų srautas (PS)**: Programų srauto formatas (PS) yra kitas konteineris, naudojamas MPEG-2 vaizdo, garso ir kitiems duomenims saugoti. Jis dažnai naudojamas vaizdo įrašams platinti ir saugoti.
    
5.  **MPG (MPEG) formatas**: .MPG failo plėtinys dažniausiai naudojamas MPEG-2 vaizdo failams, kuriuose gali būti ir vaizdo, ir garso, žymėti. M2V failai yra platesnio MPEG formato pogrupis, ypač sutelkiant dėmesį į vaizdo įrašą be garso.
    
6.  **VOB (vaizdo objektų) failai**: VOB failuose, kurie yra DVD vaizdo dalis, gali būti M2V vaizdo srautų. Kai kuriate DVD, vaizdo turinį VOB failuose dažnai sudaro M2V vaizdo įrašas ir pridedamas garso įrašas.
    
7.  **Vaizdo įrašų redagavimo programinė įranga**: vaizdo įrašų redagavimo programinė įranga, pvz., Adobe Premiere Pro, Final Cut Pro arba Sony Vegas, gali dirbti su M2V failais redagavimo tikslais. Redaktoriai sujungia M2V vaizdo įrašų srautus su garso ir kitais ištekliais, kad sukurtų užbaigtus vaizdo įrašų projektus.
    
8.  **Media grotuvai**: medijos leistuvai, pvz., VLC arba Windows Media Player, paprastai netinka tiesiogiai leisti M2V failus, nes juose trūksta garso. Šie grotuvai skirti valdyti įprastesnius daugialypės terpės formatus, tokius kaip AVI, MP4 arba MKV, kuriuose yra ir vaizdo, ir garso.
    
9.  **Blu-ray formatas (M2TS)**: nors ir nėra tiesiogiai susijęs su M2V, M2TS formatas dažniausiai naudojamas didelės raiškos vaizdo įrašams Blu-ray diskuose. M2TS failuose gali būti MPEG-2 vaizdo srautų, taip pat H.264 arba VC-1 vaizdo srautų, taip pat įvairių garso formatų.
    
10.  **Vaizdo įrašų glaudinimo standartai**: MPEG-2 vaizdo įrašas, naudojamas M2V failuose, yra susijęs su kitais vaizdo glaudinimo standartais, tokiais kaip MPEG-4 (įskaitant H.264 ir H.265) ir VP9, kurie siūlo geresnį glaudinimo efektyvumą. ir vaizdo kokybė. Šie standartai naudojami skaitmeniniam srautiniam perdavimui, internetiniam vaizdo įrašui ir naujesniems optinių diskų formatams, pvz., Blu-ray.

## Kaip atidaryti M2V failą?

Programos, kurios atidaro M2V failus, apima

- VLC medijos grotuvas (keli platforma)
- Apple QuickTime Player (Mac)
- Nullsoft Winamp
– CyberLink PowerDVD 21.
- Windows Media Player (Windows)
- Klasikinis medijos leistuvas (Windows)

## Nuorodos
* [Vaizdo įrašo failo formatas](https://en.wikipedia.org/wiki/Video_file_format)


