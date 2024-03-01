{
  "date": "2021-04-22",
  "keywords": [
".pas-tiedosto",
"pas tiedostomuoto",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "PAS - Delphi-yksikön lähdetiedosto",
  "description": "Opi PAS-tiedostomuodosta PAS-esimerkillä ja API-liittymillä, jotka voivat luoda ja avata PAS-tiedostoja.",
  "linktitle": "PAS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-pa-fis"
}
},
  "lastmod": "2021-04-22"
}

## Mikä on PAS-tiedosto?
.pas-tiedosto on itse asiassa lähdekooditiedosto, joka löytyy Delphi-ohjelmointiprojektista. Delphi on ohjelmistokehityssovellus, jota kehittäjät käyttävät Windows-pohjaisten ohjelmistojen rakentamiseen; kirjoitettu Delphin kielellä. Delphi-kieli on muunnos Object Pascal -kielestä. Joten se voidaan kääntää alkuperäiseksi Win32-koodiksi Delphi-kääntäjällä.

## PAS-tiedostomuoto

PAS-tiedostomuoto on koodaustiedosto, joka on varattu Delphi-yksikkölähteelle. Yksiköt on toteutettu Delphi-sovellusten päärakennuspalikoina. Voit tarkastella nykyisen Delphi-projektin lähdekoodia **Projekti > Näytä lähdekoodi** -valikon kautta. Ohjelmoijat voivat luoda ja tallentaa yksikön erillisenä tiedostona, jota kaikki projektit voivat käyttää. Kun yksikkö on lisätty projektiin, Delphi rekisteröi sen projektin .DPR-tiedoston uses-lauseeseen.

## PAS-tiedosto esimerkki
Kun kirjoitamme yhden rivin koodia. Delphi kirjoittaa meille monia rivejä älykkäästi. Kaikki lähdekoodi on kirjoitettu PAS-tiedostoon. Seuraavassa on perusesimerkki Delphi-lähdeyksiköstä tai PAS-tiedostosta:
```
unit Unit1;
 
 interface
 
 uses
   Windows, Messages, SysUtils, Variants, Classes, Graphics, Controls, Forms,
   Dialogs, StdCtrls;
 
 type
   TForm1 = class(TForm)
     Label1: TLabel;      // The label we have added
     Button1: TButton;    // The button we have added
     procedure Button1Click(Sender: TObject);
   private
     { private declarations }
   public
     { public declarations }
   end;
 
 var
   Form1: TForm1;
 
 implementation
 
 {$R *.dfm}
 
 // The button action we have added
 procedure TForm1.Button1Click(Sender: TObject);
 begin
   Label1.Caption := 'Hello World';    // Label changed when button pressed
 end;
 
 end.
```


## Viitteet

 * [Delphi-projektin ja yksikön lähdetiedostojen ymmärtäminen](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
 * [Kirjoittaa ensimmäistä Delphi-ohjelmaasi](http://www.delphibasics.co.uk/Article.php?Name=FirstPgm)

