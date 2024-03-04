{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie MCR failo formatą ir API, kurios gali kurti ir atidaryti MCR failus.",
  "title": "MCR – Minecraft regiono failo formatas",
  "linktitle": "MCR",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-ltr"
}
},
  "lastmod": "2022-12-14"
}

## Kas yra MCR failas?

Minecraft MCR failo formatas yra duomenų formatas, kurį Minecraft naudoja Minecraft pasaulio reljefo dalims saugoti. Jis pagrįstas NBT (Named Binary Tag) formatu, kurį sukūrė populiaraus atvirojo kodo žaidimų variklio Minecraft Forge kūrėjai. MCR failo tipas buvo pristatytas pačioje pradžioje ir vėliau buvo pakeistas [MCA file format](/game/mca/).

## MCR failo formatas

MCR failo formatas yra sudarytas kaip įvardytų dvejetainių žymų serija, kurių kiekvienoje yra tam tikro tipo duomenys. Aukščiausio lygio žyma yra Level žyma, kurioje yra visi vieno žaidimo lygio duomenys. Lygio žymoje yra keletas kitų pavadintų žymų, kuriose saugomi įvairių tipų duomenys, pvz., žyma Data, kurioje saugoma informacija apie žaidimų pasaulį, ir žymos Entities ir TileEntities, kuriose saugomi duomenys apie atitinkamai žaidimo objektai ir plytelių subjektai pasaulyje.

## Kas yra MCR failo formate?

Minecraft MCR failo formatu regionas yra 32 x 32 blokų žaidimų pasaulio sritis. MCR formatas padalina žaidimų pasaulį į regionus, kad būtų galima efektyviau valdyti duomenis ir greičiau įkelti bei išsaugoti žaidimo lygius. Kiekvienas regionas saugomas atskirame faile, o MCR failo formatas naudoja koordinačių sistemą, kad nustatytų kiekvieno regiono padėtį žaidimo pasaulyje. Regiono koordinatės nustatomos pagal apatinio kairiojo srities kampo blokų koordinates. Pavyzdžiui, regionas su koordinatėmis (-1,0) būtų vienas regionas į kairę ir nulis regionų žemiau nuo žaidimo pasaulio pradžios.

## MCR failo formato specifikacijos

MCR failo formato specifikacijos yra viešai prieinamos. NBT formato, kuriuo grindžiamas MCR formatas, specifikacijas galima rasti Minecraft Forge svetainėje. Be to, [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) taip pat turi išsamią informaciją apie MCR failo formatą, įskaitant jo struktūrą ir įvairius palaikomus duomenų tipus.

### Suspausti duomenys MCR failuose

Minecraft MCR failo formatas palaiko glaudinimą. MCR failo formatas yra pagrįstas [NBT format](https://minecraft.fandom.com/wiki/NBT_format), leidžiančiu duomenis saugoti suglaudinta forma. Tai padeda sumažinti MCR failų dydį ir veiksmingiau perkelti bei saugoti. Tai svarbi MCR failo formato savybė, nes leidžia žaidėjams dalytis dideliais Minecraft World reljefo duomenimis su kitais.

## Nuorodos

* [Pasaulinis „Minecraft“ redaktorius](https://www.mcedit.net/)

* [Apie „Minecraft“](https://www.minecraft.net/)

* [Regiono failo formatas](https://minecraft.fandom.com/wiki/Region_file_format)

* [NBT formatas](https://minecraft.fandom.com/wiki/NBT_format)


