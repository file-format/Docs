{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "BML failo formatas – pupelių žymėjimo kalbos failas",
  "description": "Sužinokite apie BML failo formatą ir API, kurios gali kurti ir atidaryti BML failus.",
  "linktitle": "BML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-bm-ltl"
}
},
  "lastmod": "2021-08-12"
}

## Kas yra BML failas?

Failas su plėtiniu .bml yra pupelių žymėjimo kalbos failas, kuriame saugomos Java klasės, skirtos Java programoms palaikyti. Tai leidžia pasiekti Java objektus ir metodus ir nereikia kurti naujų funkcijų naudojant Java klases. Jame nurodoma, kaip komponentai yra sujungti vienas su kitu, kad būtų galima atlikti naudingas užduotis. BML sukūrė IBM alphaWorks, kad apibūdintų struktūras ir komponentų ryšius. BML failus galima atidaryti ir peržiūrėti naudojant bet kurį teksto rengyklę, pvz., žiniatinklio naršykles, Microsoft Notepad ir Notepad++.

## BML failo formatas

IBM alphaworks svetainė pateikė du BML diegimus. Pirmasis diegimas yra interpretatorius, kuris paleidžia BML scenarijų, kad sukurtų norimą pupelių hierarchiją. Antrasis įgyvendinimas yra kompiliatorius, kuris sukompiliuoja bet kurį BML scenarijų į Java kodą be atspindžių. Tai naudinga ta prasme, kad leidžia užfiksuoti tarpkomponentinę programos struktūrą, naudojant šiam konkrečiam tikslui sukurtą kalbą, su papildoma galimybe ją kompiliuoti į įprastą Java kodą.

## BML žymės

Toliau pateikiamas kai kurių BML kalboje naudojamų žymų paaiškinimas:

### The<bean> žyma:

The<bean> elementas naudojamas kuriant naujas pupeles arba ieškant pupelių pagal pavadinimą. The<bean> žyma yra tokio formato:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
Žymos id yra susietas su JavaBean objektų registru.

### The<string> žyma

Yra du būdai, kaip naudoti eilutės žymą:

 1. Norėdami sukurti netuščią eilutę:

```
<string [value = "value of string"]> [value of string]
</string>
```
 2. Norėdami sukurti tuščią eilutę:

```
<string/>
```
## Nuorodos

* [Object-Oriented Messaging with XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [The Physical Markup Language](http://web.mit.edu/mecheng/pml/standards.htm)



