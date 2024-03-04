{
  "date": "2023-07-12",
  "keywords": [
"mpeg",
"mpeg failą",
"kas yra mpeg failas",
"Kaip atidaryti mpeg failą",
"failą",
"mpeg failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "MPEG failo formatas – MPEG vaizdo įrašas",
  "description": "Sužinokite apie MPEG formatą ir API, kurios gali kurti ir atidaryti MPEG failus.",
  "linktitle": "MPEG",
  "menu": {
    "docs": {
      "identifier": "video-mpeg-lt",
      "parent": "video"
}
},
  "lastmod": "2023-07-12"
}

## Kas yra MPEG failas?

MPEG failas, taip pat žinomas kaip MPEG vaizdo failas, yra skaitmeninio vaizdo failo formatas, kuriame vaizdo glaudinimui naudojami judančių paveikslėlių ekspertų grupės (MPEG) standartai. MPEG yra plačiai naudojamas vaizdo duomenų saugojimo ir perdavimo formatas.

MPEG formatu naudojamas nuostolingas glaudinimas, o tai reiškia, kad tam tikra informacija atmetama siekiant sumažinti failo dydį. Ši glaudinimo technika leidžia efektyviai saugoti ir transliuoti vaizdo turinį, išlaikant priimtiną vaizdo kokybę. Yra keletas MPEG standarto versijų, įskaitant MPEG-1, MPEG-2, MPEG-4 ir MPEG-7, kurių kiekviena turi skirtingą glaudinimo ir kokybės lygį.

MPEG failai paprastai turi failo plėtinį .mpeg arba .mpg. Juose gali būti ir vaizdo, ir garso duomenų, dažnai sujungtų į vieną failą. MPEG failai yra suderinami su daugybe daugialypės terpės grotuvų ir vaizdo įrašų redagavimo programinės įrangos, todėl jie yra populiarus pasirinkimas dalijantis ir platinant vaizdo įrašų turinį.

## Kaip atidaryti MPEG failą?

Yra daug programinės įrangos programų, kurios gali atidaryti ir leisti MPEG failus. Štai keletas populiarių parinkčių:

- VLC Media Player
- Windows Media Player.
- QuickTime grotuvas
- MPC-HC
- GOM grotuvas
- MPlayer
- PotPlayer
- Kodi

## Kaip konvertuoti MPEG failą?

Yra daugybė vaizdo įrašų programų, įskaitant VideoLAN VLC medijos leistuvą, HandBrake ir Apple QuickTime Player, galinčių konvertuoti MPEG failus į kitus formatus. Pavyzdžiui, VLC gali konvertuoti MPEG failus į šiuos formatus

- MP4
- AVI
- MKV
- MOV
- WMV
- FLV

## MPEG failų vidinės struktūros apžvalga

Vidinė MPEG failų struktūra susideda iš skirtingų komponentų ir duomenų struktūrų, kurios tvarko ir saugo vaizdo, garso ir kitą susijusią informaciją. Čia pateikiama pagrindinių MPEG failų vidinės struktūros elementų apžvalga:

- **Sistemos sluoksnis:**

Sistemų sluoksnis apibrėžia bendrą MPEG failo struktūrą. Tai apima antraštes, programų srautus ir kitus su sistema susijusius duomenis, reikalingus dekodavimui ir atkūrimui. Sistemų sluoksnis yra atsakingas už elementarių srautų sinchronizavimo ir tankinimo valdymą.

– **Elementarieji srautai:**

MPEG failuose yra atskiri pagrindiniai vaizdo, garso ir kitų duomenų srautai. Kiekvienas elementarus srautas neša suspaustus duomenis, būdingus jo tipui. Pavyzdžiui, vaizdo elementariame sraute yra suspausti vaizdo kadrai, o elementariame garso sraute yra suspausti garso pavyzdžiai.

- **Vaizdo įrašo suspaudimas:**

MPEG vaizdo įrašų glaudinimo būdai, tokie kaip vidinis ir tarpkadras, naudojami failo dydžiui sumažinti, išlaikant vaizdo kokybę. Suspausti vaizdo kadrai yra suskirstyti į paveikslėlių grupes (GOP), kurias sudaro vidinis koduotas (I), numatomas (P) ir dvikryptis (B) kadras.

- **Garso suspaudimas:**

MPEG failai palaiko įvairius garso suspaudimo kodekus, tokius kaip MP3, AAC arba MPEG-1 Audio Layer II. Garso pavyzdžiai suglaudinami naudojant šiuos kodekus, leidžiančius efektyviai saugoti ir perduoti garso duomenis.

- ** Sinchronizavimas ir laikas:**

MPEG failai naudoja laiko žymes ir sinchronizavimo informaciją, kad būtų užtikrintas tinkamas vaizdo ir garso srautų suderinimas atkūrimo metu. Šios laiko žymos padeda palaikyti sinchronizavimą ir užtikrina tikslų garso ir vaizdo kadrų dekodavimo ir atvaizdavimo laiką.

- **Metaduomenys:**

MPEG failuose gali būti metaduomenų, kurie suteikia papildomos informacijos apie vaizdo ir garso turinį. Šiuose metaduomenyse gali būti tokios informacijos kaip pavadinimas, autorius, sukūrimo data ir kita aprašomoji informacija.

- **Paketai ir paketų antraštės:**

MPEG failai suskirsto duomenis į paketus. Kiekviename pakete yra pakuotės antraštė, kurioje pateikiama informacija apie paketo turinį, pvz., srauto tipas, paketo dydis ir laiko informacija.

- **Programos specifinė informacija (PSI):**

PSI yra MPEG failų skyrius, kuriame pateikiama papildoma informacija apie programų srautus, pvz., programos ir srauto identifikatoriai, srauto tipas ir aprašai. PSI padeda iššifruoti ir demultipleksuoti elementarius srautus faile.

- **Transporto srautas:**

MPEG-2 yra specialus transportavimo srauto formatas, naudojamas vaizdo turiniui transliuoti ir perduoti. Transporto srautas sujungia kelias programas į vieną srautą, leidžiantį efektyviai perduoti ir sinchronizuoti garso, vaizdo ir kitus duomenis tinklais.

## MPEG failo formatas – daugiau informacijos

Štai keletas svarbių dalykų, kuriuos reikia žinoti apie MPEG failo formatą:

-**Suspaudimas:**

MPEG failai naudoja nuostolingo glaudinimo metodus, kad sumažintų failo dydį, išlaikant tinkamą vaizdo kokybę. Suspaudimo dydis gali skirtis priklausomai nuo MPEG versijos ir naudojamų nustatymų.

- **Vaizdo ir garso įrašai:**

MPEG failuose gali būti ir vaizdo, ir garso duomenų. Vaizdo duomenys suglaudinami naudojant MPEG standartus, o garsas gali būti suglaudintas naudojant įvairius garso kodekus, tokius kaip MP3 arba AAC.

- **MPEG versijos:**

   There are different versions of the MPEG standard, including MPEG-1, MPEG-2, MPEG-4, and MPEG-7. Each version has its own specifications, capabilities, and levels of compression. MPEG-1 is commonly used for VCDs (Video CDs), while MPEG-2 is used for DVDs and broadcast television. MPEG-4 is widely used for online video streaming, and MPEG-7 focuses on multimedia content description and metadata.

- **Failų plėtiniai:**

MPEG failai paprastai turi failų plėtinius .mpeg arba .mpg. Tačiau gali būti įvairių variantų ir plėtinių, pvz., .mp4 MPEG-4 failams arba .mp3 MPEG-1 garso sluoksnio 3 failams.

- **Kelių platformų suderinamumas:**

MPEG failus plačiai palaiko įvairūs medijos leistuvai, operacinės sistemos ir įrenginiai. Juos galima žaisti Windows, Mac ir Linux sistemose, taip pat išmaniuosiuose telefonuose, planšetiniuose kompiuteriuose ir išmaniuosiuose televizoriuose.

- **Redagavimas:**

MPEG failus galima redaguoti naudojant vaizdo redagavimo programinę įrangą. Tačiau, kadangi MPEG naudoja nuostolingą glaudinimą, pakartotinis failo redagavimas ir perkodavimas gali pabloginti kokybę. Prieš atliekant išsamų redagavimą, dažnai rekomenduojama dirbti su neprarandančiais formatais arba pasidaryti atsargines kopijas.

- **Srautas:**

MPEG failai dažniausiai naudojami vaizdo turiniui srautiniu būdu perduoti internetu. MPEG-4 ypač populiarus internetinėse vaizdo įrašų platformose ir vaizdo įrašų bendrinimo svetainėse dėl efektyvaus glaudinimo ir gero kokybės ir dydžio santykio.

– **Kilstantys standartai:**

MPEG standartai ir toliau tobulinami, kad neatsiliktų nuo technologijų pažangos. Naujesnės versijos ir variantai, pvz., MPEG-4 10 dalis (taip pat žinomas kaip H.264 arba AVC) ir MPEG-4 14 dalis (MP4), siūlo patobulintą glaudinimo efektyvumą ir pažangias funkcijas, pvz., didelės raiškos vaizdo įrašus ir 3D turinį.

– **Multimedijos programos:**

MPEG failai randa taikomąsias programas įvairiose srityse, įskaitant skaitmeninę televiziją, srautinio perdavimo paslaugas, vaizdo konferencijas, vaizdo stebėjimą, daugialypės terpės pristatymus ir kt.

## MPEG prieš kitus formatus

Lyginant MPEG failo formatą su kitais vaizdo formatais, atsižvelgiama į kelis veiksnius, įskaitant glaudinimo efektyvumą, suderinamumą, funkcijas ir palaikymą. Štai MPEG palyginimas su kai kuriais populiariais vaizdo įrašų formatais:

### MPEG vs. AVI (garso vaizdo įrašas)

-**Suspaudimas:**
   
MPEG failai paprastai pasižymi didesniu glaudinimo efektyvumu, palyginti su AVI, todėl failai yra mažesni.

- **Suderinamumas:**

AVI failus plačiai palaiko įvairūs medijos leistuvai, tačiau MPEG failai yra labiau suderinami įvairiuose įrenginiuose ir platformose.

- **Funkcijos:**

MPEG failai dažnai palaiko pažangesnes funkcijas, tokias kaip keli garso takeliai, subtitrai ir skyriai, o AVI tokios funkcijos palaiko ribotą.

- **Vaizdo įrašo kokybė:**

Priklausomai nuo glaudinimo nustatymų, MPEG ir AVI gali pasiekti panašią vaizdo kokybę, tačiau dėl pažangių glaudinimo metodų MPEG dažnai užtikrina geresnę kokybę esant mažesniam bitų dažniui.

### MPEG prieš WMV (Windows Media Video):

-**Suspaudimas:**

WMV failai paprastai pasižymi geresniu glaudinimo efektyvumu, palyginti su MPEG, todėl failai yra mažesni ir išlaikoma gera vaizdo kokybė.

- **Suderinamumas:**

MPEG failai turi didesnį suderinamumą įvairiuose įrenginiuose ir platformose, o WMV failai pirmiausia siejami su Windows sistemomis.

- **Funkcijos:**

Abu formatai palaiko daugybę funkcijų, įskaitant kelis garso takelius ir subtitrus, tačiau MPEG dažnai suteikia daugiau universalumo ir platesnį pažangių funkcijų palaikymą.

- **Vaizdo įrašo kokybė:**

Naudojant panašius glaudinimo nustatymus, MPEG ir WMV gali pasiekti panašią vaizdo kokybę, tačiau WMV gali veikti geriau tam tikrais atvejais dėl pažangių glaudinimo metodų.

### MPEG prieš MP4 (MPEG-4 14 dalis):

-**Suspaudimas:**

Tiek MPEG, tiek MP4 naudoja panašius glaudinimo būdus, o glaudinimo efektyvumas gali būti panašus. Tačiau MPEG-4 10 dalis (H.264/AVC) MP4 formate dažnai užtikrina geresnį suspaudimą nei senesni MPEG formatai.

- **Suderinamumas:**

Tiek MPEG, tiek MP4 yra plačiai suderinami įvairiuose įrenginiuose ir platformose. MP4 pastaraisiais metais įgijo didelį populiarumą dėl plataus palaikymo ir pritaikymo.

- **Funkcijos:**

MP4 siūlo daugiau išplėstinių funkcijų ir galimybių, įskaitant subtitrų, skyrių, interaktyvių meniu ir pažangių vaizdo kodekų, pvz., H.264 ir HEVC (H.265), palaikymą. MPEG-4 2 dalis (DivX, Xvid) MP4 taip pat palaiko išplėstines funkcijas.

- **Vaizdo įrašo kokybė:**

MPEG ir MP4 gali pasiekti panašią vaizdo kokybę, kai naudojami palyginami glaudinimo parametrai. Tačiau MP4 palaikymas pažangesniems vaizdo kodekams leidžia užtikrinti geresnę kokybę esant mažesniam bitų dažniui.

## Nuorodos
* [MPEG-1](https://en.wikipedia.org/wiki/MPEG-1)


