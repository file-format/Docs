{
  "date" : "2019-10-11",
  "keywords" :["xhtml", "File", "Extension", "File Format", "File Extension", "extensible html"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHTML - Extensible Hypertext Markup Language File Format",
  "description":"További információ az XHTML fájlformátumról és az API-król, amelyek XHTML-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "XHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az XHTML fájl?

Az XHTML egy szöveg alapú fájlformátum, amely XML-ben jelöli a HTML 4.0 újrafogalmazását. Ezek a fájlok kiválóan alkalmasak webböngészőben való megnyitásra vagy megtekintésre. Az XHTML-t úgy tervezték, hogy strukturáltabb, kevesebb szkriptet tartalmazzon, általános legyen; az XML összes létező lehetőségét és több eszközfüggetlenséget használ. Az XHTML egy általánosan értékes elem- és attribútumkészletet biztosít, a stíluslapokkal kombinált kiterjesztési opciókkal. Az attribútumok a metaadat-attribútumgyűjteményből kerülnek felhasználásra. Az XHTML rugalmasságot és hozzáférhetőséget biztosít azáltal, hogy az összes **[HTML](/hu/web/html/)** prezentációs elemet stíluslapoknak rendeli alá. A stíluslapok sokoldalúbbak, mint ezek a prezentációs elemek. A HTML 4.01, HTML5 és XHTML specifikációit a World Wide Web Consortium (W3C) dinamikusan fejleszti.

## Az XHTML fájlformátum rövid története

Az XHTML története a World Wide Web Consortium által 1998 decemberében kiadott dokumentumtervezettel kezdődik. Ez a dokumentum a "HTML újrafogalmazása XML-ben", az XHTML 1.0 nevű specifikációra hivatkozik. Ez az új specifikáció a meglévő elemek vagy attribútumok felhasználásával újrafogalmazta a HTML-t XML-be. 1999 májusában a W3 Consortium bejelentette, hogy a HTML 4.0-t XML-alkalmazásként alakították át. azaz XHTML. 2000. január 26-án a W3C kiadta az első XHTML 1.0-t meghatározó specifikációt. 2001. május 31-én a W3C bejelentette az XHTML-t független nyelvként, és elkezdett dolgozni a HTML 5.0 fejlesztésén. 2005-ben azonban megalakult egy munkacsoport (WHATWG), amelynek célja a közönséges HTML XHTML-től független fejlesztése volt. A WHATWG végül az XHTML 2-vel párhuzamosan kezdett el dolgozni a HTML5-ön.

## XHTML fájlformátum

Az XHTML egy formátum, amely különböző dokumentumtípusok és modulok gyűjteménye, amelyek utánozzák, kategorizálják és kiterjesztik a HTML 4-et. Az XHTML fájlok XML alapúak, és az XML alapú felhasználói ügynökökkel való együttműködésre irányulnak. Az XHTML fájlok XML-kompatibilisek. A szabványos XML-eszközök az XHTML-fájlok megtekintésére, szerkesztésére és érvényesítésére szolgálnak. A HTML Document Object Model vagy az XML Document Object Model [DOM] függő alkalmazások az XHTML dokumentumokon keresztül működhetnek. Ha ma az XHTML-t választja, a tartalomfejlesztők élvezhetik az XML összes kapcsolódó előnyét anélkül, hogy aggódnának tartalmuk előre vagy visszafelé kompatibilitása miatt.

A kapcsolódó elemek halmaza modult épít XHTML-ben. Egy űrlap- vagy táblázatmodul különféle űrlap- vagy táblázatelemeket tartalmazhat, amelyek megjeleníthetők egy weboldalon. A modularizálás célja a HTML-elemek elkülönítése volt számos kapcsolódó elemből álló halmazokká. Annak érdekében, hogy a tartalomfejlesztők kihasználhassák a modulválasztás előnyeit a különböző típusú eszközökhöz. Ezenkívül a modulok lehetővé teszik a felhasználói ügynökök számára, hogy az XHTML szabvánnyal való összhang elvesztése nélkül válasszanak ki elemeket. Az XHTML elemzési követelményei megegyeznek az XML-lel, míg a HTML a sajátját gyakorolja.

### Dokumentum megfelelőség

Az XHTML2 az XHTML 1.0 dokumentumoknak megfelelő specifikációkat kínál, amelyek az XML és XHTML 1.0 névtereinek elemeit és attribútumait használják. A dokumentumok megfelelőségének két típusa van.

A szigorúan megfelelő dokumentumok XML alapúak, és csak az ebben a specifikációban meghatározott kötelező szolgáltatásokra van szükségük. Az XHTML-fájlokhoz a következő feltételeknek kell teljesülniük:

* A fájlnak meg kell felelnie a DTD-ben és a B függelékben meghatározott megszorításoknak.
* A fájl alapelemének html-nek kell lennie.
* A fájl alapelemének tartalmaznia kell az XHTML névtér deklarációját, és a következőképpen kell meghatározni:

```
http://www.w3.org/1999/xhtml.
```

* Az alapelem a következőképpen írható:

```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Az alapelemnél korábban deklarálni kell egy DOCTYPE-ot, amelynek nyilvános azonosítójának hivatkoznia kell a három dokumentumtípus-definíció (DTD) valamelyikére. A rendszerazonosító módosítható, hogy megfeleljen a jelenlegi rendszerkonvencióknak.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

Az XML dokumentumokban szükségtelen XML deklarációkat megadni minden dokumentumban; a tartalomfejlesztőket azonban arra csábítják, hogy XML-deklarációkat használjanak minden XHTML dokumentumukban. Ezek a nyilatkozatok akkor kötelezőek, ha a dokumentum karakterkódolása eltér az UTF-8 /16-tól, vagy ha egy szabályozó protokoll nem adott meg kódolást. Az XHTML-dokumentum következő példája határozza meg az XML-deklarációkat

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

A megfelelő felhasználói ügynöknek meg kell felelnie a következő szabályoknak:

* Az XHTML-dokumentum elemzését és kiértékelését egy felhasználói ügynök végzi, amely biztosítja az XML 1.0 ajánlással való összhangját.
* A felhasználói ügynök érvényesítése esetén ellenőriznie kell a hivatkozott DTD-k dokumentumainak érvényességét az XML szerint. Amikor az XHTML fájlt a felhasználói ügynök általános XML-ként dolgozza fel, az ID típusú jellemzőket töredékazonosítóként veszi tudomásul.

Ha egy felhasználói ügynök egy ismeretlen elembe ütközik, a következő kötelező feltételeket kell teljesítenie

* feldolgozza az ismeretlen elem tartalmát
* figyelmen kívül hagyja az attribútumot és annak értékét
* Használja az alapértelmezettként megadott attribútum értékét.

Ha a felhasználói ügynök találkozik egy entitáshivatkozás-deklarációval, amelyet korábban nem dolgoztak fel, akkor azt karakterként kell feldolgozni (az „&” jellel kezdve és a pontosvesszővel végződve). A tartalomfeldolgozás során a felhasználói ügynök által megjósolható, de nem renderelhető karakterek vagy karakterentitás-hivatkozások bármilyen alternatív megjelenítést használhatnak, amely hasonló jelentést eredményez. Ebben az esetben a dokumentumot úgy kell megjeleníteni, hogy a felhasználó számára nyilvánvaló legyen, hogy a megjelenítési folyamat nem volt normális. A szóköz feldolgozásához a felhasználói ügynöknek CSS karakterekből kell kikeresnie a definíciót [CSS2].

## XHTML visszamenőleges kompatibilitás

Az XHTML 1. dokumentumok visszamenőleges kompatibilitása jól ismeri a HTML 4 felhasználói ágenseket, ha betartják a megfelelő szabályokat. Az XHTML 1.1 teljesen kompatibilis, kivéve a rubin megjegyzéseket, még akkor is, ha a HTML 4 böngészők általában figyelmen kívül hagyják őket. Az XHTML 2.0 viszonylag kevésbé kompatibilis, ennek ellenére a problémát bizonyos mértékig megoldották a szkriptek használatával.

## Hivatkozások

* [Az XHTML története: az 1990-es évektől napjainkig](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

