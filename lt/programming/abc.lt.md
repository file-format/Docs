
{
  "date": "2021-12-14",
  "keywords": [
".abc failą",
"pratęsimas",
"formatu",
"ActionScript baito kodo failas",
"kaip atidaryti .abc failą",
"abc failo formatas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ABC – ActionScript baito kodo failas",
  "description": "Sužinokite, kas yra ABC failo formatas, naudodamiesi pavyzdžiu ir API, kurios gali kurti ir atidaryti ABC failus.",
  "linktitle": "ABC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ab-ltc"
}
},
  "lastmod": "2021-12-14"
}

## Kas yra ABC failas?

Failas su plėtiniu .abc yra ActionScript baitų kodo failas, sukurtas Flash kompiliatoriaus sukūrus ActionScript scenarijaus failus. ABC faile esantį baitų kodą vykdo ActionScript virtualioji mašina (AVM ir AVM2). Baitų kodą sudaro pastovūs duomenys, instrukcijos iš AVM2 instrukcijų rinkinio ir įvairių rūšių metaduomenys. Kai ABC failas įkeliamas į AVM arba AVM2, jis tikrinamas. Jei jis neatitinka AVM2 apžvalgos, jis atmetamas. ABC failus galima atidaryti naudojant Adobe Flash Player, kuris buvo seniai nutrauktas.

## ABC failo formatas – daugiau informacijos

ABC failai išsaugomi diske dvejetainiu formatu, kurį gali nuskaityti AVM arba AVM2 virtualios mašinos. Jo vidinė failo struktūra yra vykdomojo kodo blokas su visais nuolatiniais duomenimis, tipo deskriptoriais, kodu ir metaduomenimis.

## ABC failo struktūra

ABC failo struktūra yra tokia, kaip parodyta žemiau.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### ABC failų laukai

|Lauko pavadinimas|Aprašymas|
---|---|
|minor_version, major_version|Didysis_version ir minor_version reikšmės yra pagrindinės ir mažosios abcFile formato versijų numeriai.|
|constant_pool|Constant_pool yra kintamo ilgio struktūra, sudaryta iš sveikųjų skaičių, dvigubų, eilučių, vardų erdvių, vardų erdvių rinkinių ir kelių pavadinimų.|
|method_count, method|method_count reikšmė yra įrašų skaičius metodo masyve. Kiekvienas metodo masyvo įrašas yra kintamo ilgio method_info struktūra.|
|metadata_count, metadata|Metadata_count reikšmė yra metaduomenų masyvo įrašų skaičius. Kiekvienas metaduomenų įrašas yra metadata_infostructure, susiejanti pavadinimą su eilutės reikšmių rinkiniu. |
|class_count, instance, class|Class_count reikšmė yra egzemplioriaus ir klasių masyvų įrašų skaičius. |
|script_count, script|Script_count reikšmė yra įrašų skaičius scenarijaus masyve. Kiekvienas scenarijaus įrašas yra script_info struktūra, apibrėžianti vieno scenarijaus šiame faile charakteristikas. |
|method_body_count, method_body|Metod_body_count reikšmė yra metodo_kūno masyve esančių įrašų skaičius. Kiekvieną method_bodyentry sudaro kintamo ilgio method_body_info struktūra, kurioje yra atskiro metodo ar funkcijos instrukcijos.|

## Nuorodos

 * [Tvirtas ABC (ActionScript Bytecode) [Dis-]Assembler – Github](https://github.com/CyberShadow/RABCDAsm)

