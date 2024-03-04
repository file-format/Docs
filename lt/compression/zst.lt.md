{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ZST failas – Zstandartinis suspausto failo formatas",
  "description":"Sužinokite apie ZST failo formatą ir API, kurios gali kurti ir atidaryti ZST failus.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst-lt",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## Kas yra ZST failas?

ZST failas yra suspaustas failas, generuojamas naudojant Zstandard (zstd) glaudinimo algoritmą. Tai suspaustas failas, sukurtas naudojant algoritmą be nuostolių suglaudinant. ZST failai gali būti naudojami įvairių tipų failams, pvz., duomenų bazėms, failų sistemoms, tinklams ir žaidimams, suspausti. Zstandardą valdo [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878), kuris aprašo bendrą glaudinimo mechanizmą, medijos tipą ir turinio kodavimą.

## ZST failo formatas

ZST failai diske saugomi suspausto failo formatu. Suspaudimo mechanizmas aprašytas RFC 8878, kuris paseno RFC 8478.

## ZST rėmeliai

ZST failą sudaro vienas ar daugiau kadrų. Kiekvienas rėmelis gali būti Zstandartinis rėmelis arba praleidžiamas rėmelis. Zstandartiniame kadre yra suspausti duomenys, o praleidžiamame kadre yra pasirinktiniai vartotojo metaduomenys.

### Zstandartinis rėmelis

Zstandard rėmo struktūra yra tokia.

|Laukas|Dydis baitais|
---|---|
|Magic_Skaičius |4 baitai|
|Frame_Header |2-14 baitų|
|Data_Block |n baitų|
|[Daugiau duomenų_blokų] ||
|[Content_Checksum] |4 baitai|

### Praleidžiamas kadras

Praleidžiamasis kadras leidžia įterpti vartotojo apibrėžtus metaduomenis į sujungtų kadrų srautą. Praleidžiamo rėmelio struktūra yra tokia.

|Magic_Skaičius |Rėmo_dydis |Vartotojo_duomenys|
---|---|---|
|4 baitai |4 baitai |n baitai|

## Nuorodos Nr.

* [RFC 8878 Zstandard Compression](https://www.rfc-editor.org/rfc/rfc8878)


