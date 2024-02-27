{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "BML-filformat - Bean Markup Language File",
  "description": "Lær om BML filformat og API'er, der kan oprette og åbne BML filer.",
  "linktitle": "BML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-bm-dal"
}
},
  "lastmod": "2021-08-12"
}

## Hvad er en BML fil?

En fil med filtypenavnet .bml er en Bean Markup Language-fil, der gemmer Java-klasser til understøttelse af Java-apps. Dette giver adgang til Java-objekter og -metoder og behøver ikke oprette ny funktionalitet ved hjælp af Java-klasser. Det specificerer, hvordan komponenterne er forbundet med hinanden for at udføre nyttige opgaver. BML blev udviklet af IBM alphaWorks til at beskrive strukturer og komponenters relationer. BML-filer kan åbnes og ses ved hjælp af en hvilken som helst teksteditor, såsom webbrowsere, Microsoft Notepad og Notepad++.

## BML filformat

IBM alphaworks-webstedet har leveret to implementeringer af BML. Den første implementering er en fortolker, der 'afspiller' et BML-script for at generere det ønskede bønnehierarki. Den anden implementering er en compiler, der kompilerer ethvert BML-script til reflektionsfri Java-kode. Dette er fordelagtigt i den forstand, at det gør det muligt at fange applikationens interkomponentstruktur ved hjælp af et sprog, der er designet til dette specifikke formål med den tilføjede evne til at kompilere det til 'almindelig' Java-kode.

## BML tags

Det følgende er en forklaring på nogle af de tags, der bruges i BML-sproget:

### Det<bean> tag:

Det<bean> element bruges til at skabe nye bønner eller til at slå bønner op efter navn. Det<bean> tagget har formatet:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
id i tagget er knyttet til objektregistret for JavaBean.

### Det<string> tag

Der er to måder, hvorpå string-tagget kan bruges:

 1. Sådan opretter du en ikke-tom streng:

```
<string [value = "value of string"]> [value of string]
</string>
```
 2. Sådan opretter du en tom streng:

```
<string/>
```
## Referencer

* [Object-Oriented Messaging with XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [The Physical Markup Language](http://web.mit.edu/mecheng/pml/standards.htm)



