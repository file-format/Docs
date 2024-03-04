{
  "date": "2021-08-31",
  "keywords": [
"xbe failą",
"xbe failo formatas",
"kas yra xbe failas",
"failą",
"xbe pavyzdys",
"xbe failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie XBE failo formatą ir API, kurios gali kurti ir atidaryti XBE failus.",
  "title": "XBE – „iOS“ programų paketo failas",
  "linktitle": "XBE",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-xb-lte"
}
},
  "lastmod": "2021-08-31"
}

## Kas yra XBE failas?
Failas, kurio plėtinys yra .xbe, yra vykdomoji programa iš Xbox vaizdo žaidimų disko. XBE failai yra pagrindiniai failai, vykdomi Xbox sistemoje ir paprastai neturėtų būti atidaromi kompiuteryje, tačiau juos galima atidaryti asmeniniame kompiuteryje naudojant Xbox emuliacijos programą. Šiuos failus paprastai sukuria žaidimų kūrėjai, o tada pasirašo Microsoft. Failo struktūra panaši į Windows PE failus, tačiau taikomi keli svarbūs pakeitimai pagal XBox nustatymus, kad jį būtų galima paleisti XBox.

## XBE failo formatas
XBE failą sudaro vaizdo antraštė, sekcijų antraščių rinkinys, sertifikatas, gijos vietinės saugojimo duomenys, bibliotekos versijų rinkinys, Microsoft bitmap ir skyriai, kuriuose yra kodas ir ištekliai.

### Vaizdo antraštė
Vaizdo antraštė apima informaciją, paaiškinančią, kur faile yra kiti vykdomojo failo komponentai ir kaip turi būti apdorojama ir įkeliama vykdomoji programa.

### TLS lentelė
TLS lentelę sudaro visa informacija, reikalinga XBE norint tinkamai nustatyti gijų vietinę saugyklą. Jis iš esmės yra unikalus TLS katalogui, esančiam PE32 failuose, ir gali būti tiesiogiai nukopijuotas iš ten. Ši lentelė gali būti praleista, jei XBE faile nenaudojama jokia vietinė gijų saugykla, o atitinkamas laukas vaizdo antraštėje nustatomas į nulį.

| Offset | Dydis | Vardas | Aprašymas |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Neapdorotų duomenų pradžia | Absoliutus (ty ne RVA) TLS kintamojo duomenų pradžios adresas programos vaizde. |
| 0x0004 | 0x0004 | Neapdorotų duomenų pabaiga | Absoliutus (ty ne RVA) TLS kintamojo duomenų pabaigos adresas programos vaizde. |
| 0x0008 | 0x0004 | Indekso adresas | Absoliutus (ty ne RVA) TLS indekso kintamojo adresas. |
| 0x000C | 0x0004 | Atgalinių skambučių adresas | Absoliutus (ty ne RVA) TLS atgalinio skambinimo funkcijų lentelės adresas. |
| 0x0010 | 0x0004 | Nulinio užpildymo dydis | Baitų, einančių po neapdorotų duomenų, skaičius atmintyje turėtų būti nustatytas į nulį. |
| 0x0014 | 0x0004 | Charakteristikos | Apibūdina derinimą. |

### Sertifikatas

 A a certificate is mandatory for each Xbox executable that contains information about the titles:
 
- Sertifikato sukūrimo laikas ir data
- Pavadinimo ID
- Pavadinimo pavadinimas
– Alternatyvūs pavadinimo ID
- Leidžiami laikmenų tipai, iš kurių galima paleisti vykdomąjį failą (HD, DVD, CD ir kt.)
- Žaidimo regionas
- Žaidimų reitingai
- Disko numeris
- Versija
- LAN rakto neapdoroti duomenys, naudojami sistemos nuorodai
- Parašo rakto neapdoroti duomenys (naudojami įrašytiems žaidimams pasirašyti)
- Alternatyvūs parašo raktai
- Originalus sertifikato dydis
- Internetinės paslaugos pavadinimas (nėra ankstyvose vykdomosiose programose)
- Vykdymo laiko saugos vėliavėlės (nėra ankstyvose vykdomosiose programose)
 
### Leidžiami medijos tipai
Medijos tipai, kuriuos leidžia vykdyti vykdomasis failas. Yra žinomos šios vertės:
| laikmenos tipas | Vertė |
---------------------|------------|
| HARD_DISK | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
| CD | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| DONGLE | 0x00000100 |
| MEDIA_BOARD | 0x00000200 |
| NONSECURE_HARD_DISK | 0x40000000 |
| NONSECURE_MODE | 0x80000000 |
| MEDIA_MASK | 0x00FFFFFF |

### Skyriai
Skyriai išreiškiami skyrių antraštėmis. Skyrių antraštės prasideda iškart po sertifikato ir pateikia informaciją, kurioje failo dalyje yra tikrosios skiltys. Xbox vykdomajame faile visada yra bent du skyriai:
- .tekstas
- .rdata


## Nuorodos 

* [Xbe – XBox Executable](https://xboxdevwiki.net/Xbe)



