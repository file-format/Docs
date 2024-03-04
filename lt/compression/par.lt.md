{
   "date":"2023-07-18",
   "keywords":[
"PAR",
"PAR failas",
"kaip atidaryti par failą",
"failą",
"PAR failo plėtinys",
"pratęsimas",
"failą"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"PAR failo formatas – archyvo indekso failas",
   "description":"Sužinokite apie PAR formatą ir API, kurios gali kurti ir atidaryti PAR failus.",
   "linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par-lt",
         "parent":"compression"
}
},
   "lastmod":"2023-07-18"
}

## Kas yra PAR failas?

Parchive (PAR) archyvuose .par failas reiškia indekso failą, kuriame yra lyginumo tomų arba lyginumo blokų grupė. Šis indekso failas naudojamas klaidų aptikimo ir atkūrimo tikslais, kai vienas ar keli archyve esantys failai pametami arba sugadinami.

Archyvo archyvą paprastai sudaro ir originalūs duomenų failai, ir atitinkami pariteto tomai. Pariteto tūriai sukuriami naudojant Reed-Solomon klaidų taisymo algoritmus. Šiuose pariteto tomuose yra perteklinės informacijos, kurią galima naudoti norint atkurti pradinius duomenų failus.

.par faile, taip pat žinomame kaip pariteto tomų rinkinys, yra informacijos apie pariteto tomų struktūrą ir vietą archyve. Jis naudojamas kaip atkūrimo proceso rodyklė arba žemėlapis. Naudodama .par failą, specializuota PAR programinė įranga gali nustatyti, kokie pariteto tomai reikalingi ir kaip juos naudoti norint atkurti trūkstamus arba pažeistus failus.

Kai vienas ar daugiau archyvo archyvo failų tampa neprieinami arba sugadinami, .par failas gali būti naudojamas kartu su turimais lygiaverčiais tomais prarastiems duomenims atkurti. PAR programinė įranga nuskaito .par failą, identifikuoja trūkstamus arba sugadintus failus ir naudoja pariteto tomus jiems atkurti.

## Kaip atidaryti PAR failą?

Norėdami atidaryti ir naudoti .par failus, jums reikės specializuotos PAR programinės įrangos. Štai keletas populiarių programinės įrangos parinkčių, galinčių tvarkyti .par failus:

- **QuickPar:** QuickPar yra plačiai naudojama PAR programinė įranga, skirta Windows. Tai leidžia kurti, patikrinti ir taisyti PAR failus. Galite atidaryti .par failą programoje QuickPar, kad patikrintumėte jo vientisumą arba panaudotumėte jį pažeistiems ar trūkstamiems failams archyvo archyve taisyti.

- **MultiPar:** MultiPar yra dar viena populiari PAR programinė įranga, skirta Windows. Jis palaiko ir PAR, ir PAR2 failų formatus ir suteikia pažangių funkcijų archyvams kurti, tikrinti ir taisyti. MultiPar gali atidaryti .par failus ir atlikti klaidų aptikimo bei atkūrimo operacijas pagal pateiktus pariteto tomus.

- **MacPAR deLuxe:** MacPAR deLuxe yra PAR programinė įranga, sukurta specialiai MacOS. Jis palaiko PAR ir PAR2 failų formatus ir teikia panašias funkcijas kaip QuickPar ir MultiPar. MacPAR deLuxe gali atidaryti .par failus ir padėti patikrinti archyvus bei atkurti sugadintus arba trūkstamus failus.

## PAR failo formatas – daugiau informacijos

PAR failo formatas, paprastai vadinamas Parchive, yra specifinis failo formatas, naudojamas pariteto duomenims kurti ir klaidų aptikimui bei atkūrimui failų archyvuose. PAR failo formatas paprastai susideda iš trijų tipų: PAR, PAR2 ir PAR3.

- **PAR:** Originalus PAR failo formatas, taip pat žinomas kaip PAR1, buvo sukurtas projekto Parchive. Tai apima pariteto duomenis, sugeneruotus iš pradinių duomenų failų. PAR failai suteikia pagrindinį klaidų aptikimo ir atkūrimo lygį, tačiau turi trūkumų, susijusių su klaidų taisymo galimybėmis.

- **PAR2:** PAR2 yra patobulinta PAR failo formato versija. Ji siūlo pažangesnes klaidų taisymo galimybes ir patobulintas atkūrimo funkcijas. PAR2 failai paprastai naudojami pariteto duomenims kurti, kurie gali atkurti prarastus ar sugadintus failus archyve. PAR2 failai suteikia geresnę apsaugą nuo duomenų sugadinimo ir yra plačiai naudojami failų archyvavimo tikslais.

- **PAR3:** PAR3 is the latest version of the PAR file format and provides further improvements in error correction and recovery. It offers even higher levels of redundancy and error correction capabilities compared to PAR2. PAR3 failai sukurti siekiant suteikti patikimesnę archyvuose saugomų duomenų apsaugą ir atkūrimo parinktis.

Tiek PAR2, tiek PAR3 failų formatus plačiai palaiko PAR programinė įranga ir jie suteikia galimybę patikrinti failų vientisumą archyve ir atkurti prarastus ar sugadintus duomenis. PAR ir PAR2 failai vis dar dažniausiai naudojami, o PAR3 failai pamažu populiarėja dėl patobulintų klaidų taisymo galimybių.

## Nuorodos
* [Parchive](https://en.wikipedia.org/wiki/Parchive)


