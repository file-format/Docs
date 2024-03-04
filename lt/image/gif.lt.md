{
  "date": "2019-10-11",
  "keywords": [
"gif failą",
"gif failo formatas",
"kas yra gif failas",
"failą",
"gif pavyzdys",
"gif failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GIF – vaizdo failo formatas",
  "description": "Sužinokite apie GIF failo formatą ir API, kurios gali kurti ir atidaryti GIF failus.",
  "linktitle": "GIF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-gi-ltf"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra GIF failas? ##

GIF arba grafinis mainų formatas yra labai suspausto vaizdo tipas. Unisys priklausantis GIF naudoja LZW glaudinimo algoritmą, kuris nepablogina vaizdo kokybės. Kiekvienam vaizdui GIF paprastai leidžia iki 8 bitų viename pikselyje ir iki 256 spalvų visame vaizde. Priešingai nei [JPEG](/image/jpeg/) vaizdas, kuris gali rodyti iki 16 milijonų spalvų ir gana paliečia žmogaus akies ribas. Kai atsirado internetas, GIF išliko geriausiu pasirinkimu, nes jiems reikėjo mažo pralaidumo ir jie buvo suderinami su grafika, kuri naudoja vientisas spalvų sritis. Animacinis GIF sujungia daugybę vaizdų ar kadrų į vieną failą ir pateikia juos seka, kad būtų sukurtas animacinis klipas arba trumpas vaizdo įrašas. Spalvų apribojimai yra iki 256 kiekvienam kadrui ir greičiausiai bus mažiausiai tinkami kitiems vaizdams ir nuotraukoms su spalvų gradientu atkurti.

## GIF failo formatas ##

Konceptualiai GIF failai turi fiksuoto dydžio grafinę sritį, užpildytą nuliu ar daugiau vaizdų. Kai kurie GIF failai padalija fiksuoto dydžio grafinę sritį arba blokus į antrinius vaizdus, kurie gali veikti kaip animuoti kadrai, jei yra animuotas GIF. GIF formatas naudoja 1–8 bitų pikselių gylį bitmap duomenims saugoti. Vaizdams saugoti visada naudojami RGB spalvų modelio ir paletės duomenys. Priklausomai nuo versijos, fiksuoto ilgio antraštė (GIF87a arba GIF89a) apibrėžia tipinio GIF failo pradžią.

Šiuo metu yra dvi GIF versijos: 87a ir 89a. Pirmasis yra originalus GIF formatas, o antrasis yra naujas GIF formatas. Šiame failo formate blokų charakteristikos ir pikselių matmenys minimi fiksuoto ilgio loginiame ekrano apraše. Visuotinės spalvų lentelės egzistavimą ir dydį gali nurodyti ekrano aprašas, kuris seka tolesnę informaciją, jei yra. Anonsas yra paskutinis failo baitas, kuriame yra vienas ASCII kabliataškio baitas. Įprastas GIF87a failo išdėstymas yra toks:

### Antraštė ###

Antraštėje yra šeši baitai ir ji naudojama nurodyti failo tipą kaip GIF. Nors loginio ekrano aprašas yra atskirtas nuo tikrosios antraštės, kartais jis laikomas antrąja antrašte. Ta pati struktūra, kuri naudojama antraštei saugoti, gali saugoti loginį ekrano aprašą. Visi GIF failai prasideda 3 baitų parašu ir kaip identifikatorius naudoja simbolius GIF. Versija taip pat yra trijų baitų dydžio ir deklaruoja GIF failo versiją.

### Loginis ekrano aprašas ###

Fiksuoto ilgio vaizdo aprašas nurodo ekrano ir spalvų informaciją, reikalingą GIF vaizdui sukurti. Laukuose Aukštis ir Plotis pateikiama mažiausia ekrano skiriamosios gebos reikšmė, kuri yra privaloma vaizdo duomenims rodyti. Jei rodymo įrenginys negali rodyti nurodytos skiriamosios gebos, norint tinkamai parodyti vaizdą, reikės pakeisti mastelį. Ekrano ir spalvų žemėlapio informacija rodoma keturiuose toliau pateiktos lentelės polaukiuose (tuo tarpu 0 bitas yra mažiausiai reikšmingas bitas):


|Bitai|Polaukiai
---|---|
|0-2|Visuotinės spalvų lentelės dydis
|3|Spalvų lentelės rūšiavimo vėliavėlė
|4-6|Spalvų skyra
|7|Visuotinės spalvų lentelės vėliava

#### Visuotinė spalvų lentelė ####

Neprivaloma visuotinė spalvų lentelė dedama iškart po loginio ekrano aprašo. Ši lentelė susieta taip, kad indeksuotų vaizdo duomenų pikselių spalvų duomenis. Jei nėra visuotinės spalvų lentelės, kiekvienas GIF failo vaizdas naudoja savo vietinę spalvą. Geriau pateikti numatytąją spalvų lentelę, jei nėra visuotinės ir vietinės spalvų lentelės. Trijų baitų trigubų serija sudaro spalvų lentelės elementus. Kiekvienas baitas apibūdina RGB spalvos reikšmę. Raudona, žalia ir mėlyna spalvos naudojamos kaip kiekvieno spalvų lentelės elemento reikšmės. Įrašai visuotinėje spalvų lentelėje pasiekia daugiausiai 256 įrašus ir visada reiškia dviejų laipsnį.

#### Vaizdo duomenys ####

Vaizdo duomenyse saugomas baitas nekoduotų simbolių, po kurių seka susietas sub-sąrašas kartu su LZW koduotais duomenimis.

#### Anonsas ####

Anonsas reiškia vieną duomenų baitą, kuris yra paskutinis failo simbolis. Šio baito vertė nuolat yra 3 Bh ir nurodo duomenų srauto pabaigą. Kiekvieno GIF failo paskutiniame faile turi būti anonsas.

## Nuorodos Nr.

* [GIF failo formatas](https://en.wikipedia.org/wiki/GIF)


