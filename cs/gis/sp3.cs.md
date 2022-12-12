{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SP3 - soubor NGS SP3",
  "description":"Další informace o formátu souboru SP3 a rozhraních API, která mohou vytvářet a otevírat soubory SP3.",
  "linktitle" : "SP3",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## Co je soubor SP3?

Soubor s příponou .sp3 je orbitální formát National Geodetic Survey (NGS) pro ukládání orbitálních informací. Jedná se o rozšíření formátů SP1 a SP2 od NGS a zahrnuje informace o korekci satelitního času, které se vypočítávají současně s oběžnámi dráhami. Primárně je založen na poloze a hodinách a nezahrnuje rychlosti. Formát byl navržen v Remondi v roce 1989 a byl přijat v roce 1991. Kromě informací o opravách satelitních hodin obsahuje informace, jako jsou exponenty přesnosti oběžné dráhy, komentáře, týden GPS a sekundy týdne spojené s první epochou. Soubory SP3 lze otevřít pomocí Wolfram Research Mathematica.

## Formát souboru SP3 – Další informace

Soubory SP3 se ukládají na disk ve formátu souboru ASCII a jeho obsah lze otevřít v libovolném textovém editoru pro prohlížení. Struktura souboru SP3 je patrná z následujícího obrázku.

{{< figure src="../sp3-file-format.png" title="" >}}

## Reference

* [The Extended Standard Product 3 Orbit Format (SP3-c)](http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20similar ,%20více%20flexibilní%20záhlaví%20struktura)
* [Rozšíření standardních formátů oběžné dráhy GPS National Geodetic Survey](https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)

