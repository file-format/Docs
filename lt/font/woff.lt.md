{
  "date": "2020-08-20",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WOFF - žiniatinklio atvirojo failo formatas",
  "description": "WOFF failas yra atviras šrifto formatas, sukurtas žiniatinklio atvirojo šrifto formatu.",
  "linktitle": "WOFF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-wof-ltf"
}
},
  "lastmod": "2020-09-30"
}

## Kas yra WOFF failas?

Failas su plėtiniu .woff yra žiniatinklio šrifto failas, pagrįstas žiniatinklio atvirojo šrifto formatu (WOFF). Jame yra konkretaus formato suglaudintas konteineris, pagrįstas TrueType (.TTF) arba OpenType (.OTT) šriftų tipais. WOFF buvo pristatytas siekiant atskirti žiniatinklio šriftus nuo šriftų failų, naudojamų darbalaukio programose. Be to, formatas, skirtas sumažinti šriftų perdavimo iš serverio į kliento kompiuterį tinkle delsą. Yra keletas įrankių, kurie gali konvertuoti WOFF failus į TTF ir kitus šriftų failų formatus.

## WOFF failo formatas

WOFF šrifto formatas suglaudina lentelėmis pagrįstų sfnt struktūrų šriftų duomenų lenteles, naudojamas įvairiuose šriftų tipuose, pvz., TrueType, OpenType ir Open Font Format. Tai tarsi šių šriftų tipų talpykla, kurioje taip pat galima įtraukti šrifto metaduomenis ir asmeninio naudojimo duomenis, kurie turi būti įtraukti į konteinerį. Konvertatoriai naudoja sfnt failus į WOFF formato failą, o vartotojo agentai atkuria užkoduotą failą, skirtą naudoti su žiniatinklio dokumentu. Pažymėtina, kad atkurti šrifto duomenys visais aspektais tiksliai atitinka įvesties šrifto formatą.

WOFF failo paslaugų programose dažnai yra papildomų funkcijų, tokių kaip glifo pogrupis, patvirtinimas arba šrifto funkcijų papildymai, tačiau tai nėra būtina. Tiek kūrėjas, tiek naudojimo agentai turi užtikrinti, kad būtų išsaugotas pagrindinių šrifto duomenų galiojimas.

### WOFF failo struktūra

WOFF failo struktūra yra panaši į sfnt šriftų struktūrą. Jis pagrįstas lentelių katalogu, kuriame yra kiekvieno šrifto duomenų lentelių ilgiai ir poslinkiai. Po šios pradinės informacijos pateikiamos visos lentelės. Faile yra šriftų duomenų bazė, kuri yra tokia pati kaip ir originaliuose šriftuose. Lentelių tvarka taip pat yra ta pati, tačiau kiekviena gali būti suspausta. Vis dėlto WOFF lentelės katalogas pakeičia pradinį lentelės katalogą.

WOFF failą sudaro:

 * WOFFHeader – failo antraštė su pagrindiniu šrifto tipu ir versija, kartu su metaduomenų ir privačių duomenų blokų poslinkiais.
 * TableDirectory – šriftų lentelių katalogas, nurodantis originalų dydį, suspaustą dydį ir kiekvienos lentelės vietą WOFF faile.
 * FontTables – šriftų duomenų lentelės iš įvesties sfnt šrifto, suglaudintos siekiant sumažinti pralaidumo reikalavimus.
 * ExtendedMetadata – pasirenkamas išplėstinių metaduomenų blokas, pateikiamas XML formatu ir suglaudintas saugojimui WOFF faile.
 * PrivateData – pasirenkamas privačių duomenų blokas, kurį gali naudoti šriftų kūrėjas, liejykla ar pardavėjas.

### WOFF antraštė
WOFF antraštę sudaro identifikuojantis parašas, nurodantis į failą įtrauktų duomenų rūšį. WOFF antraštė kartu su jos laukais yra tokia.

|Tipas|Lauko pavadinimas|Aprašymas|
---|---|---|
|UInt32|parašas |0x774F4646 'wOFF' |
|UInt32| flavor |Įvesties šrifto sfnt versija.|
|UInt32| ilgis |Bendras WOFF failo dydis.|
|UInt16| numTables |Įrašų skaičius šriftų lentelių kataloge.|
|UInt16| rezervuotas |Rezervuotas; nustatyti į nulį.|
|UInt32| totalSfntSize |Bendras dydis, reikalingas nesuspaustiems šrifto duomenims, įskaitant sfnt antraštę, katalogą ir šriftų lenteles (įskaitant užpildymą).|
|UInt16| majorVersion |Pagrindinė WOFF failo versija.|
|UInt16| minorVersion |Nedidelė WOFF failo versija.|
|UInt32| metaOffset |Poslinkis į metaduomenų bloką, nuo WOFF failo pradžios.|
|UInt32| metaLength |Suspausto metaduomenų bloko ilgis.|
|UInt32| metaOrigLength |Nesuspaustas metaduomenų bloko dydis.|
|UInt32| privOffset |Poslinkis į privačių duomenų bloką, nuo WOFF failo pradžios.|
|UInt32| privLength |Privačių duomenų bloko ilgis.|

## Nuorodos

 * [w3 WOFF failo formatas](https://www.w3.org/TR/WOFF/)

