{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ADMX failas – grupės strategijos administracinio šablono failo formatas",
  "description":"Sužinokite apie ADMX failo formatą ir kaip atidaryti ADMX failus.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx-lt",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Kas yra ADMX failas?

An ADMX file is a policy configuration file used by Microsoft Windows Group Policy software that manages group of computers in a group. It is an XML-based administrative template file and was introduced with Windows Vista Service Pack 1. ADMX failuose yra vartotojo abonementų, operacinės sistemos konfigūracijų ir programų konfigūracijos nustatymai. ADMX failai naudojami daugelio kompiuterių sistemų centralizuoto valdymo konfigūracijoms saugoti ir įdiegti.

Galite kurti arba redaguoti ADMX failus naudodami bet kurį su XML suderinamą teksto rengyklę arba Microsoft Group Policy Object Editor.

## ADMX failo formatas – daugiau informacijos

ADMX failai saugomi universaliu [XML](/web/xml/) failo formatu, kurį gali skaityti žmogus. Tai daugiakalbis failo formatas ir leidžia skirtingų kalbų sistemos administratoriams dirbti su tais pačiais ADMX failais. ADMX failai pakeitė senąjį [ADM](/system/adm/) failo formatą, kuris yra unikodo formato teksto failo formatas. ADMX failai nurodo registro raktus, kurie keičiami, kai pakeičiamas tam tikras grupės strategijos parametras.

### Ką daryti su ADMX failu?

ADMX failai apibrėžia, kokie veiksmai turi būti leisti vartotojų kompiuteriams, kurie yra grupės dalis. Grupės politika nustato taisykles, nustatytas kartu su Active Directory programine įranga. ADMX failai valdomi iš centrinės Windows OS parduotuvės, kuri yra pagrindinė domeno vieta.

ADMX failas, įdiegtas darbo aplinkoje, gali leisti administratoriams įgyvendinti tokias strategijas kaip:

 * Kontroliuoti interneto naudojimą
 * Tam tikrų tipų failų atsisiuntimas
 * Nuimamų įrenginių naudojimas sistemose

## Nuorodos

* [Administravimo šablonų failai – ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)

* [NetIQ – administracinių šablonų failų tvarkymas](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)

* [SSDT](https://wiki.osdev.org/SSDT)


