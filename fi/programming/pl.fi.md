{
  "date": "2021-07-23",
  "keywords": [
"PL",
"tiedosto",
"laajennus",
"muoto",
"Perl",
"Perl kieli",
"PL tiedostot",
"ohjelmointi"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Opi PL-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata PL-tiedostoja.",
  "title": "PL-tiedosto - Perl-skriptitiedostomuoto",
  "linktitle": "PL",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-p-fil"
}
},
  "lastmod": "2021-07-23"
}

## Mikä on PL-tiedosto?

Tiedosto, jonka pääte on .pl, on Perl Script -tiedosto, joka on komentosarjakieli. Nämä käännetään ja ajetaan Perl Interpreter -ohjelmistolla. PL-skriptitiedosto sisältää koodirivejä, muuttujia ja kommentteja. Komentosarjakieliä on suhteellisen vaikea käyttää
ymmärtää muita ohjelmointitiedostomuotoja, kuten {{HYPERLINKKI}}. PL-tiedostoja voidaan luoda ja ne ovat yhteensopivia Windowsin, macOS:n ja Linuxin kanssa.

## Perl-komentosarjakielen lyhyt historia

Tämä kieli otettiin ensimmäisen kerran käyttöön vuonna 1987, joten nämä tiedostot saivat alkuperänsä samana vuonna. Vuonna 1989 Perl 2 julkaistiin. Myöhemmin sitä on päivitetty ja sitä on muokattu 5.35-versioon asti, ja seuraava versio on tarkoitus julkaista ensi vuonna.

Jokaiseen päivitykseen on lisätty työkaluja kielen ja tiedostojen toimivuudesta, suorituskyvystä ja ulkoasusta. Versioihin on tehty monia tarkistuksia näiden vuosien aikana. Se oli alun perin perusskriptikieli, mutta nyt se sisältää myös monia muita moduuleja. Alun perin se oli hyvin yksinkertainen kieli, mutta tämän kielen kirjoituksia oli melko vaikea ymmärtää, koska ne olivat kompakteja.

## Perl-tiedostomuodon laajennustiedot

Näillä ohjelmointitiedostoilla on joitain ominaisuuksia tai määrityksiä, joista osa on seuraavat:

* Näihin tiedostoihin sisältyvä koodi on vain tekstimuodossa ja sitä käytetään skriptien kehittämiseen
* Palvelimen komentosarjat, tekstin jäsentäminen ja palvelimen hallinta ovat tärkeimmät näkökohdat, jotka tämän kielen komentosarja kattaa
* Monet tähän kieleen liittyvät suositut ohjelmat ovat Active State Active Perl ja Bare Bones BBEdit (yhteensopiva Mac OS:n kanssa)
* Tätä kieltä pidetään korkean tason kielenä
* Win32:ssa käyttäjän on ehkä asennettava kielen alkuperäinen binäärijakelu
* Se vaatii joitain komentosarjatyökaluja tullakseen suoritettaviksi erilaisissa Windows Resource Kitsissä
* Visual Studio .NET on kuuluisa ohjelmointikielten kehittämisen kehys. Active State -työkalua, joka tunnetaan nimellä Visual Perl, käytetään lisäämään Perl Visual Studioon
* Tiedostoissa lähdekoodin ensimmäinen rivi kuvaa käytettävän tulkin tiedot. PL-tiedostot alkavat yleensä rivillä **#!/usr/bin/perl**, joka käskee tietokonettasi suorittamaan tämän komentosarjan käyttämällä tietokoneeseen asennettua Perl-tulkkia.


## PL-skriptiesimerkkejä

```
#!/usr/bin/perl
print "Hello, world\n";
```

Tämä tulostetaan

```
Hello, World
```

### Yksirivinen kommentti ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### Monirivinen kommentti ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### Muuttujatehtävä ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### Skalaarimuuttujien määritys ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### Yksinkertaiset skalaarioperaatiot ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## Viitteet ##

- {{HYPERLINKKI}})

