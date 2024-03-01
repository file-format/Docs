
{
  "date": "2021-12-14",
  "keywords": [
".abc-tiedosto",
"laajennus",
"muoto",
"ActionScript-tavukooditiedosto",
"kuinka avata .abc-tiedosto",
"abc-tiedostomuoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ABC - ActionScript-tavukooditiedosto",
  "description": "Opi ABC-tiedostomuodosta esimerkkien ja sovellusliittymien avulla, jotka voivat luoda ja avata ABC-tiedostoja.",
  "linktitle": "ABC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ab-fic"
}
},
  "lastmod": "2021-12-14"
}

## Mikä on ABC-tiedosto?

Tiedosto, jonka tunniste on .abc, on ActionScript-tavukooditiedosto, jonka Flash-kääntäjä on luonut ActionScript-komentosarjatiedostojen kääntämisen tuloksena. ActionScript-virtuaalikone (AVM ja AVM2) suorittaa ABC-tiedoston sisältämän tavukoodin. Tavukoodi koostuu vakiodatasta, AVM2-käskyjoukon käskyistä ja erilaisista metatiedoista. Kun ABC-tiedosto ladataan AVM- tai AVM2-laitteeseen, se tarkistetaan. Jos se ei ole AVM2:n yleiskatsauksen mukainen, se hylätään. ABC-tiedostot voidaan avata Adobe Flash Playerissa, joka on lopetettu kauan sitten.

## ABC-tiedostomuoto – lisätietoja

ABC-tiedostot tallennetaan levylle binääritiedostomuodossa, joita AVM- tai AVM2-virtuaalikoneet voivat lukea. Sen sisäinen tiedostorakenne edustaa suoritettavaa koodilohkoa, jossa on kaikki vakiotiedot, tyyppikuvaajat, koodi ja metatiedot.

## ABC-tiedostorakenne

ABC-tiedostorakenne on alla olevan kuvan mukainen.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### ABC-tiedostokentät

|Kentän nimi|Kuvaus|
---|---|
|minor_version, major_version|Maaor_version- ja minor_version-arvot ovat abcFile-muodon pää- ja sivuversionumerot.|
|constant_pool|Constant_pool on muuttuvapituinen rakenne, joka koostuu kokonaisluvuista, kaksoisluvuista, merkkijonoista, nimiavaruuksista, nimiavaruusjoukoista ja moninimistä.|
|method_count, method|Method_count-arvo on menetelmätaulukon merkintöjen määrä. Jokainen menetelmätaulukon merkintä on muuttuvapituinen method_info-rakenne.|
|metadata_count, metadata|Metadata_count-arvon arvo on metatietotaulukon merkintöjen määrä. Jokainen metatietomerkintä on metadata_info-rakenne, joka yhdistää nimen merkkijonoarvojen joukkoon. |
|class_count, instance, class|Luokan_määrän arvo on instanssi- ja luokkataulukoiden merkintöjen määrä. |
|script_count, script|Skriptin_määrän arvo on komentosarjataulukon merkintöjen määrä. Jokainen komentosarjamerkintä on script_info-rakenne, joka määrittää tämän tiedoston yksittäisen skriptin ominaisuudet. |
|method_body_count, method_body|Method_body_count-arvo on merkintöjen määrä method_body-taulukossa. Jokainen method_bodyentry koostuu muuttuvapituisesta method_body_info -rakenteesta, joka sisältää ohjeet yksittäiselle menetelmälle tai funktiolle.|

## Viitteet

 * [Vahva ABC (ActionScript Bytecode) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

