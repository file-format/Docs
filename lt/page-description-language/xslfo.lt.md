{
  "date": "2019-10-11",
  "keywords": [
"XSLFO",
"XSL formatavimo objektai",
"Failas",
"Pratęsimas",
"Dokumento formatas",
"Išplečiamos stiliaus lentelės kalba"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XSLFO",
  "description": "Sužinokite apie XSLFO failo formatą ir API, kurios gali kurti ir atidaryti XSLFO failus.",
  "linktitle": "XSLFO",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-xslf-lto"
}
},
  "lastmod": "2021-04-23"
}

## Kas yra XSL-FO failas? ##

XSL-FO (XSL formatavimo objektai) yra galinga stilių lentelės kalba, skirta XML dokumentams formatuoti. Apribotos popieriaus ir spaudos formos semantiką išreiškia XSL-FO, kai matmenys yra fiksuoti. Priešingai nei HTML, kuris atspindi neribotos naršyklės lango formos semantiką su kintamaisiais matmenimis. XSL-FO formatuoti XML dokumentai dažniausiai naudojami PDF failams generuoti. XSL (Extensible Stylesheet Language) yra W3C technologijų rinkinys, skirtas XML dokumentams formatuoti ir keistis bei šios kalbos XSL-FO dalimi. XSLT ir XPath taip pat yra kitos XSL dalys.

Siūloma XML dokumentus pirmiausia paversti XSL-FO, PDF yra šio kriterijaus pavyzdys. PDF formatu rezultatai pateikiami naudojant XSLTfirst, o tada XSL-FO formatatorių. Tokiu būdu XML dokumentai gali būti formatuojami atsitiktinai. Nors XSL-FO naudojasi pakopinio stiliaus lapo (CSS) ypatybių naudojimo pranašumais ir išplečiant jas, kai tik reikia realiam formatui, jame yra puslapių šablonų, vadinamų puslapių šablonais pagal XSL-FO terminologiją. XSL-FO taip pat suteikia formatavimą gana sudėtingiems dokumentams ir palaiko rodyklės generavimą.

## Istorija ir pagrindinės sąvokos ##

2012 m. sausio mėn. paskutinį kartą buvo atnaujintas XSL-FO darbo projektas, o 2013 m. lapkritį jo darbo grupė buvo uždaryta. XSL stiliaus lentelė nurodo XML dokumentų klasės pateikimą aprašant, kaip klasės egzempliorius transformuojamas į XML dokumentą, kuriame naudojamas formatavimo žodynas. XSL-FO yra integruota pateikimo kalba ir neturi semantinių žymėjimų, kurie naudojami HTML. Be to, ši kalba saugo visus dokumento duomenis savyje, priešingai nei CSS, kuri pakeičia numatytuosius išorinio HTML arba XML dokumento nustatymus.

Bendrieji XSL-FO naudojimo kriterijai yra tai, kad vartotojas rašo dokumentą XML kalba, o ne rašo FO. Po to įvyksta XSLT transformacija. Ši XSLT transformacija yra atsakinga už XML konvertavimą į XSL-FO. Kai tik sugeneruojamas XSL-FO dokumentas, jis perduodamas programai, vadinamai FO procesoriumi. FO procesoriai yra atsakingi už šio dokumento pavertimą skaitomu ir spausdinamu dokumentu. PDF failai arba PS yra dažniausiai pasitaikančios XSL-FO išvesties pavyzdžiai. Tačiau tai nereiškia, kad FO procesorius gali gaminti tik šių dviejų tipų formatus kaip išvestį. Kai kurie FO procesoriai gali išvesti RTF failus arba net gali atsirasti langas vartotojo GUI, šiame lange rodoma puslapio seka ir jų turinys.

XSL-FO dokumentas skiriasi nuo PDF ar PS ta prasme, kad galiausiai jis neapibrėžia teksto išdėstymo skirtinguose puslapiuose. Galbūt ji formuoja puslapių stilių ir nustato vietas, kuriose bus rodomas turinys. Be to, FO procesorius sutvarko tekstą FO dokumente nurodytose ribose. Ši specifikacija netgi leidžia skirtingiems FO procesoriams elgtis atitinkamai pagal gautus puslapius. Tokio elgesio pavyzdys yra brūkšnelis, kai kurie FO procesoriai gali brūkšninti žodžius, kad sutaupytų vietos, kai eilutė nutrūksta, o kai kurie procesoriai šios parinkties nepasirenka. Nuo procesorių priklauso, ar jie pasirenka skirtingus brūkšnelių algoritmus, atitinkančius jų reikalavimus. Šie brūkšnelių algoritmai gali būti labai paprasti arba sudėtingesni. Kai kuriose situacijose XSL-FO specifikacija aiškiai apriboja FO procesorius, tam tikru mastu pasirenkant išdėstymą.

