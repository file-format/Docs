{
   "date":"2023-07-20",
   "keywords":[
"BIN",
"BIN failas",
"failą",
"BIN failo plėtinys",
"pratęsimas",
"failą"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"BIN failo formatas – „Unix“ vykdomasis failas",
   "description":"Sužinokite apie BIN formatą ir API, kurios gali kurti ir atidaryti BIN failus.",
   "linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin-lt",
         "parent":"executable"
}
},
   "lastmod":"2023-07-20"
}

## Kas yra BIN failas?

BIN failas yra vykdomasis failas Unix pagrindu veikiančiose operacinėse sistemose, tokiose kaip Linux arba FreeBSD. Jame yra sudaryta programa, sudaryta iš dvejetainio kodo, gauto iš šaltinio kodo, todėl ji yra suderinama su pagrindine sistemos architektūra. Unix Executable BIN failai gali būti lyginami su Windows .EXE failais ir macOS .APP failais pagal vykdomųjų formatų vaidmenį.

Programinės įrangos kūrimo Unix sistemoms srityje kūrėjai dažniausiai naudoja BIN failus programoms pakuoti ir platinti. Jie siūlo patogią programinės įrangos pateikimo vartotojams priemonę, leidžiančią lengvai įdiegti ir vykdyti. Be BIN failų, yra ir kitų tipų Unix vykdomųjų failų, įskaitant [.ELF](/executable/elf/), .X86, [.RUN](/executable/run/) ir .X86_64, kurių kiekvienas yra pritaikytas pagal konkrečius aparatūros arba sistemos reikalavimus.

Kalbant apie vidinę BIN failo struktūrą, ją sudaro užkoduoti duomenys, kuriuos Unix operacinė sistema naudoja, kad identifikuotų, nuskaitytų ir vykdytų pridedamą programą. Sistema remiasi konkrečiais failų parašais arba antraštėmis, kad atpažintų BIN failą kaip vykdomąjį failą, o po to interpretuoja ir vykdo dvejetaines komandas.

BIN failai dažnai pateikiami kartu su pridedamu **INSTALL.TXT** failu, kuriame pateikiamos išsamios instrukcijos, kaip tinkamai įdiegti ir nustatyti programą. Ši dokumentacija užtikrina, kad vartotojai galėtų sėkmingai naršyti diegimo procesą ir pradėti naudoti programinę įrangą be komplikacijų.

## Kaip atidaryti BIN failą?

BIN failai nėra skirti tiesiogiai atidaryti ir peržiūrėti. Tačiau galite vykdyti programas arba išgauti jose esančius duomenis. Norėdami pasiekti BIN failo turinį, atlikite šiuos veiksmus komandinėje eilutėje, darydami prielaidą, kad BIN failo pavadinimas yra sample.bin:

1. **Užtikrinkite vykdomuosius leidimus:**

Prieš vykdydami BIN failą, įsitikinkite, kad jis turi reikiamus leidimus, kad būtų paleistas kaip vykdomasis failas. Naudokite komandą:

```
$ chmod +x sample.bin
```

Ši komanda suteikia failo vykdymo teises.

2. ** Vykdykite BIN failą:**

Nustatę vykdomuosius leidimus, galite paleisti BIN failą įvesdami šią komandą:

```
$ ./sample.bin
```

**Įspėjimas**

_Būkite atsargūs dirbdami su atsisiųstais arba el. paštu siunčiamais BIN failais, nes kibernetiniai nusikaltėliai juos gali panaudoti kenkėjiškų programų platinimui. Paleiskite BIN failus tik iš patikimų šaltinių, kad sumažintumėte kenkėjiškų vykdomųjų atakų riziką._

## Kiti BIN failai

Štai kiti failų tipai, kuriuose naudojamas **.bin** failo plėtinys.

- [BIN - MacBinary Encoded File](/compression/bin/)
- [BIN - Binary Disc Image File](/disc-and-media/bin/)
- [BIN - BlackBerry IT Policy File](/settings/bin/)
- [BIN - Sega Genesis Game ROM](/game/bin/)
- [BIN - PSX PlayStation BIOS Image](/game/bin-pcsx/)

## Nuorodos

* [Kaip vykdyti dvejetainius failus sistemoje Linux](https://linuxhint.com/execute-binary-files-in-linux/)



