{
   "date":"2023-07-18",
   "keywords":[
"PAR",
"PAR failas",
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
   "title":"PAR failo formatas – FMS orlaivio parametrų failas",
   "description":"Sužinokite apie PAR formatą ir API, kurios gali kurti ir atidaryti PAR failus.",
   "linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"game-par-lt",
         "parent":"game"
}
},
   "lastmod":"2023-07-18"
}

## Kas yra PAR failas?

PAR failas, paprastai žinomas kaip orlaivio parametrų failas, yra specialiai naudojamas FMS (skraidančio modelio simuliatorius), skrydžio modeliavimo žaidime, sukurtame Windows operacinėms sistemoms. Jo tikslas yra saugoti svarbiausius duomenis apie lėktuvo geometriją ir fizines charakteristikas, įskaitant tokias savybes kaip masė, svorio centras ir inercijos momentai. Šie PAR failai yra svarbūs kuriant pritaikytus orlaivius žaidime, leidžiančius žaidėjams imituoti ir skristi savo unikalų virtualų orlaivį su tikslia ir tikroviška fizika.

## PAR failo formatas – daugiau informacijos

FMS yra programinė įranga, naudojama orlaiviuose, padedanti atlikti navigaciją, planuoti skrydį ir atlikti autopiloto funkcijas. FMS orlaivio parametrų faile, dažnai sutrumpintame kaip PAR failas, yra konkrečių duomenų, susijusių su orlaivio eksploatacinėmis savybėmis ir skrydžio valdymu.

Šis PAR failo formatas yra būdingas skrydžio modeliavimo programinei įrangai, pvz., naudojamai populiariose skrydžio treniruoklių programose, tokiose kaip Microsoft Flight Simulator arba X-Plane. Faile yra įvairių parametrų ir duomenų, kurie apibrėžia virtualaus orlaivio elgesį, našumą ir sistemas simuliatoriuje.

FMS orlaivio parametrų faile paprastai yra tokia informacija kaip:

– **Orlaivio specifikacijos:** Tai apima išsamią informaciją apie fizines orlaivio charakteristikas, pvz., svorį, matmenis, degalų talpą ir variklio specifikacijas.

– **Skrydžio našumo duomenys:** juose yra duomenys, susiję su orlaivio charakteristikomis įvairiomis skrydžio fazėmis, įskaitant pakilimą, kruizą, nusileidimą ir tūpimą. Tai gali apimti kilimo greitį, degalų sąnaudas, greičio apribojimus ir kitus su našumu susijusius parametrus.

– **Autopiloto nustatymai:** faile gali būti nurodytas orlaivio autopiloto elgesys ir apribojimai, įskaitant autopiloto režimus, aukščio ir kurso apribojimus bei valdymo jautrumą.

– **Navigacijos duomenys:** gali apimti su navigacija susijusių parametrų, pvz., orlaivio navigacijos duomenų bazę, įskaitant maršruto taškus, oro kelius ir oro uosto duomenis.

Šiuos PAR failus paprastai kuria ir prižiūri orlaivių kūrėjai arba trečiųjų šalių entuziastai, siekiantys skrydžio treniruoklio programinėje įrangoje suteikti tikrovišką ir tikslią modeliavimo patirtį. Tada failai įkeliami į treniruoklį, kad būtų galima apibrėžti imituojamo orlaivio elgseną ir veikimo charakteristikas.

## PAR failų, 3D modelių, tekstūrų ir garsų vaidmuo skrydžio modeliavimo žaidimuose

PAR failai yra tik viena viso orlaivio duomenų paketo dalis. Be PAR failų, yra keletas kitų failų, kurie kartu prisideda prie visiško orlaivio vaizdavimo žaidime. Šie papildomi failai paprastai apima 3D modelio failus, tekstūros bitmaps ir garsus.

– **3D modelio failai:**

Skrydžio modeliavimo žaidimams reikalingi detalūs 3D modeliai, kurie vizualiai atvaizduotų orlaivį virtualioje aplinkoje. Šiuos 3D modelius sudaro įvairūs komponentai, tokie kaip fiuzeliažas, sparnai, važiuoklė ir kitos sudėtingos orlaivio dalys. 3D modelio failai suteikia vizualinę struktūrą ir geometriją, reikalingą tiksliai pavaizduoti orlaivio išvaizdą ir formą žaidime.

– **Tekstūros taškinės schemos:**

Tekstūros bitų žemėlapiai, taip pat žinomi kaip tekstūros arba vaizdo žemėlapiai, naudojami spalvoms, paviršiaus detalėms ir vizualiniam tikroviškumui pridėti prie 3D modelių. Šiuose tekstūrų failuose yra tokios informacijos kaip dažų schemos, lipdukai, logotipai ir paviršiaus tekstūros, pvz., metalas, plastikas ar audinys. 3D modeliams pritaikius tekstūros bitmaps, žaidimo orlaivis gali būti vizualiai patobulintas, todėl patirtis yra įtraukesnė ir vizualiai patrauklesnė.

- **Garsai:**

Garso failai yra esminis skrydžio modeliavimo žaidimų elementas, nes jie suteikia garsinį grįžtamąjį ryšį ir tikroviškumą. Šie failai paprastai apima variklio garsus, kabinos garsus, aplinkos poveikį, pvz., vėją ar lietų, ir kitus orlaiviui būdingus garso signalus. Įtraukus atitinkamus garso failus, žaidimas gali tiksliai atkurti garso aplinką, susijusią su imituojamu orlaiviu, dar labiau sustiprindamas bendrą panardinimą.

Nors PAR faile yra konkrečių duomenų, susijusių su orlaivio veikimu ir skrydžio valdymu, tai yra PAR failų, 3D modelių failų, tekstūros bitmaps ir garso failų derinys, kuris kartu atgaivina virtualų orlaivį skrydžio modeliavimo žaidime. Kiekvienas failas tarnauja unikaliam tikslui sukurti visapusišką ir tikrovišką orlaivio vaizdą, užtikrinant žaidėjams įtraukiantį potyrį.

## Kaip atidaryti PAR failą?

Programos, kurios atidaro PAR failus, apima

- Skraidančio modelio simuliatorius (FMS)
- Microsoft Flight Simulator
- X lėktuvas

## Nuorodos
* [Flying-Model-Simulator (FMS)](https://modelsimulator.com/)

* [Microsoft Flight Simulator](https://en.wikipedia.org/wiki/Microsoft_Flight_Simulator)



