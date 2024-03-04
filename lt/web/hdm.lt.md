{
  "date": "2022-10-12",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HDM failas – delninio įrenginio žymėjimo kalbos failas",
  "description": "Sužinokite apie HDM failų formatą ir API, kurios gali kurti ir atidaryti HDM failus.",
  "linktitle": "HDM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-hd-ltm"
}
},
  "lastmod": "2022-10-12"
}

## Kas yra HDM failas?

HDM failas yra žymėjimo kalbos tinklalapio failas, sukurtas delninio įrenginio žymėjimo kalba (HDML). Jame yra žymėjimo žymų, panašių į [HTML](/web/html/) kalbą, tačiau ji skirta rankiniams elektroniniams įrenginiams, pvz., išmaniesiems telefonams ir delniniams kompiuteriams. [HDML file format specifications](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) buvo pateikti W3C standartizuoti, bet negalėjo tapti standartu. HDM yra pagrįstas [HDML](/web/hdml/) failo formato specifikacijomis, pasiekiamomis W3 svetainėje.

## HDM failo formatas – daugiau informacijos

HDM failą sudaro žymėjimo žymos, kurios pateikiamos vizualiai sukurtoje svetainėje delniniuose įrenginiuose. HDM failai nukopijuojami į įrenginius naudojant HDTP (Handheld Device Transport Protocol) protokolą, o ne HTTP protokolą, kuris naudojamas HTML puslapiams.

## HDML failo elementai

Toliau pateikiamas elementų, kurie suteikia HDML vykdymo laiko aplinką ir kurie yra vadinami vartotojo agentu, sąrašas.

|Elementas|Aprašymas|
---|---|
|Kortelės|Tai pagrindinė HDML sudedamoji dalis, kuri rodo ir leidžia vartotojui sąveikauti su informacijos kortelėmis. |
|Decks|HDML kortelės yra sugrupuotos į kaladės. HDML paketas yra panašus į HTML puslapį, nes jis identifikuojamas URL [RFC1738] ir yra turinio vienetas, kurio prašoma iš serverio ir kurį talpykloje saugo vartotojo agentas.|
|Veiksmai|Veiksmai gali būti PREV, SOFT1-SOFT8 ir HELP tipo. Jie yra abstraktūs ir palaikomi vartotojo sąsajoje pagal vartotojo agentą.|
|Veikla|Veikla yra tarsi susijusių kortelių grupė, kuri atlieka vieną loginę funkciją. Jie gali apimti vieną ar daugiau denių. HDML naršymo ir būsenos modelis yra suskirstytas į veiklą.|
|Istorija pagrįsta navigacija|Vartotojo agentas saugo vartotojui rodomų kortelių istoriją. Kiekviena atverta kortelė įtraukiama į kortelių istoriją. Vartotojo agentas leidžia vartotojui lengvai pereiti prie ankstesnės istorijos kortelės.|

## Nuorodos

* [HDML – Vikipedija](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)

* [HDML specifikacijos – W3 mokyklos](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)


