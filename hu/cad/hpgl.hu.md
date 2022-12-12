{
  "date" : "2020-07-28",
  "keywords" :[ "HPGL", "Fájlformátum", "Megnyitás", "Olvasás", "Létrehozás", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a HPGL fájlformátumról és az API-król, amelyek HPGL fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"HPGL fájlformátum – Tanuljon a fájlformátum-szakértőktől!",
  "linktitle" : "HPGL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Mi az a HPGL fájl?

Egy HPGFL (Hewlett-Packard Graphics Language) fájl tartalmazza a HP által kifejlesztett plottervezérlési utasításkészletet. A HP plotterek ezt a fájlt használják vektor- és rasztertartalom rajzolására és nyomtatására a papírra.

### HPGL parancs

A HPGL parancs a következőkből áll.
* Az ábécé két karakterből álló parancsrésze
* Paraméter rész
* Terminátor rész

A fájlban minden paramétert elválasztóval kell elválasztani több paraméter esetén.

### HPGL parancs példa

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Koordináta-rendszer

A koordinátarendszerek kétdimenziós mérési mutatókból állnak, amelyek lehetővé teszik bármely konkrét hely meghatározását. A HPGL mind a Plotter, mind a felhasználói koordinátarendszert használja erre a célra.

#### Plotter koordinátarendszer

Ezt a koordinátarendszert a plotter mozgásán alapuló rajzok ábrázolására használják. A plotter minimális mozgásának tipikus XY egysége 0,025 mm. A lehetséges rajztartomány a plotter fajtákkal változik.

#### Felhasználói koordinátarendszer

A felhasználó által megadott koordináta-rendszer a skála és az origó segítségével állítható be. Ezeket az IP paranccsal és az SC paranccsal plotter koordinátákká alakítja. A plotter rendszer koordinátái alapértelmezés szerint használatosak, ha ez az átalakítás nem történik meg.

## HPGL fájlformátum
A HPGL fájlok ASCII (szövegfájl) formátumúak, és néhány beállítási paranccsal kezdődnek. Ez beállít bizonyos paramétereket a plotter számára a nyomtatáshoz. Egy tipikus HPGL-fájl a következőképpen néz ki.

|Parancs|Jelentés
---|---|
|IN;|inicializál, rajzolási munka indítása|
|IP;|állítsa be a skálázási pontokat (P1 és P2) az alapértelmezett helyzetükre|
|SP1;|válasszon tollat 1|
|PU0,0;|emelje fel a tollat, és lépjen a következő művelet kezdőpontjára|
|PD100,0,100,100,0,100,0,0;|tedd le a tollat, és menj a következő helyekre (rajzolj egy négyzetet az oldal köré)|
|PU50,50;|Pen Up és lépjen az X,Y koordinátákra 50,50|
|CI25;|rajzoljon egy 25| sugarú kört
|SS;|válaszd a szabványos karakterkészletet|
|DT*,1;|állítsd a szöveghatárolót csillagra, és ne nyomtasd ki őket (az 1, azaz "igaz")|
|PU20,80;|emelje fel a tollat és lépjen 20,80|-ra
|LBHello World*;|rajzolj címkét|

## Hivatkozások
* [HPGL a Wikipedia által](https://en.wikipedia.org/wiki/HP-GL)
* [HPGL referenciaútmutató](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)

