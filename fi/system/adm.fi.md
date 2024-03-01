{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ADM-tiedosto - Hallintomallin tiedostomuoto",
  "description":"Opi ADM-tiedostomuodosta ja ADM-tiedostojen avaamisesta.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm-fi",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Mikä on ADM-tiedosto?

ADM-tiedosto on mallitiedosto, jota Microsoft Group Policies -ohjelmisto käyttää rekisteripohjaisten käytäntöasetusten sijainnin määrittämiseen rekisteritiedostossa. Järjestelmänvalvojat käyttävät sitä käytäntöjen määrittämiseen ryhmään kuuluvien tietokoneiden ryhmän hallintaan. Näistä tiedoista tulee osa ryhmäkäytäntöobjekteja (GPO), jotka luodaan ryhmän hallintaa varten.

Voit avata ADM-tiedostoja Microsoft Group Policy Object Editorilla.

## ADM-tiedostomuoto - lisätietoja

ADM-tiedostot tallennetaan unicode-muotoiltuina tekstitiedostoina. Niitä käytettiin ensisijaisesti Windows Vistan ja Windows 7:n rekisterin rekisteripohjaisten käytäntöasetusten sijainnin kuvaamiseen.

ADM-tiedostoja ei enää tueta, ja ne on korvattu [ADMX](/system/admx/)-tiedostoilla. GPA ohittaa seuraavat oletusarvoiset ADM-tiedostot tietokoneissa, joissa on Microsoft Windows Vista Service Pack 1 tai uudempi.

 * system.adm
 * inetres.adm
 * conf.adm
 * wmplayer.adm
 * wuau.adm

## Viitteet

* [Hallintamallitiedostot – ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)

* [NetIQ – Hallintamallitiedostojen hallinta](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)

* [SSDT](https://wiki.osdev.org/SSDT)


