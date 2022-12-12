{
  "date" : "2021-07-29",
  "keywords" :[ "soubor pes", "formát souboru pes", "co je soubor pes", "soubor", "příklad pes", "přípona souboru pes", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru PES - formát Brother PE Embroidery",
  "description":"Další informace o formátu souboru PES a rozhraních API, která mohou vytvářet a otevírat soubory PES.",
  "linktitle" : "PES",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## Co je to vyšívací soubor PES?

Vyšívací soubor PES je soubor návrhu, který obsahuje pokyny pro vyšívací/šicí stroje. Byl vyvinut společností Brother Industries pro jejich vyšívací stroje, ale později byl formalizován jako obecný formát souborů. PES soubory používají šicí stroje ke čtení pokynů pro přišívání vzorů na látku. Tyto soubory slouží dvěma účelům; za prvé poskytuje informace o návrhu pro aplikaci PE-Design vyvinutou společností Brother Industries a za druhé poskytuje název návrhu, barvy a kódy vyšívacího stroje, jako je „stop“, „skok“ a „trim“.

## Formát souboru PES – Další informace

Soubor PES se uloží na disk v binárním formátu souboru. Obsahuje několik sekcí, které mají informace o šití uložené pomocí předdefinované metody. Formát souboru PES je následující.

* Údaje o verzi – Poskytuje informace o verzi a může mít libovolnou hodnotu `#PES0001`, `#PES0020`, `#PES0030`, `#PES0040`, `#PES0050`, `#PES0055`, `#PES0060`
* Hodnota hledání PEC – 4bajtové celé číslo typu little-endian, které bezprostředně následuje po datech verze a představuje hodnotu hledání pro sekci PEC, která obsahuje podrobnosti návrhu Informace
* Sekce PSE – Obsahuje informace o designu relevantní pro Brother PE-Design a může jít o další šicí aplikace
* Sekce PCE – Může být kdekoli v souboru PSE, ale odkazuje na ni PEC Seek Value.

## Typ šicích strojů používajících soubor PES

Soubory PES jsou primárně vytvářeny softwarem PE-Design používaným se šicími stroji Brother. Některé další stroje, které mohou podporovat soubory PES, zahrnují domácí vyšívací stroje Babylock a Bernina.

## Jak převést soubory PSE?

Softwarová aplikace PE-Design může [převést soubor PSE](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl =pes+file) na jiné formáty, jako jsou .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd nebo .xxx. To lze provést pomocí aplikace PE-Design otevřením souboru a výběrem formátu konverze.

## Reference

* [PE Design – návod k použití](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)

