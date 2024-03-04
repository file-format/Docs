{
   "date":"2023-10-18",
   "keywords":[
"cpi",
"cpi failą",
"cpi avchd vaizdo klipo informacijos failas",
"kaip atidaryti cpi failą",
"failą",
"cpi failo plėtinys",
"pratęsimas",
"failą"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"CPI failo formatas – AVCHD vaizdo klipo informacija",
   "description":"Sužinokite apie CPI AVCHD vaizdo klipo informacijos failo formatą ir API, kurios gali kurti ir atidaryti CPI failus.",
   "linktitle":"CPI",
   "menu":{
      "docs":{
         "identifier":"video-cpi-lt",
         "parent":"video"
}
},
   "lastmod":"2023-10-18"
}

## Kas yra CPI failas?

CPI reiškia Clip Information ir yra naudojamas metaduomenims apie atskirus vaizdo įrašus saugoti AVCHD katalogo struktūroje. Šiuose .CPI failuose yra informacijos apie vaizdo klipus, pvz., kiekvieno klipo pradžios ir pabaigos laikas, vaizdo įrašo formatas (raiška, kadrų dažnis ir kt.) ir kita informacija.

.CPI failai paprastai saugomi vaizdo kameros ar kito įrašymo įrenginio AVCHD katalogo struktūros poaplanke. Šie failai yra būtini norint tvarkyti ir atkurti vaizdo įrašus, nes juose pateikiama informacija, reikalinga programinei įrangai ir įrenginiams suprasti ir tinkamai rodyti vaizdo įrašų turinį.

## CPI failo formatas – daugiau informacijos

.CPI failuose AVCHD katalogų struktūrose yra svarbios informacijos apie vaizdo klipus, įrašytus AVCHD vaizdo kameromis arba įrenginiais. Štai keletas papildomos pagrindinės informacijos, kuri paprastai saugoma .CPI failuose:

1.  **Klipo informacija:** .CPI failuose saugoma išsami informacija apie atskirus vaizdo klipus, įskaitant jų pradžios ir pabaigos laiką. Ši informacija yra labai svarbi norint atkurti ir valdyti klipus.
    
2.  **Vaizdo įrašo formatas:** .CPI failuose yra duomenų apie klipuose naudojamą vaizdo įrašo formatą, įskaitant skiriamąją gebą, kadrų dažnį ir kraštinių santykį. Ši informacija reikalinga norint tinkamai rodyti vaizdo įrašą.
    
3.  **Garso formatas:** informacija apie klipuose naudojamą garso formatą, pvz., garso kanalų skaičius, atrankos dažnis ir kodekas, paprastai saugoma .CPI failuose.
    
4.  **Timestamps:** .CPI files may include timestamps for each clip, allowing users to organize and sort clips by recording date and time.
    
5.  **Failo struktūra:** AVCHD katalogų struktūras dažnai sudaro .MTS arba .M2TS vaizdo failų ir .CPI klipų informacijos failų ir .CPI failų derinys, padedantis susieti vaizdo ir garso turinį su metaduomenimis.
    
6.  **Scenos aptikimas:** kai kuriuose .CPI failuose saugoma scenos aptikimo informacija, kuri padeda nustatyti perėjimus tarp įrašytos filmuotos medžiagos scenų. Tai gali būti naudinga redaguojant vaizdo įrašą.
    
7.  **Miniatūros vaizdai:** kai kuriuose .CPI failuose gali būti miniatiūrų vaizdų arba peržiūros kadrų, kuriuose pateikiamas kiekvieno vaizdo klipo vaizdinis vaizdas. Tai dažnai naudojama programinėje įrangoje ir įrenginiuose, kad būtų rodoma turinio peržiūra.
    
## Kaip atidaryti CPI failą?

.CPI failai paprastai nėra skirti vartotojams tiesiogiai atidaryti. Vietoj to, kai naudojate vaizdo grotuvus arba redaktorius, kad dirbtumėte su AVCHD vaizdo turiniu, saugomu .MTS failuose, susietas .CPI failas įkeliamas automatiškai, jei jis tinkamai susietas su MTS failu. Kitaip tariant, šie .CPI failai yra svarbūs užkulisiniai duomenys, padedantys vaizdo įrašų programinei įrangai suprasti ir valdyti susijusius vaizdo įrašus. Šis ryšys užtikrina, kad programinė įranga gali interpretuoti tokius dalykus kaip klipo informacija, vaizdo ir garso formatai bei laiko žymos, todėl jums bus lengviau naršyti ir redaguoti AVCHD vaizdo turinį.

Programos, kurios atidaro arba nurodo CPI failus, apima

– **Adobe Premiere Pro 2023** (nemokama bandomoji versija), skirta (Windows, Mac)
- **Kdenlive** (nemokama), skirta (Windows, Mac, Linux)

## Adobe Premiere Pro

Adobe Premiere Pro yra garsi profesionali vaizdo redagavimo programinė įranga, kuri ilgą laiką buvo pagrindinė filmų ir vaizdo įrašų gamybos pramonė. Jis siūlo patikimą vaizdo įrašų redagavimo, postprodukcijos ir turinio kūrimo įrankių rinkinį. Premiere Pro yra žinomas dėl savo nelinijinės redagavimo sistemos, leidžiančios redaktoriams savarankiškai dirbti su vaizdo ir garso takeliais, todėl tai yra lanksti ir galinga platforma. Jis siūlo platų funkcijų spektrą, įskaitant redagavimą pagal laiko juostą, kelių kamerų redagavimą ir įvairius vaizdo efektus bei perėjimus. Jo integravimas su kitomis Adobe Creative Cloud programėlėmis, tokiomis kaip After Effects ir Photoshop, supaprastina kūrybos procesą.

Premiere Pro spalvų korekcijos ir vertinimo įrankiai leidžia tiksliai valdyti vaizdo turinio estetiką. Programinė įranga taip pat apima garso redagavimo ir maišymo galimybes, leidžiančias vartotojams pagerinti savo projektų garso takelių kokybę.

## Kdenlive

Kdenlive yra atvirojo kodo vaizdo redagavimo programinė įranga, kuri siūlo patogią ir įvairiapusę platformą vaizdo įrašų kūrėjams. Ši programinė įranga suteikia nelinijinę redagavimo aplinką, leidžiančią vartotojams sklandžiai redaguoti vaizdo ir garso turinį laiko juostoje. Jis palaiko platų vaizdo ir garso formatų spektrą, todėl yra pritaikomas įvairiems projekto reikalavimams.

Kdenlive siūlo daugybę redagavimo įrankių, įskaitant perėjimus, efektus ir garso koregavimus. Jame taip pat yra pagrindinių kadrų animacija, skirta tiksliai valdyti projekto elementus. Nors tai gali būti ne tokia turtinga funkcijų, kaip kai kurie profesionalūs mokami sprendimai, tai yra patrauklus pasirinkimas turintiems biudžetą turinio kūrėjams arba tiems, kurie teikia pirmenybę atvirojo kodo programinei įrangai.

Programinės įrangos sąsaja yra intuityvi, todėl ji tinka tiek pradedantiesiems, tiek patyrusiems redaktoriams. Jį galima naudoti Linux, Windows ir MacOS, todėl užtikrinamas kelių platformų suderinamumas.

## Kiti CPI failai

Štai kiti failų tipai, kuriuose naudojamas **.cpi** failo plėtinys.

**Vaizdo įrašas ir sistema**
- [CPI - AVCHD Video Clip Information](/video/cpi/)
- [CPI - Codepage Information File](/system/cpi/)

## Nuorodos
* [Kdenlive](https://en.wikipedia.org/wiki/Kdenlive)


