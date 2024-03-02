{
  "date": "2019-10-11",
  "keywords": [
"ascx",
"ascx tiedosto",
"ascx tiedostomuoto",
"ascx tiedostotyyppi",
"tiedosto",
"tyyppi",
"mikä on ascx-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASCX tiedostomuoto",
  "description": "Opi mikä on ASCX-tiedosto ja API:t, jotka voivat luoda ja avata ASCX-tiedostoja.",
  "linktitle": "ASCX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asc-fix"
}
},
  "lastmod": "2020-09-10"
}

## Mikä on ASCX-tiedosto?

Tiedosto, jonka laajennus on .ascx, on käyttäjän ohjausobjekti, jota käytetään uudelleenkäytettävänä osana verkkosivuilla. Siihen viitataan missä tahansa ASP-sivustossa vetämällä se ohjauslaatikosta sivulle. ASCX-käyttäjien ohjaimet lisätään projektiin keskeisenä lähteenä, minkä seurauksena käyttäjän ohjauksessa tapahtuvat muutokset näkyvät koko verkkosivustolla. Toisin kuin ASMX-tiedostot, jotka määrittävät mekanismin kommunikoida kahden objektin sisällä Internetissä, ASCX-tiedostot ovat käyttäjän ohjaimia sivuille tai verkkosivustoille upottamista varten.

## ASCX tiedostomuoto

ASCX-tiedostot kirjoitetaan vain tekstimuodossa ja voivat käyttää koodia ominaisuuksien, kuten verkkosivujen takana, jotka päättyvät .ascx.cs. Käyttäjäohjaimien merkintäkoodi alkaa @Control-käskyllä seuraavan esimerkin mukaisesti.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

Tätä verkkokäyttäjän hallintaa voidaan käyttää uudelleen useilla sivuilla, kuten sivun alatunnisteella, ylätunnisteella tai jollain sivuston navigoinnilla. Web-käyttäjien ohjaimilla on ominaisuuksia, menetelmiä ja tapahtumia, kuten kaikilla muillakin säätimillä, jotka tekevät niistä hyödyllisiä määritettäessä heidän visuaalista käyttäytymistään.

### Esimerkki käyttäjäohjaimien rekisteröimisestä web.configissa

Yhden käyttäjän ohjauksen käyttämiseksi useilla sivuilla verkkohallinta voidaan rekisteröidä web.config-tiedostoon. Tämä mahdollistaa kaikkien verkkosivustojen hallinnan sen sijaan, että rekisteröityisi jokaiselle sivulle erikseen. Seuraava esimerkkikoodi määrittää, kuinka web-ohjausobjekti rekisteröidään web.config-tiedostoon, jotta se näytetään alatunnisteena koko verkkosivustolla.

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## Viitteet

 * [ASCX User Control](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

