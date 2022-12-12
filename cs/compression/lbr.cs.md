{
  "date" : "2021-04-08",
  "keywords" :[ "soubor mst", "formát souboru mst", "co je soubor mst", "soubor", "příklad mst", "přípona souboru mst", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
	

},
  "draft" : "false",
  "toc" : true,
  "title" :"LBR - Formát souboru archivu knihovny LU",
  "description":"Další informace o formátu souborů LBR a rozhraních API, která mohou vytvářet a otevírat soubory LBR.",
  "linktitle" : "LBR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Co je soubor LBR?

Soubor s příponou .lbr je archivní soubor vytvořený programem LU a používaný v operačních systémech CP/M a DOS během 80. let. Již se nepoužívá a byl nahrazen moderními archivačními formáty souborů. Formát nekomprimuje členské soubory a funguje jako kontejnerový archiv pro ně. Funkce archivace byla většinou používána pro přenos archivovaných souborů přes internet. Protože LBR nenabízel kompresi, byly ke komprimaci členských souborů před archivací nebo výsledného archivního souboru po archivaci použity další nástroje, jako je SQ nebo CRUNCH, aby se zmenšila jeho velikost.

## Formát souboru LBR

Formát souboru LBR navrhl Gary P. Novosielski a nemá veřejně dostupné žádné technické podrobnosti. Soubory LBR začínají bajtem 0x00, následuje 11 mezer (0x20), pak dva bajty 0x00 a potom dva bajty, které nejsou oba 0x00. Vzhledem k tomu, že jde o formát souboru kontejneru, lze jej extrahovat pomocí LU.COM a NULU.COM.

## Reference

* [LBR – Wikipedie](https://en.wikipedia.org/wiki/LBR_(formát_souboru))

