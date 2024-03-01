{
  "date": "2023-03-01",
  "keywords": [
"sirutiedosto",
"mikä on sirutiedosto",
"tiedosto",
"kuinka avata sirutiedosto",
"chip tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CHIP-tiedostomuoto - Microarray-merkintätiedosto",
  "description": "Opi CHIP-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CHIP-tiedostoja.",
  "linktitle": "CHIP",
  "menu": {
    "docs": {
      "identifier": "spreadsheet-chip-fi",
      "parent": "spreadsheet"
}
},
  "lastmod": "2023-03-01"
}

## Mikä on CHIP-tiedosto?

CHIP-tiedosto on microarray-merkintätiedosto ja liittyy Gene Set Enrichment Analysis (GSEA) -ohjelmistoon. GSEA on laskennallinen menetelmä, joka arvioi, näyttääkö ennalta määritellyssä geenijoukossa (geenisarjassa) tilastollisesti merkittäviä eroja kahden biologisen tilan välillä, kuten terve ja sairas kudos tai lääkkeellä hoidetut ja käsittelemättömät solut. GSEA:n suorittamiseksi tarvitset geeniekspressiotietojoukon ja geenisarjatietokannan. Geenisarjatietokanta sisältää tietoa geenisarjojen geeneistä, kuten niiden toiminnasta, reitistä tai kudosspesifisestä ilmentymisestä.

A CHIP file is a specific type of gene set database that is used by GSEA. It contains information about the genes and gene sets that are relevant to the microarray platform being used in the experiment. The CHIP file provides annotations for each probe on the microarray, such as the gene symbol, gene name, gene description, and chromosomal location. This information is used to match the probes with the genes in the gene expression dataset and to assign them to the appropriate gene sets for GSEA analysis.

Jos haluat käyttää CHIP-tiedostoa GSEA:ssa, sinun on tuotava se ohjelmistoon ja linkitettävä se microarray-tietojoukkoon. GSEA tukee erilaisia microarray-alustoja ja tarjoaa valmiita CHIP-tiedostoja monille niistä. Voit kuitenkin myös luoda oman CHIP-tiedoston käyttämällä merkintätietokantoja ulkoisista lähteistä, kuten NCBI tai Ensembl.

## Lisää tietoa

CHIP-tiedosto ei ole laskentataulukko, mutta se voidaan avata ja muokata taulukkolaskentaohjelmassa, kuten Microsoft Excel tai Google Sheets. CHIP-tiedosto on sarkaineroteltua dataa sisältävä tekstitiedosto, joka voidaan helposti tuoda taulukkolaskentaohjelmaan tarkastelua ja muokkausta varten.

Taulukkolaskentaohjelmassa voit muokata CHIP-tiedoston tietoja lisätäksesi, poistaaksesi tai muokataksesi merkintöjä geeneille ja geenijoukoille microarrayssa. Voit esimerkiksi käyttää taulukkolaskentaohjelmaa lisätäksesi mukautettuja merkintöjä geeneille, jotka eivät sisälly alkuperäiseen CHIP-tiedostoon, tai yhdistää useita CHIP-tiedostoja eri lähteistä yhdeksi tiedostoksi.

On kuitenkin tärkeää huomata, että CHIP-tiedostolla on tietty muoto ja rakenne, jotka on säilytettävä, jotta ne ovat yhteensopivia GSEA-ohjelmiston kanssa. Jos muokkaat CHIP-tiedoston sisältöä taulukkolaskentaohjelmassa, varmista, että muutokset eivät muuta tiedostomuotoa tai sisältöä tavalla, joka voisi vaikuttaa GSEA-analyysin tarkkuuteen tai kelpoisuuteen.

## Kuinka avata CHIP-tiedosto?

Koska CHIP-tiedosto sisältää sarkaimilla eroteltuja tietoja, joten jos haluat tarkastella laskentataulukon tietoja, voit avata sen Microsoft Excelissä.

## Viitteet
* [GSEA](https://en.wikipedia.org/wiki/Gene_set_enrichment_analysis)
