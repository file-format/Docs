{
  "date": "2021-06-16",
  "keywords": [
"LZO",
"Suspaustas",
"Failas",
"Pratęsimas",
"Dokumento formatas",
"Lempel-Ziv-Oberhume"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "LZO failo formatas",
  "description": "Sužinokite apie LZO failo formatą ir API, kurios gali kurti ir atidaryti LZO failus.",
  "linktitle": "LZO",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lz-lto"
}
},
  "lastmod": "2021-06-16"
}

## Kas yra LZO failas? ##

Failas su plėtiniu .lzo yra derinamas su failų archyvavimo funkcijomis, kurios gali sumažinti visų suspausto failo failų dydį. Visi suspausti failai gali sudaryti vieną ar daugiau failų ar net segtuvų grupių su keliais skirtingų tipų ir matmenų failais. Suglaudinto failo dydis yra mažesnis, palyginti su visų failų ir aplankų, saugomų LZO suglaudintame faile, jungtimi. Visi LZO suspausti failai yra saugomi LZO formatu ir yra aiškiai vykdomi naudojant LZOP failų glaudinimo ir išskleidimo programinės įrangos suglaudinimo funkcijas. Visos glaudinimo specifikacijos yra sujungtos į šią failų glaudinimo ir išskleidimo programą, kuri yra sukurta iš Lempel-Ziv-Oberhume failų glaudinimo bibliotekos. Spartesnis dekompresijos greitis ir sukurti suspaudimo koeficientai taip pat yra sujungti į šiuos LZO failus.

## LZO specifikacijos Nr.

Markus Franz Xaver Johannes Oberhumer developed the original "lzop" algorithm, based on earlier algorithms by Abraham Lempel and Jacob Ziv, in 1996. Ši biblioteka įgyvendina įvairius algoritmus su šiomis savybėmis:

* Greitesnis suspaudimas nei DEFLATE

* Greita dekompresija

* Papildomi buferiai, kurių reikia glaudinant (8 KB arba 64 KB dydžio, priklausomai nuo glaudinimo lygio)

* Šaltinio ir paskirties buferiai yra visa atmintis, reikalinga dekompresijai

* Suteikia tiek suspaudimo laipsnio, tiek suspaudimo greičio valdymą


Kaip bloko glaudinimo algoritmas, LZO atlieka persidengiantį glaudinimą ir dekompresiją vietoje. Norint pasiekti persidengiantį suspaudimą, suspaudimo ir išskleidimo bloko dydis turi atitikti. LZO glaudinimo algoritmas padalija įvesties duomenis į atitikmenis (slenkantį žodyną) ir nesutampančius pažodinius žodžius, suteikdamas gerus rezultatus su labai pertekliniais duomenimis ir priimtinus rezultatus su nesuspaudžiamais, tik padidindamas nesuspaudžiamus duomenis 1/64 originalo. dydis.

## Problemos atidarant LZO failą ##

Toliau pateikiamos kelios problemos, dėl kurių gali prastai veikti LZO failo formatas:
  
* Failas gali būti sugadintas. Norėdami išspręsti šią problemą, atsisiųskite failą dar kartą arba paprašykite siuntėjo dar kartą išsiųsti failą
* Antroji priežastis yra užkrėstas failas, šiuo atveju tinkamai nuskaitykite failą
* Netinkamos nuorodos į LZO failą
  *	 Removal of the description of the LZO 
* Nepakanka aparatinės įrangos išteklių
* Pasenusios įrangos tvarkyklės
  
## Nuorodos Nr.

* [LZO – Vikipedija](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)


