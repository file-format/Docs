{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAZ - komprimovaný soubor výměny dat LIDAR",
  "description":"Další informace o formátu souborů LAZ a rozhraních API, která mohou vytvářet a otevírat soubory LAZ.",
  "linktitle" : "LAZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Co je soubor LAZ?

Formát souboru LAZ je komprimovaná verze formátu souboru LAS (Lidar LASer), který je speciálně navržen pro ukládání dat lidarového mračna bodů. Soubory LAZ si uchovávají stejná data a strukturu jako soubory LAS, ale využívají techniky bezztrátové komprese ke snížení velikosti souboru při zachování původní věrnosti dat.

## Formát souboru LAZ - Stručná historie

Formát souboru LAZ byl vyvinut, aby reagoval na rostoucí poptávku po efektivním ukládání a přenosu velkých datových sad lidar. Komprimací souborů LAS soubory LAZ výrazně zmenšují svou velikost, což usnadňuje jejich správu a přenos. Komprese je dosaženo použitím kombinace různých algoritmů, jako je entropické kódování a kódování s proměnnou délkou, pro reprezentaci lidarových bodových atributů v kompaktnější podobě.

## Formát souboru LAZ

I přes kompresi si soubory LAZ zachovávají schopnost plně obnovit původní data LAS bez jakékoli ztráty informací. To znamená, že jakmile je soubor LAZ dekomprimován, lze jej zpracovat a analyzovat stejným způsobem jako nekomprimovaný soubor LAS. Proces komprese a dekomprese se obvykle provádí pomocí specializovaného softwaru nebo knihoven, které podporují formát LAZ.

Formát souboru LAZ zachovává kompatibilitu se soubory LAS a zajišťuje interoperabilitu napříč softwarem lidar a nástroji pro zpracování. To znamená, že aplikace, které mohou číst a zpracovávat soubory LAS, mohou obvykle zpracovávat soubory LAZ bez jakýchkoli úprav. Kromě toho soubory LAZ stále obsahují záhlaví souboru, záznamy s proměnnou délkou (VLR) a záznamy bodových dat, přičemž zachovávají stejnou strukturu jako soubory LAS.

## Výhody formátu souborů LAZ

**Snížená velikost souboru:** Komprese LAZ výrazně snižuje velikost souborů datových sad lidar, takže je lze lépe spravovat a snáze se ukládají a přenášejí.

**Integrita dat:** Komprese LAZ je bezeztrátová, což znamená, že dekomprimovaná data jsou přesnou replikou původních dat LAS, což zajišťuje, že nedojde ke ztrátě informací nebo přesnosti.

**Interoperabilita:** Soubory LAZ jsou kompatibilní se soubory LAS, což umožňuje bezproblémovou integraci se stávajícím softwarem lidar a pracovními postupy.

**Efektivní zpracování:** Díky jejich zmenšené velikosti lze soubory LAZ načítat a zpracovávat rychleji, což zkracuje celkovou dobu zpracování a analýzy.

Formát souboru LAZ se stal široce přijatým v komunitě lidarů jako standard pro ukládání a výměnu komprimovaných dat lidaru. Nabízí rovnováhu mezi účinnou kompresí dat a integritou dat, což umožňuje snadnější manipulaci s velkými datovými soubory lidar při zachování přesnosti a kvality původních dat.

## Reference

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