Dėl šių FO procesorių skirtumų gaunami skirtingi rezultatai, dėl kurių procesoriai dažnai nesirūpina. Kadangi XSL-FO pagrindinis dėmesys skiriamas puslapių / spausdintų dokumentų gamybai. Patys XSL-FO dokumentai paprastai veikia kaip tarpininkai, jų pagrindinė funkcija yra sukurti PDF failus arba dokumentą, kurį galima atspausdinti kaip platinamą išvestį. Naudojant HTML/CSS arba XSL-FO, PDF paskirstymas kaip galutinis rezultatas, o ne formatavimo kalbos įvedimas rodo, kad imtuvai lieka nepaveikti dėl gaunamo universalumo, atsirandančio dėl formatavimo kalbos vertėjų skirtumų. Kita vertus, akivaizdu, kad nėra lengvo būdo, kaip dokumentas gali patenkinti įvairius gavėjų poreikius, pvz., kintamo puslapio dydžio ar pageidaujamo šrifto dydžio, arba pritaikymo puslapiui ar spaudiniui.

## XSLFO failo formatas ##

SL-FO dokumentai iš esmės yra XML dokumentai, tačiau jie neatitinka jokios schemos. Vietoj to SL-FO dokumentai laikosi sintaksės, apibrėžtos jų kalbos specifikacijoje. Kiekviename XSL-FO dokumente turi būti dvi dalys:

1. Skyrius, kuriame nurodomas etiketėmis pažymėtų puslapių maketų sąrašas.
1. Skyrius su visa išsamia dokumento duomenų informacija su žymėjimu, kuris nustato turinio rodymą skirtinguose puslapiuose, naudojant įvairius puslapių išdėstymus.

Puslapio ypatybės minimos puslapių maketuose, kurie gali apibrėžti teksto organizavimą, kad atitiktų konkrečios kalbos taisykles. Be to, puslapio dydis, jų paraštės ir puslapių sekos (kurios nustato skirtingas nelyginių ir lyginių puslapių savybes) taip pat apibrėžiami puslapių maketuose.

Dokumento duomenų dalis yra padalinta į srautų seriją, kur kiekvienas srautas yra susietas su puslapio išdėstymu. Srautai apima juose esančių blokų sąrašą. Šiame blokų sąraše gali būti įterptųjų žymėjimo funkcijų arba tekstinių duomenų sąrašo, o gal ir abiejų vienu metu. Dokumento paraštėse taip pat gali būti rodomi puslapių numeriai arba skyrių antraštės. Tiek blokų, tiek įterptinių elementų funkcionalumas išlieka toks pat kaip ir CSS, tačiau kai kurios užpildymo ir paraštės taisyklės skiriasi FO ir CSS.

The page orientation direction is entirely specified for the extension of blocks and inlines, thus making FO documents perform under the languages different from English. The language of the FO specification uses the words start and end rather than left and right for directions description. XSL-FO's basic content markup and cascading rules are taken from CSS. XSL-FO's language agrees to the following specifications.

## Keli stulpeliai ##

Puslapyje gali būti keli stulpeliai ir blokai ir pagal numatytuosius nustatymus jis gali tęstis iš vieno stulpelio į kitą. Keli puslapiai gali turėti skirtingą plotį ir stulpelių skaičių. Visos FO charakteristikos atitinka kelių stulpelių puslapio ribas.

### Sąrašai ###

XSL-FO sąrašas sudaromas dviem blokų rinkiniais, išdėstytais skruostais pagal žandikaulį. Konceptualiai, sąraše esantis blokas kairėje nurodo skaičių, ženklelį arba teksto eilutę, o dešinysis blokas gali veikti taip, kaip tikėtasi. XSL-FO sąrašų numeracija paprastai atliekama naudojant XSLT.

### Lentelės ###

FO lentelė yra panaši į HTML/CSS lentelę. Vartotojas gali pasirinkti kiekvienos atskiros ląstelės duomenų eilutes, stiliaus informaciją, fono spalvą. Naudodamas atskirą stiliaus informaciją, vartotojas turi teisę pasirinkti pirmąją eilutę kaip lentelės antraštės eilutę. FO procesorius gali būti aiškiai informuotas apie kiekvieno stulpelio vietos specifikaciją arba automatiškai pritaikyti tekstą lentelėje.

### Indeksavimas ###

XSL-FO 1.1 turi funkcijų, kurios padeda sugeneruoti indeksą nurodant tinkamai pažymėtus elementus.

### Privalumai ###

* Tinka leidybai pagal turinį

* Lengvas naudojimas

* Žema kaina


## Nuorodos Nr.

* [Kas yra XSL-FO?](https://www.xml.com/articles/2017/01/01/what-is-xsl-fo/)

* [XSL formatavimo objektai](https://en.wikipedia.org/wiki/XSL_Formatting_Objects)


