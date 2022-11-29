{
  "date" : "2019-11-25",
  "keywords" :[ "jpeg-fil", "jpeg-filformat", "vad är en jpeg-fil", "fil", "jpeg-exempel", "jpeg-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPEG - Bildfilformat",
  "description":"Läs mer om JPEG-filformat och API:er som kan skapa och öppna JPEG-filer.",
  "linktitle" : "JPEG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-08"
}

## Vad är en JPEG-fil? ##

En JPEG är en typ av bildformat som sparas med metoden för förlustkomprimering. Utdatabilden, som ett resultat av komprimering, är en kompromiss mellan lagringsstorlek och bildkvalitet. Användare kan justera komprimeringsnivån för att uppnå önskad kvalitetsnivå samtidigt som lagringsstorleken minskas. Bildkvaliteten påverkas försumbart om 10:1-komprimering tillämpas på bilden. Ju högre komprimeringsvärde, desto högre försämring i bildkvalitet.

## Filformatspecifikationer ##

JPEG-bildfilformatet standardiserades av Joint Photographic Experts Group och därav namnet JPEG. Formatet har varit valet av att lagra och överföra fotografiska bilder på webben. Nästan alla operativsystem har nu tittare som stöder visualisering av JPEG-bilder, som ofta också lagras med JPG-tillägg. Även webbläsarna stöder visualisering av JPEG-bilder. Innan du går in i specifikationerna för JPEG-filformat måste den övergripande processen med steg som är involverade i JPEG-skapandet nämnas.

### JPEG-komprimeringssteg ###

**Transformation:** Färgbilder omvandlas från RGB till en luminans/krominansbild (ögat är känsligt för luminans, inte krominans, så den krominansdelen kan förlora mycket data och kan därför komprimeras mycket.

**Nedsampling:** Nedsamplingen görs för färgad komponent och inte för luminanskomponent. Nedsampling görs antingen i förhållandet 2:1 horisontellt och 1:1 vertikalt (2h 1 V). Således minskar bilden i storlek eftersom "y"-komponenten inte berörs, det finns ingen märkbar förlust av bildkvalitet.

**Ordna i grupper:** Pixlarna för varje färgkomponent är organiserade i grupper om 8×2 pixlar som kallas "dataenheter" om antalet rader eller kolumner inte är en multipel av 8, den nedre raden och kolumnerna längst till höger dupliceras.

**Diskret Cosine Transformation:** Discrete Cosine Transform (DCT) appliceras sedan på varje dataenhet för att skapa 8×8 karta över transformerade komponenter.DCT innebär en viss förlust av information på grund av datoraritmetikens begränsade precision. Detta innebär att även utan kartan kommer det att bli en viss förlust av bildkvalitet men den är normalt liten.

**Kvantisering:** Var och en av de 64 transformerade komponenterna i dataenheten delas med ett separat tal som kallas dess 'kvantiseringskoefficient (QC)' och avrundas sedan till ett heltal. Det är här information går förlorad oåterkalleligt, stora kvalitetskontroller orsakar mer förlust. I allmänhet tillåter de flesta JPEG-verktyg användning av QC-tabeller som rekommenderas av JPEG-standarden.

**Kodning:** De 64 kvantiserade transformerade koefficienterna (som nu är heltal) för varje dataenhet kodas med en kombination av RLE- och Huffman-kodning.

**Lägga till rubrik:** Det sista steget lägger till rubrik och alla använda JPEG-parametrar och matar ut resultatet.

JPEG-avkodaren använder stegen omvänt för att generera originalbilden från den komprimerade.

### Filstruktur ###

En JPEG-bild representeras som en sekvens av segment där varje segment börjar med en markör. Varje markör börjar med 0xFF byte följt av markörflagga för att representera typen av markör. Nyttolasten följt av markör är olika beroende på markörtyp. Vanliga JPEG-markörtyper är som listas nedan:

|Kort namn|Bytes|Nyttlast|Namn|Kommentarer
---|---|---|---|---|
|SOI|0xFF, 0xD8|ingen|Start av bild|
|S0F0|0xFF, 0xC0|variabel storlek|Början av bildruta|
|S0F2|0xFF, 0xC2|variabel storlek|Start för ram|
|DHT|0xFF, 0xC4|variabel storlek|Definiera Huffman-tabeller|
|DQT|0xFF, 0xDB|variabel storlek|Definiera kvantiseringstabell(er)|
|DRI|0xFF, 0xDD|4 byte|Definiera omstartsintervall|
|SOS|0xFF, 0xDA|variabel storlek|Start av skanning|
|RSTn|0xFF, 0xD//n//(/sv//n//#0..7)|ingen|Starta om|
|APPn|0xFF, 0xE//n//|variabel storlek|Applikationsspecifik|
|COM|0xFF, 0xFE|variabel storlek|Kommentar|
|EOI|0xFF, 0xD9|ingen|Slut på bild|

Inom den entropikodade datan, efter varje 0xFF-byte, infogas en 0x00-byte av kodaren före nästa byte, så att det inte verkar finnas en markör där ingen är avsedd, vilket förhindrar inramningsfel. Avkodare måste hoppa över denna 0x00 byte. Denna teknik, som kallas [byte stuffing](https://en.wikipedia.org/wiki/Byte_stuffing) (se JPEG-specifikationsavsnitt F.1.2.3), tillämpas endast på entropikodade data, inte på markördata för nyttolast . Observera dock att entropikodad data har några egna markörer; specifikt återställningsmarkörerna (0xD0 till 0xD7), som används för att isolera oberoende bitar av entropikodad data för att möjliggöra parallell avkodning, och kodare är fria att infoga dessa återställningsmarkörer med jämna mellanrum (även om inte alla kodare gör detta).

