{
  "date": "2022-04-07",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HAML-tiedostomuoto - Haml-lähdekooditiedosto",
  "description": "Opi HAML-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata HAML-tiedoston.",
  "linktitle": "HAML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ham-fil"
}
},
  "lastmod": "2022-04-07"
}

## Mikä on HAML-tiedosto?

HAML-tiedosto on HTML-abstraktiokuvauskielitiedosto, joka sisältää [Haml](https://haml.info/)-kielellä kirjoitetun lähdekoodin. Sitä voidaan käyttää ERB:n (Ruby template scripts) korvaajana. HAML-tiedosto sisältää mallin lähdekoodin, jolla luodaan verkkodokumentin HTML-koodi. ERB-tiedostot voidaan korvata yksinkertaisesti korvaamalla nämä sovellus/näkymät-kansiossa olevat tiedostot Hamliin vaihtamalla tiedoston tunniste. HAML-tiedostoja voidaan avata millä tahansa tekstieditorilla, kuten Microsoft Notepad, Notepad++, Apple TextEdit,

## HAML-tiedostomuoto

HAML-tiedostot ovat lähdetiedostoja, jotka on tallennettu levylle tekstitiedostoina. Se sisältää HAML-syntaksilla kirjoitetun koodin. HAML korvaa **<>**-tunnisteet **%**-merkillä koodin yksinkertaistamiseksi ja helpottamiseksi. ERB-tiedostot voidaan korvata HAML:lla seuraavan yksinkertaisen esimerkin mukaisesti.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### HAML-esimerkki

Seuraava on esimerkki Hello World -esimerkki HAML:stä.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
joka renderöi seuraavan HTML-tulosteen.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Viitteet

* [HAML - Github](https://github.com/haml/haml)


