{
  "date": "2019-10-11",
  "keywords": [
"asax",
"asax tiedosto",
"asax tiedostomuoto",
"asax tiedostotyyppi",
"tiedosto",
"tyyppi",
"mikä on asax-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASAX - ASP.NET-palvelinsovellustiedosto",
  "description": "Opi tuntemaan, mikä on ASAX-tiedosto ja API:t, jotka voivat luoda ja avata ASAX-tiedostoja.",
  "linktitle": "ASAX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asa-fix"
}
},
  "lastmod": "2021-06-07"
}

## Mikä on ASAX-tiedosto?

Tiedosto, jonka laajennus on .asax, on ASP.NET-sovellusten käyttämä tiedosto, joka sijaitsee palvelinpuolella. Se sisältää koodin, jolla vastataan ASP.NET- tai HTTP-moduulien herättämiin sovellus- ja istuntotason tapahtumiin. Tämä sisältää myös tiettyjen tapahtumien käsittelyn, kun sovellus käynnistyy tai sammuu. ASAX-tiedostot ovat valinnaisia, ja vain yksi ASAX-tiedosto lisätään verkkosovelluksiin käsittelemään sovellustason tapahtumia ja virheitä globaalilla tasolla. Toisin kuin ASPX-sivut, ASAX-tiedostot eivät sisällä koodia sovelluksen toiminnallisuuden toteuttamiseksi.

## ASAX tiedostomuoto

ASAX-tiedostot on kirjoitettu vain tekstitiedostomuodossa ja ne ovat ihmisen luettavissa. Yleisimmin käytetty ASAX-tiedosto on Global.asax, joka sijaitsee ASP.NET-sovelluksen juurihakemistossa. Web-palvelimet on määritetty hylkäämään kaikki tähän tiedostoon saapuvat puhelut estääkseen käyttäjiä lataamasta tai katsomasta tämän tiedoston koodia.

### Global.ASAX - Esimerkki ASAX-tiedostomuodosta

Yksi ASAX-tiedosto koostuu useista osista, jotka on kirjoitettu käsittelemään sovellustason tapahtumia. Nämä ovat seuraavat.

 * **Sovellusdirektiivit** – Sovellusdirektiivit ovat tunnisteita, joita käytetään määrittämään valinnaisia sovelluskohtaisia asetuksia, joita ASP.NET-jäsentäjä käyttää Global.asax-tiedoston käsittelyn aikana. Nämä käskyt sijaitsevat Global.asax-tiedoston alussa ja määritellään seuraavasti.

```
<%@ direktiivi attribuutti=arvo [attribuutti=arvo … ]%>
```
 * **Koodin ilmoituslohkot** - Koodiilmoituslohkoja käytetään määrittämään palvelinkoodin osia, jotka on upotettu ASP.NET-sovellustiedostoihin \-tiedostossa.<script> blocks marked with a runat=server attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

```
<html>
  <script language="C#" runat="server">
      void EnterBtn_Click(Object Src, EventArgs E) {
          Message.Text = "Hi " + Name.Text + ", welcome to ASP.NET!";
  }
  </script>

  <body>
   <form runat="server">
    Enter your name: <asp:textbox id="Name" runat=server/>
                     <asp:button text="Enter" Onclick="EnterBtn_Click" runat="server"/>
        <p>
        <asp:label id="Message" runat=server/>
    </form>
  </body>
</html>
```
 * **Koodin renderöintilohkot** - Nämä määrittävät rivin sisäisen koodin tai lausekkeet, jotka suoritetaan, kun sivu hahmonnetaan. Kaksi koodinrenderointilohkotyyliä sisältävät rivin koodin ja rivin lausekkeet. Ensin mainittua käytetään määrittelemään itsenäisiä koodirivejä tai -lohkoja, kun taas lateraalista käytetään pikakuvakkeena Write-menetelmän kutsumiseen.

## Viitteet

 * [HTTP-käsittelijöiden ja HTTP-moduulien yleiskatsaus](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
 * [Global.asax Syntax](https://learn.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

