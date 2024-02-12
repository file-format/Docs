{
  "date" : "2024-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CUBE File - Gaussian Cube File - Co je soubor .cube a jak jej otevřít?",
  "description" : "Přečtěte si o souboru Gaussian Cube File a o tom, jak jej otevřít.",
  "linktitle" : "CUBE",
  "menu" : {
    "docs" : {
      "identifier" : "data-cs-cube",
      "parent" : "data"
    }
  },
  "lastmod" : "2024-01-25"
}

## Co je soubor CUBE?

Souborový formát CUBE, také známý jako soubor Gaussovy krychle (.cube), se používá ve výpočetní chemii pro ukládání molekulárních dat, zejména informací o hustotě elektronů vyplývajících z výpočtů kvantové chemie. Tento formát je běžně spojován s **Gaussovským softwarovým balíčkem**, který je široce používán pro provádění ab initio výpočtů elektronické struktury.

Soubory Gaussian Cube ukládají trojrozměrná data, která obvykle představují elektronovou hustotu nebo jiné vlastnosti molekul, získaná pomocí výpočtů kvantové chemie. Soubor obsahuje sekci záhlaví s metadaty (jako je počátek, počet datových bodů podél každé osy a rozestupy), následovanou mřížkou číselných hodnot představujících zájmovou vlastnost (např. hustotu elektronů) v každém bodě mřížky v prostoru.

Soubor Gaussian Cube (.cube) je prostý textový soubor se specifickou strukturou. Záhlaví obsahuje informace o molekulárním systému a datové mřížce a datové hodnoty jsou uspořádány ve formátu trojrozměrné mřížky. Soubory Gaussian Cube se často používají k vizualizaci molekulárních vlastností pomocí softwaru pro molekulární vizualizaci. Programy jako **VMD (Visual Molecular Dynamics)** nebo **PyMOL** mohou číst soubory Gaussovy krychle a zobrazovat molekulární povrchy, elektronovou hustotu nebo jiné vypočítané vlastnosti.

## Zjednodušený příklad souboru Gaussian Cube:

```
Příklad souboru Cubefile
Generováno Gaussianem
   0 1 0 0 0 0 0 0 0 0
   0,000000000000000E+00 0,000000000000000E+00 0,0000000000000000E+00
  50 0,1000000000000000E+01 0,0000000000000000E+00 0,0000000000000000E+00
  50 0,0000000000000000E+00 0,100000000000000E+01 0,0000000000000000E+00
  50 0,0000000000000000E+00 0,0000000000000000E+00 0,1000000000000000E+01
    0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02
    ... (hodnoty dat pro hustotu elektronů v každém bodě mřížky)
```

## O Gaussově

Gaussian je sada softwarových aplikací pro kvantovou chemii a výpočetní chemii. Gaussian se primárně zaměřuje na ab initio metody kvantové chemie, což jsou vysoce přesné, ale výpočetně náročné přístupy ke studiu elektronové struktury molekul. Tento software je široce používán ve výzkumu a akademickém prostředí pro různé aplikace, včetně předpovídání molekulárních vlastností, studia reakčních mechanismů a zkoumání molekulárních struktur.

## O NWChem

NWChem je open-source software pro výpočetní chemii navržený pro vysoce výkonné simulace kvantové chemie. Využívá ab initio metod, jako je Hartree-Fock a teorie funkcionálních funkcí hustoty, podporuje paralelní výpočty pro efektivní výpočty na klastrech a nachází uplatnění v různých vědeckých oborech, včetně výpočetní chemie, biochemie a vědy o materiálech. NWChem je známý svou všestranností, která umožňuje výzkumníkům studovat různé chemické systémy, a jeho open source povaha podporuje příspěvky komunity a přizpůsobení.

## O VMD

VMD, což je zkratka pro Visual Molecular Dynamics, je výkonný a široce používaný molekulární vizualizační program pro zobrazování, analýzu a animaci trajektorií molekulární dynamiky (MD) a také statických molekulárních struktur. Je obzvláště populární v oblastech výpočetní chemie, molekulární biologie a strukturální bioinformatiky. VMD vyniká ve vizualizaci molekulárních struktur a poskytuje vysoce kvalitní 3D vykreslování molekul a molekulárních komplexů. Podporuje různé formáty molekulárních souborů.

## O PyMOL

PyMOL je molekulární vizualizační systém a softwarový nástroj používaný pro trojrozměrnou vizualizaci molekulárních struktur. Je obzvláště populární v oblastech strukturní biologie, bioinformatiky a výpočetní chemie. PyMOL poskytuje vysoce kvalitní 3D vykreslování molekulárních struktur, což uživatelům umožňuje vizualizovat a zkoumat tvary, povrchy a interakce biologických makromolekul.

## Jak otevřít soubor CUBE?

Soubor CUBE lze otevřít a odkazovat pomocí následujících programů.

- **NWChem** (zdarma) pro (Windows, MAC, Linux)

## Reference
* [Formát souboru Gaussian Cube](https://paulbourke.net/dataformats/cube/)
