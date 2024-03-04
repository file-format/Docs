{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Sužinokite apie Age of Empires 2 Expansion Replay MGX failo formatą ir API, kurios gali kurti ir atidaryti MGX failus.",
  "title" : "MII failas – „Wii Virtual Avatar“ failo formatas",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii-lt",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## Kas yra MII failas?

MII failas yra virtualaus avataro failo formatas, naudojamas virtualiems avatarams saugoti Nintendo Wii žaidimų konsolėje. Šiuose failuose yra tokios informacijos kaip avataro išvaizda, judesiai ir animacija. Jie gali būti naudojami žaidimuose, socialinių tinklų programose ir kitoje Wii programinėje įrangoje. MII faile taip pat yra kitų pseudoportreto funkcijų, tokių kaip lytis, plaukų spalva, odos spalva, veido bruožai ir akių tipas.

MII failą galite atidaryti naudodami [My Avatar Editor](https://rc24.xyz/goodies/mii/).

## MII failo formatas

MII failo formatas yra išsamiai apibrėžtas [Wii Brew](https://wiibrew.org/wiki/Mii_data). Stygos MII faile saugomos Unicode formatu (UTF-16), big-endian.

### MI blokas

MII failo duomenys Wiimote saugomi dviem blokais. Kiekvienas blokas yra 750 baitų ilgio, su 2 baitais CRC, todėl iš viso yra 752 baitai. Kiekvienas blokas prasideda 4 baitų reikšme (RNCD), kuri, atrodo, yra magiškas MII failo formato skaičius.

## Kaip sukurti MII failus?

Yra keletas skirtingų būdų, kaip sukurti Nintendo Wii avatarus:

1. Naudojant Wii integruotą Mii kanalą: Šis kanalas leidžia kurti pasirinktinius avatarus naudojant įvairius įrankius, įskaitant veido bruožus, kūno formas ir drabužius. Sukūrę savo pseudoportretą, galite išsaugoti jį kaip Mii failą ir naudoti žaidimuose bei kitoje programinėje įrangoje Wii.

1. Mii Maker programos naudojimas Nintendo 3DS: Mii Maker programa leidžia kurti pasirinktinius avatarus naudojant Nintendo 3DS jutiklinį ekraną ir fotoaparatą. Sukūrę pseudoportretą, galite išsaugoti jį kaip Mii failą ir belaidžiu ryšiu perkelti į savo Wii.

1. Naudojant trečiosios šalies programinę įrangą: kai kurie kūrėjai sukūrė programinę įrangą, leidžiančią sukurti pasirinktinius Wii avatarus. Ši programinė įranga paprastai skirta naudoti kompiuteryje ir gali prireikti papildomų veiksmų norint perkelti pseudoportretą į jūsų Wii.

1. Iš anksto sukurtų pseudoportretų naudojimas: kai kuriuose Wii žaidimuose ir programinėje įrangoje gali būti iš anksto sukurti avatarai, kuriuos galite naudoti.

Visais atvejais turite turėti Nintendo paskyrą, kad galėtumėte sukurti ir išsaugoti savo avatarą Wii.

## Nuorodos

* [Mano avataro redaktorius](https://rc24.xyz/goodies/mii/)

* [Wii Brew](https://wiibrew.org/wiki/Mii_data)


