{
  "date" : "2023-01-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Sužinokite apie Unreal Static Meshes VPK failo formatą ir API, kurios gali kurti ir atidaryti VPK failus.",
  "title" : "VPK failas – nerealus statinių tinklelių failas",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "identifier":"game-vpk-lt",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-16"
}

## Kas yra VPK failas?

.vpk failas yra failo formatas, naudojamas **Source Engine**, Valve Corporation sukurtas žaidimų variklis. VPK failai naudojami žaidimų turiniui, pvz., modeliams, tekstūroms ir garsams, pakuoti, ir dažniausiai naudojami tokiuose žaidimuose kaip Team Fortress 2, Left 4 Dead ir Counter-Strike: Global Offensive. Failus galima atidaryti ir išskleisti naudojant įvairius įrankius, tokius kaip GCFScape ir VPK Tool.

## VPK failo formatas – daugiau informacijos

VPK failai saugomi diske kaip dvejetainiai failai. Vienas vpk failas gali būti VPK paketo dalis arba gali veikti kaip nepriklausomas neapdorotas VPK failas. Informacija, kurią galima saugoti VPK faile, apima žemėlapius, medžiagą, žaidimų turinį ir choreografines scenas.

### Kaip sukurti VPK failą?

Yra keletas būdų, kaip sukurti .vpk failą, atsižvelgiant į turimus įrankius.

1. Naudojant VPK įrankį: tai komandinės eilutės įrankis, kurį galima naudoti VPK failams kurti ir išskleisti. VPK failą galima sukurti naudojant šią komandą:
```
"vpk.exe -M <directory> <output_file.vpk>"
```
Tai sukurs VPK failą iš nurodyto katalogo ir išsaugos jį kaip nurodytą išvesties failą.

1. Hammer Editor naudojimas: Hammer Editor yra įrankis, įtrauktas į šaltinio SDK, kurį galima naudoti žaidimų, kuriuose naudojamas šaltinio variklis, lygiams kurti ir redaguoti. Taip pat yra galimybė kurti VPK failus, dešiniuoju pelės mygtuku spustelėjus aplanką skirtuke Failų sistema ir pasirinkus Sukurti VPK.

1. Naudojant Valve VPK kūrėją: tai Valve sukurtas įrankis, naudojamas žaidimų turiniui pakuoti ir platinti. Šis įrankis gali būti naudojamas kuriant VPK failus, taip pat tai yra oficialus įrankis VPK failams kurti.

## Nuorodos

 * [Valve Software](https://www.valvesoftware.com/en/)
 * [VPK kūrėjo ištekliai](https://developer.valvesoftware.com/wiki/GCF)

