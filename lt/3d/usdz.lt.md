{
  "date": "2021-02-01",
  "keywords": [
"usdz",
"usdz failą",
"usdz failo formatas",
"Dokumento formatas",
"3d",
"usdz failo atsisiuntimas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "USDZ – universalus scenos aprašymo ZIP formatas",
  "description": "Sužinokite apie USDZ failo formatą ir API, kurios gali atidaryti ir kurti USDZ failus.",
  "linktitle": "USDZ",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-usd-ltz"
}
},
  "lastmod": "2021-02-01"
}

## Kas yra USDZ failas?

Failas su .usdz yra nesuspaustas ir nešifruotas ZIP archyvas, skirtas [USD](/3d/usd/) (Universal Scene Description) failo formatui, kuriame yra kitų formatų failų (pvz., tekstūrų ir animacijų), įterptų į archyvą ir juos paleidžiančių serverių. tiesiogiai su USD vykdymo laiku, nereikia išpakuoti. USDZ failai yra paketai, kurių dizainas pagrįstas nauja paketo Ar lygio abstrakcija. Usdz buvo užregistruotas IANA ir turi modelio laikmenos tipo pavadinimą ir potipio pavadinimą vnd.usd+zip, o išsamią informaciją galite rasti [IANA registration page](https://www.iana.org/assignments/media-types/model/vnd.usdz+zip).

## USDZ failo formatas

USDZ files are based on the ZIP file format that archive individual files in its container. This enables the receiver end to just unzip the contents and use the normal USD scene description files to work with and inspect. Almost all operating systems provide builtin support for the ZIP file formats and choosing this archiving format over any custom method makes it easy for USDZ files to be useful as a simple transport protocol.

### ZIP apribojimai

USDZ failo formatas naudoja ZIP failo formatą be jokio glaudinimo ir šifravimo. Tai buvo sukurta siekiant atitikti du reikalavimus:

 * Jei paketas jau įkeltas į atmintį arba kaip vienas failas diske, API galima USD USD, kad būtų galima pasiekti vaizde esančius duomenis.
 * Nereikėtų išskleisti failų į diską arba skirti daugiau saugyklos

Naudojant USDZ abu šie reikalavimai yra įvykdyti, nes dauguma pačių vaizdo formatų leidžia naudoti vidinio glaudinimo schemas, todėl failo dydis yra kompaktiškas.

### Išdėstymo reikalavimai

USDZ paketai reikalauja, kad failų išdėstymas pakete būtų toks, kad kiekvieno failo duomenys turėtų prasidėti 64 baitų kartotiniais nuo paketo pradžios. Tačiau paketas turėtų prasidėti vietiniu [USD](/3d/usd/) failu, jei paketą nukreipiate naudojant paprastą nuorodą. Tokiu atveju šis pirmasis USD failas vadinamas numatytuoju sluoksniu. Klientai, norintys pateikti srautinį turinį, taip pat gali norėti atsižvelgti į kitus išdėstymo apribojimus.

## USDZ failo atsisiuntimas
Kadangi usdz failai yra supakuoti su kitais aukštos kokybės vaizdais ir usd failais, jie gali užimti didesnę disko saugyklą. Čia galite rasti paprastą ir mažesnį USDZ pavyzdinį failą, kurį galite atsisiųsti:

- [Sample.usdz](../sample.usdz)

## Nuorodos

* [USDZ failo formato specifikacijos](https://openusd.org/release/spec_usdz.html)


