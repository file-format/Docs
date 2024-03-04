{
  "date": "2021-04-08",
  "keywords": [
"lz4 failą",
"lz4 failo formatas",
"kas yra lz4 failas",
"failą",
"lz4 pavyzdys",
"lz4 failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LZ4 – LZ4 suspausto failo formatas",
  "description": "Sužinokite apie LBR failo formatą ir API, kurios gali kurti ir atidaryti LZ4 failus.",
  "linktitle": "LZ4",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lz-lt4"
}
},
  "lastmod": "2021-04-19"
}

## Kas yra LZ4 failas?

Failas su plėtiniu .lz4 yra suglaudintas archyvo failas, sukurtas naudojant programas/paslaugas, kurios palaiko [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)) glaudinimą. LZ4 algoritmas sutelkia dėmesį į greičio ir suspaudimo laipsnio kompromisą. Suspaustus LZ4 archyvus galima sukurti naudojant LZ4 komandų eilutės įrankį ir išskleisti naudojant tą patį.

## LZ4 failo formatas

LZ4 failo formatas, pagrįstas LZ4 glaudinimo algoritmu, nepriklauso nuo procesoriaus tipo, operacinės sistemos, failų sistemos ir simbolių rinkinio. Jis tinka failų glaudinimui ir srautinio perdavimo glaudinimui naudojant LZ4 algoritmą. Pradinį LZ4 formato diegimą [C](/programming/c/) kalba atliko Yann Collet 2011 m., o kūrėjas gali susipažinti su juo [Github](https://github.com/lz4/lz4).

### LZ4 rėmelio formatas

Bendra LZ4 failo formato struktūra yra tokia, kaip parodyta toliau.

|MagicNb|F. Deskriptorius| Blokas|(...)|Pabaigos žymėjimas |C. Kontrolinė suma|
---|---|---|---|---|---|
|4 baitai| 3-15 baitų ||| 4 baitai| 0-4 baitai|

#### Magiškas skaičius

4 baitai, Little endian formatas. Vertė: 0x184D2204

#### Rėmelio aprašas

Kadro aprašas susideda iš 3 t0 15 baitų ir yra svarbiausia specifikacijų dalis. Kartu laukai Magic_Number ir Frame_Descriptor vadinami LZ4 rėmelio antrašte, o jo dydis svyruoja nuo 7 iki 19 baitų. Tai yra taip, kaip parodyta žemiau.

|FLG| BD| (Turinio dydis)| (Žodyno ID)| HC|
---|---|---|---|---|
|1 baitas| 1 baitas| 0–8 baitai| 0–4 baitai| 1 baitas|

#### Duomenų blokai

Kiekvienas duomenų blokas seka tokia tvarka.

|Bloko dydis| duomenys| (Blokuoti kontrolinę sumą)|
---|---|---|
|4 baitai| |0–4 baitai|

#### Pabaiga

Blokų srautas baigiasi, kai po paskutinio duomenų bloko yra 32 bitų reikšmė 0x00000000.

#### Turinio kontrolinė suma

Content_Checksum patikrina teisingai iššifruoto turinio pagrįstumą ir atliekama naudojant xxHash-32 algoritmo rezultatą. Jis patvirtina sėkmingo visų blokų perdavimo rezultatus teisinga tvarka ir be klaidų.

## Nuorodos

* [LZ4 rėmelio formatas](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)

* [LZ4 glaudinimo algoritmas – Vikipedija](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))


