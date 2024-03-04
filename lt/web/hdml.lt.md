{
  "date": "2021-08-21",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Delninio įrenginio žymėjimo kalbos failas",
  "description": "Sužinokite apie HDML failo formatą ir API, kurios gali kurti ir atidaryti HDML failus.",
  "linktitle": "HDML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-hdm-ltl"
}
},
  "lastmod": "2021-08-21"
}

## Kas yra HDML failas?

Failas su plėtiniu .hdml (Handheld Device Markup Language) yra žymėjimo kalba, skirta kurti nešiojamų elektroninių įrenginių, pvz., delninių kompiuterių, išmaniųjų telefonų ir informacijos rodymo prietaisų, tinklalapius. Teigiama, kad HDML yra [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language) kalbos plėtinys. HDML yra panašus į HTML, bet skirtas belaidžiams ir delniniams įrenginiams, turintiems mažus ekranus, pvz., PDA, mobiliesiems telefonams ir pan. Jis buvo pakeistas WML, kuriam jis turėjo didelę įtaką.

## HDML failo formatas – daugiau informacijos

HDML yra delninių įrenginių žymėjimo kalba, pagrįsta žymėjimo žymomis, panašiomis į HTML. HDML buvo pateiktas W3C standartizuoti, tačiau jis niekada netapo standartu. Tačiau jo failo formato specifikacijas galima rasti adresu [W3 website](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html). [syntax for HDML language](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) yra kūrėjo nuoroda ir gali būti naudojamas pavyzdiniam programų kūrimui.

## HDML elementai

Toliau pateikiamas elementų, kurie suteikia HDML vykdymo laiko aplinką ir kurie yra vadinami vartotojo agentu, sąrašas.

|Elementas|Aprašymas|
---|---|
|Kortelės|Tai pagrindinė HDML sudedamoji dalis, kuri rodo ir leidžia vartotojui sąveikauti su informacijos kortelėmis. |
|Decks|HDML kortelės yra sugrupuotos į kaladės. HDML paketas yra panašus į HTML puslapį, nes jis identifikuojamas URL [RFC1738] ir yra turinio vienetas, kurio prašoma iš serverio ir kurį talpykloje saugo vartotojo agentas.|
|Veiksmai|Veiksmai gali būti PREV, SOFT1-SOFT8 ir HELP tipo. Jie yra abstraktūs ir palaikomi vartotojo sąsajoje pagal vartotojo agentą.|
|Veikla|Veikla yra tarsi susijusių kortelių grupė, kuri atlieka vieną loginę funkciją. Jie gali apimti vieną ar daugiau denių. HDML naršymo ir būsenos modelis yra suskirstytas į veiklą.|
|Istorija pagrįstas naršymas|Vartotojo agentas saugo vartotojui rodomų kortelių istoriją. Kiekviena atverta kortelė įtraukiama į kortelių istoriją. Vartotojo agentas leidžia vartotojui lengvai pereiti prie ankstesnės istorijos kortelės.|

## Nuorodos

* [HDML – Vikipedija](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)

* [HDML specifikacijos – W3 mokyklos](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)


