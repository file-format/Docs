{
  "date" : "2019-10-11",
  "keywords" :[ "yaml", ".yaml", "mi az a yaml fájl", "yaml fájl megnyitása", "kiterjesztés", "fájl", "yaml fájl", "yaml fájlformátum", ". yaml kiterjesztése" , "yaml vs json", "YAML fájl példa", "docker yaml fájl példa"],
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tudjon meg többet a YAML fájlformátumról és az API-król, amelyek YAML fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"YAML fájlformátum",
  "linktitle" : "YAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-05"
}

## Mi az a YAML fájl? ##

A **YAML fájl** egy YAML (YAML Ain't Markup Language) nyelvből áll, amely egy Unicode alapú adatsorosító nyelv; konfigurációs fájlokhoz, internetes üzenetküldéshez, objektummegmaradáshoz stb. használják. A YAML a .yaml kiterjesztést használja fájljaihoz. Szintaxisa független egy adott programozási nyelvtől. Alapvetően a YAML-t emberi interakcióra tervezték, és jól működik a modern programozási nyelvekkel. A tetszőleges natív adatszerkezetek sorosításának támogatása növelte a YAML-fájlok olvashatóságát, de kissé bonyolulttá tette az elemzési és fájlgenerálási folyamatot.

## Rövid története ##

A YAML-t először 2001-ben javasolták, és Clark Evans, Ingy döt Net és Oren Ben-Kiki fejlesztette ki. A YAML-ról először azt mondták, hogy „egy újabb jelölőnyelvet” jelent, hogy jelezze a jelölőnyelvként való célját. Később „YAML Aint Markup Language” néven újrahasznosították, hogy jelezze, hogy adatorientált.


## YAML fájlformátum ##

A YAML fájl a következő adattípusokból áll

- **Skalárok**: A skalárok olyan értékek, mint a Strings, Integers, Booleans stb.
- **Sorozatok**: A sorozatok olyan listák, amelyekben minden elem kötőjellel (-) kezdődik. A listák egymásba ágyazhatók is.
- **Leképezések**: A leképezés lehetővé teszi a kulcsok értékekkel való felsorolását.

### Szintaxis ###

- **Szóköz**: A szóközök behúzása a beágyazás és az általános szerkezet jelzésére szolgál.

``` yaml
név: John Smith
kapcsolatba lépni:
otthon: 1012355532
iroda: 5002586256
cím:
utca: |
123 Tornado Alley
Lakosztály 16
város: East Centerville
állam: KS
```

- **Megjegyzések**: A megjegyzések "#" szimbólummal kezdődnek.

``` yaml
# Ez egy YAML megjegyzés
```

- **Listák**: Kötőjel (-) a listatagok jelölésére szolgál, minden egyes tag külön sorban. A listatagok szögletes zárójelbe ([...]) is tehetők, a tagokat vesszővel (,) elválasztva.

``` yaml
  - A
  - B
  - C
```

``` yaml
[A, B, C]
```

- **Associative Array**: Az asszociatív tömböt göndör zárójelek veszik körül ({...}). A billentyűket és az értékeket kettősponttal (:), az egyes párokat pedig vessző (,) választja el.

``` yaml
  {name: John Smith, age: 20}
```

- **Strings**: A karakterlánc írható dupla idézőjelekkel (") vagy szimpla idézőjelekkel (').

``` yaml
Minta karakterlánc
"Minta karakterlánc"
"Minta karakterlánc"
```

- **Scalar Block tartalom**: A skaláris tartalom blokkjelöléssel írható a következő használatával:
  - **|**: All live breaks are significant.
  - **>**: Each line break is folded to space. It removes the leading whitespace for each line.

``` yaml
adatok: |
YAML
(YAML nem jelölőnyelv)
egy adatsorosító nyelv
```

``` yaml
adatok: ?
YAML (YAML nem jelölőnyelv)
egy adatsorosító nyelv
```

- **Több dokumentum**: A több dokumentumot három kötőjel (---) választja el egyetlen adatfolyamban. Kötőjelek jelzik a dokumentum kezdetét. A kötőjeleket az irányelvek és a dokumentumtartalom elkülönítésére is használják. A dokumentum végét három pont (...) jelzi.

``` yaml
  ---
1. dokumentum
  ---
2. dokumentum
...
```

- **Típus**: Az érték típusának megadásához dupla felkiáltójelek (!!) használatosak.

``` yaml
a: !!úszó 123
b: !!str 123
```

- **Címke**: Címke hozzárendeléséhez egy „és” jelet (&), a csomópontra való hivatkozáshoz pedig egy csillagot (*) használunk.

``` yaml
név: John Smith
számlázási cím: &id01
utca: |
123 Tornado Alley
Lakosztály 16
város: East Centerville
állam: KS

szállítási cím: *id01
```

- **Irányelvek**: A YAML-dokumentumokat folyamban direktívák előzhetik meg. Az irányelvek százalékjellel (%) kezdődnek, ezt követi a név, majd a paraméterek szóközzel elválasztva.

``` yaml
%YAML 1.2
  ---
Dokumentum tartalma
```
## YAML fájl példa
Itt láthat egy **docker yaml fájl példát** alább:

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML vs JSON
Alapvetően mind a JSON-t, mind a YAML-t úgy fejlesztették ki, hogy egy ember által olvasható adatcsere-formátumot biztosítsanak. A YAML a JSON formátum szuperkészleteként valósul meg. Ez azt jelenti, hogy a JSON-t YAML értelmezővel tudjuk elemezni. Bár ennek az elméletnek a gyakorlati megvalósítása kevéssé trükkös. Ezért az alábbiakban bemutatunk néhány alapvető különbséget a YAML és a JSON között:

|YAML| JSON|
---|---|
|A soros adatok elemzésének összetett és időigényes folyamata |Gyorsan és egyszerűen elemezheti a JSON soros adatokat egyszerűbb kialakításával|
|Kevesebb közösségi támogatás| Nagyobb közösségi támogatás és népszerűség|
|Támogatja a megjegyzéseket| Nem támogatja a megjegyzéseket|
|Lehetőség más adatobjektumok hivatkozásának használatára| Az összetett struktúrák objektumhivatkozásokkal történő sorozatosítása lehetetlen|
|A hierarchiát kettős szóközökkel jelöljük. Tabulátor karakterek nem engedélyezettek|Az objektumok és tömbök kapcsos zárójelben vannak feltüntetve.|
|Az idézőjelek nem kötelezőek, de támogatja az egy- és dupla idézőjeleket.|A karakterláncoknak dupla idézőjelben kell lenniük.|
|A gyökércsomópont bármely érvényes adattípus lehet|A gyökércsomópontnak tömbnek vagy objektumnak kell lennie.|


## Referenciák ##

- [YAML - Wikipedia](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)

