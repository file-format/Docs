{
  "date": "2023-06-08",
  "keywords": [
"crx failą",
"kas yra crx failas",
"Kaip įdiegti crx failą google chrome",
"kaip atidaryti crx failą",
"kas yra crx faile",
"koks yra crx failo formatas",
"failą",
"crx failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CRX failo formatas – „Google Chrome“ plėtinys",
  "description": "Sužinokite apie CRX formatą ir API, kurios gali kurti ir atidaryti CRX failus.",
  "linktitle": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx-lt",
      "parent": "misc"
}
},
  "lastmod": "2023-06-08"
}

## Kas yra CRX failas?

CRX failo formatas susietas su Google Chrome naršyklės plėtiniais. CRX failas iš esmės yra suspaustas paketas, kuriame yra būtinų failų ir metaduomenų, kad plėtinys būtų įdiegtas ir paleistas Google Chrome. Tai pagerina žiniatinklio naršyklės funkcionalumą arba išvaizdą, nes suteikia papildomą funkciją arba temą.

Kai CRX failas atsisiunčiamas ir įdiegiamas Google Chrome, naršyklė patikrina plėtinio vientisumą naudodama viešąjį raktą ir parašą. Jei patvirtinimas sėkmingas, Chrome ištraukia CRX failo turinį ir įdiegia plėtinį, kad jį būtų galima naudoti. Naudotojai gali tvarkyti savo plėtinius naudodami Chrome plėtinių puslapį, kuriame galima įgalinti, išjungti arba pašalinti įdiegtus plėtinius.

## Kaip įdiegti CRX failą „Google Chrome“?

Norėdami įdiegti CRX failą Google Chrome, galite atlikti šiuos veiksmus:

1. Atidarykite Chrome naršyklę.
2. Adreso juostoje įveskite chrome://extensions ir paspauskite Enter.
3. Įgalinti Kūrėjo režimo perjungimo jungiklį, esantį viršutiniame dešiniajame plėtinių puslapio kampe.
4. Spustelėkite mygtuką Įkelti išpakuotą.
5. Raskite ir pasirinkite aplanką, kuriame yra ištrauktas CRX failo turinys (arba tiesiog pasirinkite patį CRX failą).
6. Spustelėkite Atidaryti, kad įdiegtumėte plėtinį.

## Kas yra CRX faile?

CRX faile yra būtinų failų ir metaduomenų, reikalingų Google Chrome plėtiniui. Čia pateikiamas tipinio CRX failo turinio suskirstymas:

- **Manifest file (manifest.json):** This file is a JSON-formatted file that includes information about extension such as its name, version, description, permissions and background scripts. It defines the structure and behavior of extension.
– **JavaScript failai:** šiuose failuose yra kodas, apibrėžiantis plėtinio funkcionalumą. Juose gali būti scenarijų, skirtų įvykiams tvarkyti, tinklalapiams keisti arba sąveikauti su Chrome API.
– **HTML, CSS ir vaizdo failai:** plėtiniuose dažnai yra vartotojo sąsajos elementų, pvz., iššokančių langų arba parinkčių puslapių. HTML failai apibrėžia šių sąsajų struktūrą, o CSS failai kontroliuoja jų išvaizdą. Vaizdo failai naudojami piktogramoms ar kitiems grafiniams ištekliams.
– **Pasirenkami išteklių failai:** plėtiniuose gali būti papildomų išteklių, pvz., lokalizacijos failų, skirtų kelioms kalboms palaikyti. Šiuose failuose yra teksto, naudojamo plėtinio vartotojo sąsajoje, vertimai.
– **Foniniai scenarijai:** jei plėtinyje yra foninių procesų arba scenarijų, kurie veikia nepriklausomai nuo aktyvaus tinklalapio, šie scenarijai bus įtraukti į CRX failą.
– **Turinio scenarijai:** turinio scenarijai yra scenarijai, kuriuos galima įterpti į tinklalapius, siekiant pakeisti jų elgesį arba sąveikauti su jų turiniu. Jei plėtinys naudoja turinio scenarijus, būtini failai tiems scenarijams bus pateikti CRX faile.
– **Kiti ištekliai:** atsižvelgiant į konkrečius plėtinio reikalavimus, gali būti įtraukti papildomi failai, pvz., garso ar vaizdo failai, šriftai arba duomenų failai.

CRX failo formatas iš esmės yra suspaustas paketas, kuriame struktūrizuotai yra visi šie failai ir aplankai. Kai CRX failas yra įdiegtas Google Chrome, naršyklė ištraukia turinį ir įdeda jį į atitinkamas vietas, kad būtų galima įkelti plėtinį ir paleisti jį naršyklėje.

## Koks yra CRX failo formatas?

CRX failo formatas yra specifinis Google Chrome plėtinių pakavimo ir platinimo formatas. Iš esmės tai yra suspaustas ZIP archyvas su skirtingu failo plėtiniu. Pagrindinė CRX failo struktūra yra tokia:

– **Failo parašas:** pirmuose 4 failo baituose yra magiškas skaičius Cr24 (šešioliktainis skaičius: 43 72 32 34), kuris naudojamas kaip parašas, identifikuojantis failą kaip CRX failą.
– **Versijos numeris:** Kiti 4 baitai nurodo CRX formato versijos numerį.
– **Viešojo rakto ilgis:** šie 4 baitai nurodo užkoduoto viešojo rakto, naudojamo plėtinio parašo patvirtinimui, ilgį.
- **Parašo ilgis:** paskesni 4 baitai nurodo plėtinio parašo ilgį.
– **Viešasis raktas:** šioje skiltyje yra užkoduotas viešasis raktas, naudojamas plėtinio vientisumui patikrinti.
- **Parašas:** šioje skiltyje yra plėtinio parašas, kuris sugeneruojamas pasirašant plėtinio turinį naudojant privatų raktą, atitinkantį aukščiau paminėtą viešąjį raktą.
– **ZIP archyvas:** likę CRX failo baitai sudaro suglaudintą ZIP archyvą. Šiame archyve yra visi reikalingi failai ir plėtinių aplankai, įskaitant manifesto failą, JavaScript failus, HTML failus, CSS failus, vaizdus ir visus kitus išteklius.

## Nuorodos
* [CRX formato specifikacija](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)


