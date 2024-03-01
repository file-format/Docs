{
  "date": "2021-07-13",
  "keywords": [
"scr tiedosto",
"mikä on scr-tiedosto",
"tiedosto",
"scr esimerkki",
"scr tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "SCR - Windowsin näytönsäästäjätiedosto",
  "description": "Opi SCR-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata SCR-tiedostoja.",
  "linktitle": "SCR",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-sc-fir"
}
},
  "lastmod": "2021-07-13"
}

## Mikä on SCR-tiedosto? 
Tiedosto, jonka laajennus on .scr, on Microsoft Windows -käyttöjärjestelmän käyttämä näytönsäästäjätiedosto. Se sisältää animaatioita, grafiikkaa, diaesityksiä tai videoita, joita voidaan käyttää Windowsin näytönsäästäjänä. SCR-tiedostot tallennetaan yleensä Microsoft Windowsin päähakemistoon. Näytönsäästäjien piti estää CRT- tai plasmatietokoneiden näyttöjä kärsimästä tilasta, joka ilmenee, kun näytöllä näkyy sama kuva liian pitkään. Vaikka uusimmat näytöt eivät kärsi tällaisesta kunnossa, mutta näytönsäästäjiä käytetään silti estämään näyttöä turvallisuussyistä.

## SCR-tiedostomuoto 
Näytönsäästäjä on tietokoneohjelma, joka täyttää sen animoiduilla kuvilla tai kuvioilla, kun tietokoneella ei tapahdu mitään toimintaa pitkään aikaan. Näytönsäästäjät otettiin käyttöön estämään fosforin palaminen plasmassa, katodisädeputkissa (CRT) ja OLED-tietokonenäytöissä. Näytönsäästäjät on yleensä asetettu käyttämään perussuojaustasoa vaatimalla salasanaa laitteen avaamiseksi uudelleen. Näytönsäästäjiä kehitetään ja koodataan yleensä käyttämällä erilaisia ohjelmointikieliä sekä grafiikkaliittymiä. Useimmiten näytönsäästäjien kehittäjät käyttävät C- tai C++-ohjelmointikieliä sekä graafisia kirjastoja tai GDI:itä, kuten OpenGL:ää, joka toimii monilla 3D-renderöintiin kykenevillä alustoilla. Näytönsäästäjätuloste tallennetaan kannettavana suoritettavana tiedostona.

### SCR-tiedoston käyttö
Vanhoissa CRT- tai plasmapohjaisissa näytöissä ilmoitettiin näytön palamisesta, koska sama kuva näkyi näytöllä pitkään. Näytön palaminen on tapaus, jossa näytön sisällä olevien loisteainepinnoitteen paljaiden alueiden ominaisuudet muuttuvat vähitellen ja johtavat lopulta tummaan varjokuvaan näytölle. Joten näytönsäästäjien piti muuttaa näyttökuvaa jatkuvasti ja yleensä ne .scr-tiedostot olivat välttämättömiä pankkiautomaattien tai rautatien lippuautomaattien näytöille. Myöhemmin LCD-näytöt ja monitorien edistyneemmät versiot ratkaisivat ongelman. Siksi näytönsäästäjiä käytetään edelleen nykyaikana suojaamaan käyttämättömät laitteet toisen henkilön käytöltä. Laitteen uudelleenkäyttö vaatii salasanan tai kuvion.

## Näytönsäästäjän luominen C#:lla
Vaikka voimme luoda näytönsäästäjän millä tahansa .NET-ohjelmointikielellä, tässä annetaan C#-ohjelmointikieli:

```
class MyCoolScreensaver : Screensaver
{
   public MyCoolScreensaver()
   {
      Initialize += new EventHandler(MyCoolScreensaver_Initialize);
      Update += new EventHandler(MyCoolScreensaver_Update);
      Exit += new EventHandler(MyCoolScreensaver_Exit);
   }

   void MyCoolScreensaver_Initialize(object sender, EventArgs e)
   {
   }

   void MyCoolScreensaver_Update(object sender, EventArgs e)
   {
      Graphics0.Clear(Color.Black);
      Graphics0.DrawString(
         DateTime.Now.ToString(),
         SystemFonts.DefaultFont, Brushes.Blue,
         0, 0);
   }

   void MyCoolScreensaver_Exit(object sender, EventArgs e)
   {
   }

   [STAThread]
   static void Main()
   {
      Screensaver ss = new MyCoolScreensaver();
      ss.Run();
   }
}
```
Muuta suoritettavan tiedoston tunniste .exe-tiedostosta .scr. Joten SCR-tiedosto voidaan nimetä nimellä ScreenSaver.scr.

## Viitteet 

* [Näytönsäästäjä](https://en.wikipedia.org/wiki/Screensaver)

* [Kirjoita näytönsäästäjä, joka todella toimii](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)



