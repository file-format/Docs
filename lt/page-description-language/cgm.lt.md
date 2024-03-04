{
  "date": "2019-10-11",
  "keywords": [
"CGM",
"Kompiuterinės grafikos metafailas",
"Failas",
"Pratęsimas",
"Dokumento formatas",
"Vektorinė grafika",
"Metafailo aprašas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CGM failo formatas",
  "description": "Sužinokite apie CGM failo formatą ir API, kurios gali kurti ir atidaryti CGM failus.",
  "linktitle": "CGM",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-cg-ltm"
}
},
  "lastmod": "2021-04-23"
}

## Kas yra CGM failas? ##

Kompiuterinės grafikos metafailas (CGM) yra nemokamas, nuo platformos nepriklausomas, tarptautinis standartinis metafailo formatas, skirtas vektorinei grafikai (2D), rastrinei grafikai ir tekstui saugoti ir keistis. CGM vaizdams gaminti naudoja į objektą orientuotą metodą ir daugybę funkcijų nuostatų. CGM naudoja šias į objektą orientuotas charakteristikas grafiniams elementams perdaryti, kad būtų pateiktas vaizdas. Metafaile yra būtinos informacijos, kuri apibrėžia kitus failus. CGM teksto šaltinio faile yra visi grafiniai elementai, kuriuos vėliau galima sukompiliuoti į dvejetainį failą. Iš esmės CGM yra būdas palengvinti 2D grafinių duomenų mainus, nepriklausomai nuo konkrečios platformos ar įrenginio.

CGM formatas suteikia skirtingus elementus funkcijoms atlikti ir objektams žymėti, kad būtų galima koreguoti geometrinius primityvus ir grafinę informaciją. Nors CGM buvo pakeistas kitais grafikos vaizdų tinklalapiuose formatais, nes jis nėra gerai palaikomas tinklalapiuose, vis dar labai populiarus tarp pramonės, aeronautikos ir kitų techninių programų. Nors World Wide Web Consortium sukūrė WebCGM – alternatyvų CGM naudojimo internete metodą. Pirminis CGM diegimas buvo grafinės branduolio sistemos (GKS) pagrindinių operacijų sekos pavyzdys. Jis nebuvo labai pritaikytas profesionaliam dizainui, tačiau jį iš esmės išstūmė kiti formatai, tokie kaip DXF ir SVG.

## Istorija ##

1987 m. CGM pasirodė esąs tarptautinis standartas (ISO 8632-1987), JK BSI jį taip pat priėmė kaip nacionalinį standartą, o ANSI – JAV. Po kelių pakeitimų 1991 m. 1992 m. buvo išleistas peržiūrėtas CGM standartas (ISO 8632:1992). 2001 m. World Wide Web Consortium sukūrė WebCGM su patobulintomis galimybėmis naudoti su tinklalapiais. 2007 m. buvo išleista antroji WebCGM versija, o trečioji versija buvo išleista 2010 m. su patobulintomis galimybėmis.

## CGM failo formatas ##

Kompiuterinės grafikos metafailai iš esmės yra grafinės informacijos duomenų bazė ir suteikia grafinių duomenų fiksavimo, saugojimo ir perdavimo priemones. Vadinasi, turi būti grafinis sistemos komponentas duomenų bazei kurti kartu su metafailo formato programos vykdymu. Daugeliu atvejų šis komponentas yra Metafile generatorius. Be to, reikia kito komponento, kuris galėtų gauti, interpretuoti ir pateikti grafinius duomenis metafaile. Šį poreikį patenkina metafailų vertėjas. Toliau pateiktame paveikslėlyje pavaizduota grafinio metafailo darbo aplinka.

CGM ryšys su kitais tipinės grafikos sistemos komponentais parodytas aukščiau esančiame paveikslėlyje. Iš paveikslo taip pat matyti, kad metafailo funkcionalumas nepriklauso nuo galutinio įrenginio išvesties.

Generally, there are two categories of metafile: **section capture** and **picture capture**. The primary functionality of picture capture metafile is the capturing of device-independent, multiple picture definitions. While session capture metafiles use the system interface to capture the output dialogue in a graphical system. CGM belongs to the category of static picture capture metafiles. CGM provides a well-organized arrangement of components with a two-level structure.

1. Metafailo deskriptorius
1. Logiškai nepriklausomų vaizdų telkinys

Kiekviena nuotrauka yra paveikslėlio aprašų rinkinys ir paveikslėlio turinys, įskaitant paveikslėlio apibrėžimą. metafailo deskriptorius apibrėžia aprašomąją informaciją, kuri vienodai taikoma visoms to metafailo nuotraukoms. Ši informacija padeda vertėjui teisingai išanalizuoti metafailą ir atpažinti išteklius, reikalingus teisingam paveikslėlio atvaizdavimui. Nors paveikslėlio aprašas taip pat apima aprašomąją informaciją, jis gali atpažinti tik paveikslėlį, kuriame yra aprašas. Šiame failo formate kiekvienas paveikslėlio apibrėžimas yra savarankiškas ir logiškai nepriklausomas. Jie nepriklauso nuo visų kitų paveikslėlių apibrėžimų faile. Iškart po metadeskriptoriaus interpretacijos nuotraukos gali būti prieinamos ir interpretuojamos atsitiktinai. Ankstesnių nuotraukų būklės pasikeitimas neturi įtakos jų įpėdiniams. Ši vaizdo nepriklausomybė yra dar viena svarbi CGM savybė. CGM susideda iš koordinačių erdvės, kurios yra 2D Dekarto koordinatės, vadinamos virtualiojo įrenginio koordinatėmis ir gali būti pavaizduotos skaičiumi arba tikslumu, nurodant diapazoną ir detalumą. CGM nurodo ir tiesioginį spalvų pasirinkimą, ir pasirinkimą pagal indeksą. Pirmuoju atveju spalvų specifikaciją sudaro RGB trigubas, o vėliau spalvų specifikatorius nurodo indeksą į spalvų lentelę.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
