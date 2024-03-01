{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "BML-tiedostomuoto - Bean Markup Language -tiedosto",
  "description": "Opi BML-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata BML-tiedostoja.",
  "linktitle": "BML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-bm-fil"
}
},
  "lastmod": "2021-08-12"
}

## Mikä on BML-tiedosto?

Tiedosto, jonka pääte on .bml, on Bean Markup Language -tiedosto, joka tallentaa Java-luokat Java-sovelluksia tukevia sovelluksia varten. Tämä mahdollistaa pääsyn Java-objekteihin ja -menetelmiin, eikä sinun tarvitse luoda uusia toimintoja Java-luokkien avulla. Se määrittää, kuinka komponentit on kytketty toisiinsa hyödyllisten tehtävien suorittamiseksi. IBM alphaWorks on kehittänyt BML:n kuvaamaan rakenteita ja komponenttien suhteita. BML-tiedostoja voidaan avata ja tarkastella millä tahansa tekstieditorilla, kuten Web-selaimilla, Microsoft Notepadilla ja Notepad++:lla.

## BML-tiedostomuoto

IBM alphaworks -sivustolla on kaksi BML-toteutusta. Ensimmäinen toteutus on tulkki, joka toistaa BML-skriptin halutun papuhierarkian luomiseksi. Toinen toteutus on kääntäjä, joka kääntää minkä tahansa BML-komentosarjan heijastusvapaaksi Java-koodiksi. Tämä on edullista siinä mielessä, että se mahdollistaa sovelluksen komponenttien välisen rakenteen kaappaamisen tähän tarkoitukseen suunnitellulla kielellä, johon on lisätty mahdollisuus kääntää se tavalliseksi Java-koodiksi.

## BML-tunnisteet

Seuraavassa on selitys joistakin BML-kielessä käytetyistä tunnisteista:

### The<bean> tag:

The<bean> elementtiä käytetään uusien papujen luomiseen tai papujen etsimiseen nimen perusteella. The<bean> tagi on muodossa:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
Tunnisteen id liittyy JavaBeanin objektirekisteriin.

### The<string> tag

Merkkijonotunnistetta voidaan käyttää kahdella tavalla:

 1. Ei-tyhjän merkkijonon luominen:

```
<string [value = "value of string"]> [value of string]
</string>
```
 2. Tyhjän merkkijonon luominen:

```
<string/>
```
## Viitteet

* [Object-Oriented Messaging with XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [The Physical Markup Language](http://web.mit.edu/mecheng/pml/standards.htm)



