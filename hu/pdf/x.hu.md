{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDF/X fájlformátum",
  "description":"További információ a PDF/X fájlformátumról és az API-król, amelyek PDF/X fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "PDF/X",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Mi az a PDF/X fájl? #

A PDF/X egy ISO 15930 szabvány, amelyet 2001-ben tettek közzé a PDF funkciók egy részével. A szabványt a nyomda- és kiadóipar sajátos követelményei alapján hozták létre és tették közzé. A szabvány követelményeit a nyomdaipar és a kiadóipar különféle igényei szerint dolgozták ki. A PDF/X megköveteli, hogy a megfelelő fájlok teljesek, azaz önállóak legyenek. Ez megköveteli, hogy az oldalon használt elemek, például a betűtípusok a dokumentum részét képezzék. Az olyan tartalom, mint a 3D vagy a videó, nem lehet PDF/X dokumentum része. A PDF/X dokumentumban szereplő információknak pontosnak kell lenniük.

## PDF/X szabványok és változatok ##

A PDF/X szabványcsalád több verzióból áll, amelyek mindegyike speciális eredményre készült. E szabványok kidolgozásának célja a nyomda- és kiadóipar sokféle igényének kielégítése volt.

* `PDF/X-1a` – A PDF/X család első szabványaként is ismert PDF/X-1a megköveteli, hogy minden tartalom a PDF dokumentum részét képezze ahhoz, hogy ki lehessen nyomtatni. A dokumentumelemek, például a betűtípusok, űrlapok, jelszavas védelem és látható megjegyzések nem engedélyezettek. A PDF/X-1a-nak megvannak a maga sajátos követelményei, valamint megengedettek például az átlátszóságra és a rétegekre vonatkozó követelmények. Ezekhez a nyomtatási elemeknek is csak CMYK-, szürkeárnyalatos vagy direkt színeket kell használniuk, így nem kell RGB-t vagy eszközfüggetlen színteret használni. olyan cserék számára készült, amelyekben az összes fájlt CMYK-ban (és/vagy direkt színekben) kell kézbesíteni, RGB vagy színkezeléssel kezelt adatok nélkül. A PDF/X-1a-t Complete Exchange-nek is nevezik, az általuk igényelt információk teljessége miatt
* `PDF/X-3` - 2002-ben vezették be, és megszüntette a PDF/X-1a számos korlátozását. Ez lehetővé tette a PDF/X-3 grafikák számára a CMYK, grescale, RGB, Lab és ICC alapú színterek használatát. Valójában az 1.3-as PDF-szabványokon alapul [ICC-profil](https://en.wikipedia.org/wiki/ICC_Profile). Színkezelésnek is nevezik a PDF-dokumentumokban szereplő színekkel kapcsolatos rugalmassága és szabályai miatt.
* `PDF/X-4` - támogatja az írásvetítő-fóliákat, így a PDF-X/4 tartalmazza a lapítás nélküli kimenethez szükséges összes adatot.
* `PDF/X-5` - PDF/X-4 alapú, amely támogatja a külső grafikákat referencia XObjects-en keresztül, valamint külső n-színező profilokat a rendereléshez. Használja a nyomtatási adatok részleges cseréjére a PDF 1.6-os verziójával

## Referenciák ##

* [PDF/X – a Wikipédia által](https://en.wikipedia.org/wiki/PDF/X)

