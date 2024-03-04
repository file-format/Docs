{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WMV failo formatas",
  "description": "Sužinokite apie WMV failo formatą ir API, kurios gali kurti ir atidaryti WMV failus.",
  "linktitle": "WMV",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-wm-ltv"
}
},
  "lastmod": "2019-09-16"
}

## Kas yra WMV failas?

Išplėstinių sistemų formatas (ASF) yra skaitmeninis daugialypės terpės konteineris, pirmiausia skirtas medijos srautams saugoti ir perduoti. Microsoft Windows Media Video (WMV) yra suspausto vaizdo formatas, o Microsoft Windows Media Audio (WMA) yra suspausto garso formatas kartu su papildomais metaduomenimis ASF konteineryje, kurį sukūrė Microsoft. Kai WMV arba WMA failai yra užkoduoti naudojant Windows Media Video ir Windows Media Audio kodekus, jie pateikiami su plėtiniu .asf. WMV suglaudina didelius failus, kad būtų geresnis perdavimo greitis tinkle, kartu išlaikant vaizdo kokybę. WMV yra specialiai sukurtas veikti visuose Windows įrenginiuose. Kino ir televizijos inžinierių draugijai (SMPTE) standartizavus, WMV dabar laikomas atviru standartiniu formatu.

## Istorija ##

With the help of Microsoft proprietary codecs new compressed video format was developed in 1999 known as WMV7 which was based on MPEG-4 Part 2. Patobulinimai buvo papildyti dar dviejose versijose, ty WMV8 ir 9. Microsoft pateikė 9^^th^^ WMV versiją SMPTE standartizuoti 2003 m., kuri galiausiai buvo standartizuota 2006 m. kaip SMPTE 421M, taip pat žinoma kaip VC-1. WMV idėja buvo sukurti medijos formatą, kurį galėtų palaikyti visa Microsoft palaikoma aparatinė ir programinė įranga. Be to, kitas pagrindinis tikslas buvo perduoti vaizdo srautus internetu pagal optimalų scenarijų. Po SMPTE standartizacijos WMV taip pat tapo Blu-ray diskų vaizdo formatu.

## Failo formato specifikacijos

### Konteineris

Paprastai WMV yra supakuotas į ASF konteinerį, bet be to, Matroska arba AVI konteineris taip pat gali jį palaikyti su atitinkamai .mkv ir .avi plėtiniais.

### Windows Media Video 9

Nors Windows Media Video 9 serijoje yra įvairių garso ir vaizdo kodekų, skirtų skaitmeninės laikmenos kūrimui ir atkūrimui, WMV-9 kodekas yra naujausias ir geriausias vaizdo kodekas, nes jis gali pasiekti optimalų suspaudimą naudojant labai mažą bitų spartą, ty 160 x 120 10 Kb/s iki 1920 x 1080 4–8 Mb/s įvairiems HD vaizdo įrašams.

### Kodeko struktūra

WMV-9 turi 8 bitų 4:2:0 vidinį spalvų formatą. Kaip ir visi kiti populiarūs vaizdo glaudinimo standartai MPEG-1 ir H.261, WMV-9 naudoja bloku pagrįstą judesio kompensavimo ir erdvinio transformavimo schemą. Apskritai galime pasakyti, kad šie standartai atlieka bloko judesio kompensavimą iš ankstesnio rekonstruoto kadro, naudodami 2-D dydį, vadinamą judesio vektoriumi (MV), kad signalizuotų apie erdvinį poslinkį. Dabartinis blokas formuojamas numatant reikšmes iš tokio pat dydžio ankstesnio rekonstruoto kadro, kuris judesio vektoriumi yra išstumtas iš esamos padėties. Galų gale likutinė paklaida apskaičiuojama kaip skirtumas tarp numatomo bloko, kompensuoto judesio, ir tikrojo bloko. Ši liekamoji paklaida transformuojama naudojant tiesinę energiją sutankinančią transformaciją, tada kvantuojama ir užkoduojama entropija.

Quantized transform coefficients are entropy decoded, de-quantized, and inverse transformed to produce an approximation of the residual error on the decoder side, which is then added to the motion-compensated prediction to generate the reconstruction. The high-level description of the codec is shown in the following image.

Likusioje dalyje bus aptariami nauji WMV-9 patobulinimai, kurie išskiria jį nuo kitų vaizdo kodavimo sprendimų, tokių kaip MPEG standartai. WMV-9 turi vidinius (I), prognozuojamus (P) ir dvipusius prognozuojamus (B) kadrus. Vidiniai kadrai yra tie, kurie koduojami nepriklausomai ir nepriklauso nuo kitų kadrų. Numatyti kadrai yra kadrai, priklausantys nuo vieno kadro praeityje. Numatomo kadro dekodavimas gali įvykti tik po to, kai yra iškoduoti visi atskaitos kadrai prieš dabartinį kadrą, pradedant nuo paskutinio (I) kadro. B kadrai yra kadrai, turintys dvi nuorodas – vieną laikinoje praeityje ir kitą laikinoje ateityje. B kadrai perduodami po jų nuorodų, o tai reiškia, kad B kadrai siunčiami netvarkingai, siekiant užtikrinti, kad jų nuorodos būtų prieinamos dekodavimo metu. B kadrai WMV-9 nenaudojami kaip nuoroda į tolesnius kadrus. Taip B kadrai yra už dekodavimo kilpos ribų, todėl dekoduojant B kadrus galima naudoti sparčiuosius klavišus be dreifo ar ilgalaikių vaizdo artefaktų. Aukščiau pateiktas I, P ir B kadrų apibrėžimas galioja tiek progresinėms, tiek persipynusioms sekoms.

Vaizdo kodekų našumas lyginamas su jų greičio iškraipymo (RD) diagrama. Tai 2-D kreivė, rodanti iškraipymus, kuriuos sukelia suspaudimas esant tam tikram bitų greičiui.

WMV-9 išsprendė šią problemą įdiegdama įvairius toliau išvardytus metodus:

1. Adaptyvi bloko dydžio transformacija

2. Riboto tikslumo transformatorių rinkinys

3. Judesio kompensacija

4. Kvantizacija ir dekvantizacija

5. Išplėstinis entropijos kodavimas

6. Kilpų filtravimas

7. Išplėstinis B rėmelio kodavimas

8. Interlace kodavimas

9. Persidengimo lyginimas

10. Mažos kainos įrankiai

11. Išblukimo kompensacija

## Nuorodos

* [https://bytescout.com/blog/2018/02/windows-media-video-format.html](https://bytescout.com/blog/2018/02/windows-media-video-format.html )

* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)


