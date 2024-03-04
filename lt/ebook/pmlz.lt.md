{
  "date": "2021-03-30",
  "keywords": [
"PMLZ",
"Suspaustas delno žymėjimo kalbos failas",
"pratęsimas",
"Failas",
"formatu",
"eBook",
"Palmių žymėjimo kalba"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie PMLZ failo formatą, Palm Markup Language ir API, kurios gali kurti ir atidaryti PMLZ failus.",
  "title": "PMLZ – suglaudintas delno žymėjimo kalbos failas",
  "linktitle": "PMLZ",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-pml-ltz"
}
},
  "lastmod": "2021-03-30"
}

## Kas yra PMLZ failas?

Palm Inc pristatė elektroninės knygos failo tipą; žinomas kaip PMLZ failo formatas, kuris yra suglaudinta [PML](/ebook/pml/) failo formato versija, todėl failai su plėtiniais .pmlz yra žinomi kaip **Zipped Palm Markup Language File**. PMLZ failas yra tik failo, sujungiančio [PDB](/programming/pdb/) failus, skirtus **eReader** (žinoma kaip el. knygų skaitymo įrenginys, pvz., planšetinis kompiuteris), dokumentams kurti. PML failas suteikia PDB failo (kuriame yra įvairių duomenų failų) išdėstymą, kad jis būtų rodomas Palm įrenginyje. PDB failas yra duomenų bazės failas, kurį naudoja įvairios programos, įskaitant Quicken, Pegasus, Microsoft Visual Studio ir Palm Pilot. Trumpai tariant, PMLZ yra suspaustas PML ir PDB failų konteineris.


## Žinios apie palmių žymėjimo kalbą
Šioje lentelėje nurodytos PML komandos:

|Komanda|Aprašymas|
---|---|
| \p | Naujas puslapis |
| \x | Naujas skyrius; taip pat sukelia naują puslapio lūžį. Skyriaus pavadinimą (ir bet kokius stiliaus kodus) pridėkite \x ir \x |
| \Xn | Naujas skyrius su įtrauka n lygių (n tarp 0 ir 4 imtinai) Skyriaus dialogo lange; nesukelia puslapio pertraukos. Pridėkite skyriaus pavadinimą (ir bet kokius stiliaus kodus) su \Xn ir \Xn |
| \Cn=Skyriaus pavadinimas | Į skyrių sąrašą įterpkite Skyriaus pavadinimą n lygiu (pvz., \Xn). Tekstas puslapyje nerodomas ir nėra priverstinio puslapio lūžio. Tai kartais gali būti naudinga įterpiant skyriaus ženklą, pavyzdžiui, skyriaus įvado pradžioje. |
| \c | Centruokite šį teksto bloką; uždaryti su \c eilutės pradžioje |
| \r | Teisingas lygiavimo teksto blokas; uždaryti su \r eilutės pradžioje |
| \i | Kursyvas blokas; uždaryti su \i |
| \u | Pabraukimo blokas; uždaryti su \u |
| \o | Overstrike blokas; uždaryti su \o |
| \v | Nematomas tekstas; uždaryti su \v (galima naudoti komentarams) |
| \t | Įtraukų blokas. Pradėkite nuo eilutės pradžios, uždarykite su \t eilutės pabaigoje |
| \T=50% | Įtraukia nurodytą ekrano pločio procentą, šiuo atveju 50%. Jei dabartinė piešimo vieta jau yra už nurodytos ekrano vietos, ši žyma nepaisoma. |
| \w=50% | Įdėkite horizontalią tam tikro ekrano pločio procentinę taisyklę, šiuo atveju 50%. Ši žyma sukelia eilutės lūžį prieš ir po jos. Taisyklė yra centre. Procento ženklas yra privalomas. |
| \n | Perjunkite į įprastą šriftą, kurį nurodo vartotojas |
| \s | Perjungti į stdFont; uždarykite su \s, kad grįžtumėte į įprastą šriftą |
| \b | Perjungti į boldFont; uždarykite su \b, kad grįžtumėte į įprastą šriftą (nenaudojamas; vietoj jo naudokite \B) |
| \l | Perjungti į didelį šriftą; uždarykite su \l, kad grįžtumėte į įprastą šriftą |
| \B | Pažymėti tekstą kaip paryškintą. Skirtingai nuo žymos \b, \B nekeičia šrifto, todėl galite turėti didelį paryškintą tekstą. Negalite maišyti \b ir \B tame pačiame PML faile. |
| \Sp | Pažymėkite tekstą kaip viršutinį indeksą. Negalima maišyti su kitais stiliais, pvz., pusjuodžiu šriftu, kursyvu ir pan. Viršuje pažymėtą tekstą pridėkite \Sp. |
| \Sb | Pažymėkite tekstą kaip apatinį indeksą. Negalima maišyti su kitais stiliais, pvz., pusjuodžiu šriftu, kursyvu ir t. t. Užrašykite tekstą su \Sb. |
| \k | Užduotą tekstą paverskite mažomis didžiosiomis raidėmis; uždaryti su \k. Bet kokie simboliai, esantys \k žymose (įskaitant tuos, kuriuose yra diakritinių ženklų), rašomi didžiosiomis raidėmis ir atvaizduojami mažesniu dydžiu nei įprasti didžiosios raidės. |
| \\ | Reiškia vieną pasvirąjį brūkšnį |
| \aXXX | Įterpkite ne ASCII simbolį, kurio Windows-1252 kodas yra dešimtainis XXX. Daugiau informacijos rasite PML simbolių lentelėje. |
| \UXXXX | Įterpkite ne ASCII simbolį, kurio Unikodo kodas yra šešioliktainis XXXX. Išsamesnės informacijos ieškokite išplėstinėje PML simbolių lentelėje. |
| \m=vaizdovardas.png | Įdėkite pavadintą paveikslėlį. Žiūrėkite žemiau esantį skyrių apie vaizdus. |
| \q=#linkanchorŠiek tiek teksto\q | Nurodykite nuorodos inkarą, kuris yra kitoje dokumento vietoje. Eilutė po inkaro specifikacijos ir prieš galinį \q yra pabraukta arba kitaip rodoma kaip nuoroda peržiūrint dokumentą. |
| \Q=linkanchor | Dokumente nurodykite nuorodos inkarą. |
| \- | Įdėkite minkštą brūkšnelį. Švelnus brūkšnelis rodomas tik tada, kai reikia pertraukti žodį per eilutę. |
| \Fn=footnote11\Fn | Susiekite 1 su išnaša, kurios pavadinimas yra išnaša1, pažymėta PML dokumento pabaigoje. Žr. toliau esantį skyrių apie išnašas ir šonines juostas. |
| \Sd=šoninė juosta1Šoninė juosta\Sd | Susiekite Šoninės juostos tekstą su šonine juosta, kurios pavadinimas yra šoninė juosta1, pažymėta PML dokumento pabaigoje. Žr. toliau esantį skyrių apie išnašas ir šonines juostas. |
| \I | Pažymėti kaip atskaitos indekso elementą. Indekso elementą (ir bet kokius stiliaus kodus) pridėkite \I ir \I.|


## Nuorodos

* [Palm Markup Language – MobileRead](https://wiki.mobileread.com/wiki/EReader)

* [E-Reader – MobileRead](https://en.wikipedia.org/wiki/E-reader)


