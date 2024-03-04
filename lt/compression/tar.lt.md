{
  "date": "2019-10-11",
  "keywords": [
"tar failą",
"tar failo formatas",
"kas yra tar failas",
"failą",
"deguto pavyzdys",
"tar failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TAR – Unix archyvo failo formatas",
  "description": "Sužinokite, kas yra TAR failas ir API, kurios gali kurti ir atidaryti TAR failus.",
  "linktitle": "TAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-ta-ltr"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra TAR failas?

Failai su plėtiniu .tar yra archyvai, sukurti naudojant Unix pagrįstą įrankį, skirtą rinkti vieną ar daugiau failų. Keli failai saugomi nesuglaudintu formatu, todėl į archyvą galima įtraukti failus ir aplankus. TAR įrankis Unix yra pagrįstas komandomis, tačiau tokiu būdu sukurtus failus palaiko dauguma failų archyvavimo sistemų beveik visose operacinėse sistemose. Pirmą kartą jį 1979 m. sukūrė AT&T Bell Laboratories, o vėliau buvo paskelbtos versijos.

## TAR failo formatas

TAR is an open file format with full specifications available for developer's reference. Its file structure was standardized in POSIX.1-1988 and later in POSIX.1-2001. Tar sukurti duomenų rinkiniai išsaugo informaciją apie failų sistemos parametrus, tokius kaip:

* Vardas

* Laiko žymos

* Nuosavybė

* Prieigos prie failų leidimai

* Katalogų organizavimas


TAR failas neturi stebuklingo numerio. Jame yra blokų serija, kur kiekvienas blokas yra BLOCKSIZE baitų.

Kiekvienas archyvuotas failas yra pavaizduotas antraštės bloku, apibūdinančiu failą, po kurio seka nulis ar daugiau blokų, kurie nurodo failo turinį. Archyvo failo pabaigoje yra du 512 baitų blokai, užpildyti dvejetainiais nuliais kaip failo pabaigos žymeklis. Pagrįsta sistema turėtų įrašyti tokį failo pabaigos žymeklį archyvo pabaigoje, bet neturi manyti, kad toks blokas egzistuoja skaitant archyvą. Ypač GNU tar visada pateikia įspėjimą, jei su juo nesusiduria.

Blokai gali būti užblokuoti atliekant fizines I/O operacijas. Kiekvienas n blokų įrašas (kur n yra nustatytas blokavimo koeficientas = 512 dydžio parinktis į tar) įrašomas naudojant vieną write() operaciją. Magnetinėse juostose tokio įrašo rezultatas yra vienas įrašas. Rašant archyvą, paskutinis blokų įrašas turi būti parašytas visu dydžiu, blokuose po nulinio bloko turi būti visi nuliai. Skaitant archyvą, protinga sistema turėtų tinkamai tvarkyti archyvą, kurio paskutinis įrašas yra trumpesnis už kitus arba kuriame yra šiukšlių įrašai po nulinio bloko.

### TAR failo antraštė

Kaip ir bet kurioje kitoje failo antraštėje, tar failo antraštės įraše yra failo metaduomenys ir jis parodytas šioje lentelėje.

|Lauko poslinkis|Lauko dydis (baitai)|Laukas
---|---|---|
|0|100|Failo pavadinimas
|100|8|Failo režimas
|108|8|Savininko skaitmeninis vartotojo ID
|116|8|Skaitmeninis grupės vartotojo ID
|124|12|Failo dydis baitais (aštuontainė bazė)
|136|12|Paskutinio pakeitimo laikas skaitmeniniu Unix laiko formatu (aštuontainis)
|148|8|Antraštės įrašo kontrolinė suma
|156|1|Nuorodos indikatorius (failo tipas)
|157|100|Susieto failo pavadinimas

Nenaudojami laukai užpildomi NUL baitais. Antraštę sudaro 257 baitai, kurie yra užpildyti NUL baitais, kad būtų užpildyta iki 512 baitų.

## Kaip sukurti TAR failą

### Sukurkite TAR failą sistemoje Windows

Sistemoje Windows galite naudoti Windows posistemį, skirtą Linux (WSL) arba trečiųjų šalių įrankius, pvz., 7-Zip, kad sukurtumėte TAR failus. Štai kaip tai padaryti naudojant WSL:

 1. Įdiekite WSL, jei dar to nepadarėte. Jį galite įdiegti naudodami Windows funkcijų nustatymus.

 1. Atidarykite WSL terminalą ir naudokite tą pačią tar komandą kaip Linux arba Unix sistemose, kad sukurtumėte TAR failą.

### Sukurkite TAF failą Linux iš komandinės eilutės

Norėdami sukurti TAR failą naudodami komandų eilutę Linux arba Unix sistemose, atidarykite terminalą ir naudokite tar komandą. Galite sukurti TAR failą įvairiais glaudinimo formatais (pvz., .tar.gz, .tar.bz2, .tar.xz), bet čia mes sukursime paprastą .tar failą:

Norėdami sukurti TAR failą iš vieno failo arba katalogo, naudokite šią komandą:

```
tar -cvf archive.tar file_or_directory
```

## Kaip atidaryti TAR failą

### Atidarykite TAR failą sistemoje Windows

Windows operacinėje sistemoje turite įdiegti išskleidimo priemonę, pvz., 7-Zip. Tai nemokama archyvavimo programa, kurią galima naudoti norint sukurti ir išgauti įvairius suspaustų failų formatus. Dešiniuoju pelės mygtuku spustelėkite savo TAR failą ir pasirinkite parinktį **Ištraukti**.

### Atidarykite TAR failą Mac.

Mac kompiuteryje tiesiog dukart spustelėkite TAR, TGZ arba TAR.GZ failą, kad jį išpakuotumėte.

### Atidarykite TAR failą sistemoje Linux.

Jei naudojate Linux arba Mac terminalo programą, naudokite tar -xvf TAR failams arba tar -xvzf failams, kurie baigiasi TGZ arba TAR.GZ.

## Nuorodos Nr.

* [TAR – Vikipedija](https://en.wikipedia.org/wiki/Tar_(computing))

* [TAR pagrindinis formatas](https://www.gnu.org/software/tar/manual/html_node/Standard.html)


