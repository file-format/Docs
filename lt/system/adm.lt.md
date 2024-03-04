{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ADM failas – administracinio šablono failo formatas",
  "description":"Sužinokite apie ADM failo formatą ir kaip atidaryti ADM failus.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm-lt",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Kas yra ADM failas?

ADM failas yra šablono failas, kurį naudoja Microsoft Group Policies programinė įranga, kad nurodytų registro strategijos parametrų vietą registro faile. Jį naudoja sistemos administratoriai, norėdami apibrėžti kompiuterių, kurie yra grupės dalis, valdymo politiką. Ši informacija tampa grupės strategijos objektų (GPO), kurie sukuriami grupei valdyti, dalimi.

ADM failus galite atidaryti naudodami Microsoft Group Policy Object Editor.

## ADM failo formatas – daugiau informacijos

ADM failai saugomi kaip unikodo formato tekstiniai failai. Jie pirmiausia buvo naudojami registru pagrįstų politikos nustatymų vietai aprašyti Windows Vista ir Windows 7 registruose.

ADM failai nebepalaikomi ir buvo pakeisti [ADMX](/system/admx/) failais. GPA nepaiso šių numatytųjų ADM failų kompiuteriuose, kuriuose veikia Microsoft Windows Vista 1 arba naujesnis pakeitimų paketas.

 * system.adm
 * inetres.adm
 * conf.adm
 * wmplayer.adm
 * wuau.adm

## Nuorodos

* [Administravimo šablonų failai – ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)

* [NetIQ – administracinių šablonų failų tvarkymas](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)

* [SSDT](https://wiki.osdev.org/SSDT)


