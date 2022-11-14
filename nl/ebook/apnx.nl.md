{
  "date" : "2021-03-11",
  "keywords" :[ "APNX", "Amazon Paginanummer Index", "extensie", "bestand", "format", "eBook", "Amazon Kindle"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over Amazon APNX-bestandsindeling en API's die APNX-bestanden kunnen maken en openen.",
  "title" :"APNX - Amazon-paginanummerindex",
  "linktitle" : "APNX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## Wat is een APNX-bestand? ##

Het Amazon Page Number Index-bestand dat de .apnx-extensie gebruikt, is een eBook-bestandstype; gebruikt door Amazon Kindle. Deze bestanden zijn eigenlijk bekend als pagineringsbestanden die worden gebruikt door Kindle-apparaten. Dus de APNX-bestanden worden meestal gemaakt om de pagina's van Kindle eBooks te markeren. De pagineringsfunctie is gestart op Amazon Kindle-apparaten sinds de 3.1-firmware. Het zoekt in het APNX-bestand naar pagina-indexen en wijst het vervolgens toe aan de paginanummers in het originele gedrukte boek. Deze bestanden worden samen met Amazon eBooks-bestanden op Kindle-apparaten opgeslagen. U kunt de APNX-bestanden niet openen of bewerken.

## Specificaties APNX-bestandsindeling ##

### Lay-out

|bytes| inhoud| opmerkingen|
---|---|---|
|4 |00010001 | Formaat-ID. Waarde van 65537 little-endian.|
|4 |begin volgende | De offset na de eindlocatie van de eerste kop. Start een nieuwe reeks koptekstinfo|
|4 |lengte| Lengte van eerste kop|
|N |eerste kop | Tekenreeks met inhoudsheader. Het begint de volgende reeks|
|2 |onbekend | Altijd 1|
|2 |lengte | Lengte van tweede kop|
|2 |paginatelling | Totaal aantal bytes na de tweede kop die pagina's vertegenwoordigen. Dit totaal omvat bytes die worden genegeerd door de pageMap.|
|2 |onbekend | Altijd 32|
|N |tweede kop | Tekenreeks die de koptekst voor paginatoewijzing bevat|
|4*N |vulling | Het eerste getal in de koptekst van de paginatoewijzing geeft het aantal 0 bytes aan.|
|4*N |pagina lijst ||

### Inhoudskop

De inhoudsheader bestaat uit een tekenreeks tussen {} die sleutel-, waardeparen bevat:

|inhoud| opmerkingen|
---|---|
|contentGuid| Gids.|
|asin | Amazon-ID voor de Kindle-versie van het boek.|
|cdeType | MOBI cdeType. Moet altijd EBOK zijn voor e-boeken.|
|fileRevisionId | Revisie van dit bestand.|

#### Voorbeeld
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### Koptekst voor paginatoewijzing
De koptekst van de paginatoewijzing bestaat uit een tekenreeks tussen {} die sleutel-waardeparen bevat.

|inhoud | opmerkingen|
---|---|
|asin | Het ISBN 10 voor het papieren boek waarmee de pagina's overeenkomen|
|pageMap| Drie waarde tupel. Ziet eruit als: "(N,N,N)\
1) Aantal bytes na kop waarmee de paginanummeringsreeks begint\
2) onbekend\
3) onbekend\|
#### Voorbeeld
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Paginalijst

De paginalijst is een reeks verschuivingen in de onbewerkte HTML. Elk
waarde is het begin van een nieuwe pagina. Elke invoer is een big endian van 4 bytes
int.



## Referenties

* [Amazon APNX-bestandsindeling](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)
* [APNX - door MobileRead Wiki](https://wiki.mobileread.com/wiki/APNX)

