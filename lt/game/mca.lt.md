{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie MCA failo formatą ir API, kurios gali kurti ir atidaryti MCA failus.",
  "title": "MCA – „Minecraft Anvil Region“ failo formatas",
  "linktitle": "MCA",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-lta"
}
},
  "lastmod": "2022-12-13"
}

## Kas yra MCA failas?

Minecraft Anvil regiono failo formatas yra duomenų saugojimo formatas, naudojamas populiariame vaizdo žaidime **Minecraft** saugoti Minecraft pasaulio reljefo dalis. Minecraft pasaulį sudaro regionai, kuriuose kiekvienas regionas yra padalintas į dalis. MCA failo formatas leidžia efektyviai saugoti didelius žaidimo duomenų kiekius, pvz., blokų ir objektų vietą tam tikroje žaidimų pasaulio dalyje. MCA failus reikia derinti su kitais MCA failais, kad būtų sukurtas visas pasaulis.

Be žaidimo duomenų saugojimo, Anvil regiono failo formatas taip pat apima įvairių kitų duomenų tipų, tokių kaip žaidėjo duomenys ir metaduomenys, palaikymą. Tai leidžia efektyviai saugoti visą informaciją, kurios reikia norint visiškai atkurti tam tikrą žaidimų pasaulio dalį, įskaitant blokų, objektų ir kitų žaidimo objektų vietą.

## MCA failo formatas – daugiau informacijos

Anvil regiono failo formatas yra NBT (Named Binary Tag) formato variantas, kuris yra hierarchinė medį primenanti struktūra, skirta duomenų saugojimui dvejetainiame faile. Tai leidžia efektyviai saugoti sudėtingas duomenų struktūras kompaktišku ir lengvai skaitomu formatu.

### MCA failo gabalai

Minecraft gabalas yra 16 x 16 x 16 blokų žaidimų pasaulio sritis, kuri įkeliama į atmintį ir pateikiama žaidėjo ekrane. Anvil regiono failo formatas išsaugo visus tam tikros dalies duomenis viename faile, kurį prireikus galima greitai įkelti į atmintį. Tai leidžia efektyviai saugoti ir greitai pasiekti žaidimo duomenis, o tai svarbu norint užtikrinti sklandų ir sklandų žaidimų patirtį.

### Mažas MCA failo dydis

Viena iš pagrindinių Anvil regiono failo formato ypatybių yra glaudinimo naudojimas. Tai leidžia efektyviai saugoti didelius duomenų kiekius, neprarandant duomenų kokybės ar greičio, kuriuo galima juos pasiekti. Tai atliekama naudojant įvairius metodus, tokius kaip gzip glaudinimas ir duomenų gabalų glaudinimas.

Dėl suspausto MCA failų formato tai yra svarbi žaidimo duomenų saugojimo ir valdymo sistemos dalis. Veiksmingas suspaudimo naudojimas ir įvairių duomenų tipų palaikymas leidžia efektyviai saugoti ir greitai pasiekti žaidimo duomenis, užtikrinant sklandų ir sklandų žaidėjų žaidimų patirtį.

## MCA failo formato struktūra

Vidinę MCA failų formato struktūrą sudaro:
 * Antraštė ir a
 * Naudinga apkrova

### MCA antraštė

MCA regiono failo antraštė prasideda 8KiB antrašte, padalyta į dvi 4KiB lenteles. Pirmoje lentelėje yra dalių poslinkiai pačiame regiono faile, o antroje lentelėje pateikiamos paskutinių šių dalių atnaujinimų laiko žymos.

### MCA naudingoji apkrova

MCA naudingoji apkrova susideda iš gabalų, kur kiekvienas gabalo duomenys prasideda (didžiojo galo) keturių baitų ilgio lauku. Šiame lauke nurodomas tikslus likusių duomenų gabalų ilgis baitais. Paskutinio gabalo duomenys paminkštinti, kad jų ilgis būtų 4096B kartotinis. Minecraft nepriima failų, kurių paskutinė dalis nėra užpildyta.

## Kaip atidaryti MCA failus

Galite atidaryti ir redaguoti MCA failus naudodami MCEdit programą, kuri yra nemokama atvirojo kodo rengyklė, skirta Minecraft. Galite [download MCEdit](https://www.mcedit.net/) iš oficialios svetainės ir naudoti ją norėdami atidaryti ir peržiūrėti savo Anvil regiono failo turinį.

Įdiegę MCEdit, galite atidaryti Anvil regiono failą atlikdami šiuos veiksmus:

 1. Paleiskite MCEdit ir spustelėkite mygtuką Atidaryti viršutiniame kairiajame lango kampe.

 1. Dialogo lange Atviras pasaulis eikite į savo Anvil regiono failo vietą ir pasirinkite jį.

 1. Spustelėkite mygtuką Atidaryti, kad atidarytumėte failą MCEdit.

 1. MCEdit įkels failą ir pagrindiniame lange parodys jo turinį. Tada galite naudoti MCEdit įrankius ir funkcijas norėdami peržiūrėti, redaguoti ir ištraukti duomenis iš Anvil regiono failo.

## Nuorodos

* [Pasaulinis „Minecraft“ redaktorius](https://www.mcedit.net/)

* [Apie „Minecraft“](https://www.minecraft.net/)

* [Regiono failo formatas](https://minecraft.fandom.com/wiki/Region_file_format)


