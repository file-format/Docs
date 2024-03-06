{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ADM fails — administratīvās veidnes faila formāts",
  "description":"Uzziniet par ADM faila formātu un to, kā atvērt ADM failus.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm-lv",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Kas ir ADM fails?

ADM fails ir veidnes fails, ko izmanto Microsoft Group Policies programmatūra, lai norādītu reģistra politikas iestatījumu atrašanās vietu reģistra failā. Sistēmas administratori to izmanto, lai definētu politiku tādas datoru grupas pārvaldīšanai, kas ir daļa no grupas. Šī informācija kļūst par daļu no grupas politikas objektiem (GPO), kas tiek izveidoti grupas pārvaldībai.

ADM failus var atvērt, izmantojot Microsoft grupas politikas objektu redaktoru.

## ADM faila formāts — vairāk informācijas

ADM faili tiek saglabāti kā unikoda formatēti teksta faili. Tie galvenokārt tika izmantoti, lai aprakstītu reģistra politikas iestatījumu atrašanās vietu Windows Vista un Windows 7 reģistrā.

ADM faili vairs netiek atbalstīti, un tie ir aizstāti ar [ADMX](/system/admx/) failiem. GPA ignorē tālāk norādītos noklusējuma ADM failus datoros, kuros darbojas Microsoft Windows Vista 1. servisa pakotne vai jaunāka versija.

 * system.adm
 * inetres.adm
 * conf.adm
 * wmplayer.adm
 * wuau.adm

## Atsauces

* [Administratīvo veidņu faili — ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)

* [NetIQ — administratīvo veidņu failu pārvaldība](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)

* [SSDT](https://wiki.osdev.org/SSDT)


