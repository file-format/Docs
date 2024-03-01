{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ADMX-tiedosto - Ryhmäkäytännön hallintamallin tiedostomuoto",
  "description":"Opi ADMX-tiedostomuodosta ja ADMX-tiedostojen avaamisesta.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx-fi",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Mikä on ADMX-tiedosto?

An ADMX file is a policy configuration file used by Microsoft Windows Group Policy software that manages group of computers in a group. It is an XML-based administrative template file and was introduced with Windows Vista Service Pack 1. ADMX-tiedostot sisältävät käyttäjätilien, käyttöjärjestelmän kokoonpanojen ja sovellusten määritysasetuksia. ADMX-tiedostoja käytetään konfiguraatioiden tallentamiseen ja käyttöönottoon monien tietokonejärjestelmien keskitettyä hallintaa varten.

Voit luoda tai muokata ADMX-tiedostoja millä tahansa XML-yhteensopivalla, millä tahansa tekstieditorilla tai Microsoft Group Policy Object Editorilla.

## ADMX-tiedostomuoto - lisätietoja

ADMX-tiedostot on tallennettu yleisessä [XML](/web/xml/)-tiedostomuodossa, joka on ihmisen luettavissa. Se on monikielinen tiedostomuoto, ja sen avulla eri kielten järjestelmänvalvojat voivat työskennellä samojen ADMX-tiedostojen kanssa. ADMX-tiedostot korvasivat vanhan [ADM](/system/adm/)-tiedostomuodon, joka on unicode-muotoiltu tekstitiedostomuoto. ADMX-tiedostot määrittävät rekisteriavaimet, jotka muuttuvat, kun tiettyä ryhmäkäytäntöasetusta muutetaan.

### Mitä voin tehdä ADMX-tiedostolla?

ADMX-tiedostot määrittelevät, mitkä toiminnot sallitaan ryhmään kuuluville käyttäjien tietokoneille. Ryhmäkäytäntö asettaa säännöt, jotka on asetettu yhdessä Active Directory -ohjelmiston kanssa. ADMX-tiedostoja hallitaan Windows-käyttöjärjestelmän keskussäilöstä, joka on toimialueen keskeinen sijainti.

Työympäristössä käyttöön otettu ADMX-tiedosto voi antaa järjestelmänvalvojille mahdollisuuden toteuttaa käytäntöjä, kuten:

 * Hallitse Internetin käyttöä
 * Tiettyjen tiedostotyyppien lataaminen
 * Irrotettavien laitteiden käyttö järjestelmissä

## Viitteet

* [Hallintamallitiedostot – ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)

* [NetIQ – Hallintamallitiedostojen hallinta](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)

* [SSDT](https://wiki.osdev.org/SSDT)


