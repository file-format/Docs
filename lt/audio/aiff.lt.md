{
  "date": "2021-04-26",
  "keywords": [
"aiff",
"failą",
"pratęsimas",
"formatu",
"garso mainų failo formatas",
"muzika",
"aiff failo formatas",
"aiff į mp3",
"aiff vs wav",
"Konvertuoti aiff į mp3"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie AIFF failo formatą ir API, kurios gali kurti, konvertuoti ir atidaryti AIFF failus.",
  "title": "AIFF – garso mainų failo formatas",
  "linktitle": "AIFF",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-aif-ltf"
}
},
  "lastmod": "2021-04-26"
}

## Kas yra AIFF failas?
AIFF (Audio Interchange File Format) yra nesuspausto garso failo formatas, kurį Apple sukūrė 1998 m., tačiau jis pagrįstas **EA IFF 85** (Electronic Arts sukurtas mainų formato failų standartas), įvyniojimo formatu, naudojamu Amiga sistemose. . Šiame failo formate yra atrinktų garsų saugojimo standartas. Formatas yra pakankamai lankstus ir leidžia saugoti monofoninius arba daugiakanalius atrinktus garsus įvairiais atrankos dažniais ir pločiais. Kadangi AIFF failai yra nesuspausti, dėl to jie yra didesni nei kiti nuostolingi formatai, pvz., [MP3](/audio/mp3/).

AIFF failus sudaro 2 nesuspausto stereo garso kanalai, kurių imties dydis yra 16 bitų, įrašytas 44,1 khz dažniu. Dėl aukštos garso kokybės 5 minučių garso įrašas gali užimti iki 50 MB vietos diske, o tai panašu į [WAV](/audio/wav/) failo formatą.

## AIFF prieš WAV

AIFF ir WAV kokybės požiūriu yra beveik vienodi. Abu jie naudoja tą patį PCM (impulsinio kodo moduliacijos) kodavimą, todėl jie yra didesni, palyginti su kitais nuostolingais formatais, tokiais kaip [MP3](/audio/mp3/), [M4A](/audio/m4a/). Kai kurie bendrieji skirtumai pateikti toliau esančioje lentelėje:

|AIFF|WAV|
---|---|
|Dažniausiai naudojamas MAC|Dažniausiai naudojamas asmeniniams kompiuteriams|
|Leidžia metadeta| Neleidžia metadeta|

## AIFF failo struktūra

**EA IFF 85** nustato bendrą duomenų saugojimo failuose struktūrą. **EA IFF 85** failą sudaro daugybė duomenų dalių. AIFF failo bloką sudaro tam tikra antraštės informacija, po kurios seka duomenys:
{{< figure src="../chunk.png" alt="AIFF dalis" >}}

AIFF failas yra kelių skirtingų tipų gabalų rinkinys. Yra du bendrieji gabalų tipai, kurie yra svarbūs formuojant AIFF failo dalį:
- **Common Chunk**: yra svarbių parametrų, apibūdinančių atrinktą garsą, pvz., jo ilgis ir atrankos dažnis.
- **Garso duomenų dalis**: yra tikrieji garso pavyzdžiai.
Yra daug kitų pasirenkamų dalių, kuriose pateikiami instrumento parametrai, apibrėžiami žymekliai, saugoma konkrečios programos informacija ir kt.

### Vietiniai gabalų tipai

AIFF formavimo gabalų tipai pateikti toliau esančioje lentelėje:

|Grupo tipas| Aprašymas|
---|---|
|Common Chunk|Common Chunk aprašo pagrindinius atrinkto garso parametrus|
|Garso duomenų dalis|Garso duomenų gabale yra tikrieji pavyzdiniai kadrai|
|Marker Chunk|Žymeklio skiltyje yra žymekliai, kurie nurodo garso duomenų pozicijas|
|Instrument Chunk|Instrument Chunk apibrėžia pagrindinius parametrus, kuriuos instrumentas, pvz., mėginių ėmiklis, gali naudoti garso duomenims atkurti|
|MIDI Data Chunk|MIDI Data Chunk gali būti naudojamas MIDI duomenims saugoti|
|Garso įrašymo dalis|Garso įrašymo dalyje yra informacijos, susijusios su garso įrašymo įrenginiais|
|Application Specific Cunk|Programų gamintojai gali naudoti konkrečias programos dalis bet kokiais tikslais|
|Komentarų dalis|Komentarų dalis naudojama komentarams saugoti FORM AIFF|
|Teksto dalys – vardas, autorius, autorių teisės, anotacija| Visi yra teksto gabalai|

## Nuorodos Nr.

* [Garso mainų failo formatas – pagal Vikipediją](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)


