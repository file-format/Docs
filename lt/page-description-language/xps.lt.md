{
  "date": "2019-10-11",
  "keywords": [
"XPS",
"XML popieriaus specifikacijos",
"Failas",
"Pratęsimas",
"Dokumento formatas",
"EMF",
"PDF"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XPS – puslapio maketo failo formatas",
  "description": "Sužinokite apie XPS failo formatą ir API, kurios gali kurti ir atidaryti XPS failus.",
  "linktitle": "XPS",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-xp-lts"
}
},
  "lastmod": "2021-04-23"
}

## Kas yra XPS failas?

XPS failas yra puslapio išdėstymo failai, pagrįsti Microsoft sukurtomis XML popieriaus specifikacijomis. Jis buvo sukurtas kaip EMF failo formato pakaitalas ir yra panašus į [PDF](/pdf/) failo formatą, bet naudoja XML dokumento išdėstymui, išvaizdai ir spausdinimo informacijai. Tiesą sakant, labiau pagrįsta teigti, kad XPS yra PDF bandymas, tačiau dėl daugelio priežasčių nepavyko gauti pakankamai populiarumo, nes priklauso PDF. Microsoft pagal numatytuosius nustatymus teikia XPS Document Writer nuo Windows 7, kad būtų galima kurti XPS failus. XPS failus galima sugeneruoti pasirinkus Microsoft XPS Document Writer kaip spausdintuvą spausdinant dokumentą.

XPS peržiūros priemonės yra integruotos kaip Windows Vista, Windows 7, Windows 8 ir Internet Explorer 6 ar naujesnės versijos dalis. Sugeneruoti XPS failai tampa tik skaitomi. Tai padidina vartotojo pasitikėjimą gautais dokumentais, siunčiamais kaip XPS, dėl dokumento autentiškumo. XPS dokumente gali būti vienas ar daugiau puslapių, konvertuotų iš originalaus dokumento.

## Trumpa istorija ##

Microsoft pateikė XPS specifikaciją Ecma International. 2007 m. birželio mėn. buvo įkurtas Ecma Technical Committee 46 (TC46), kuris sukūrė standartą, pagrįstą OpenXPS popieriaus specifikacijomis. Ecma International patvirtino Ecma standartą (ECMA-388) [XPS specifications](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/) 2009 m. birželio mėn. 97-ojoje Generalinėje asamblėjoje.

## XPS failo formatas ##

XPS formatą sudaro XML žymėjimas, kuris apibrėžia dokumento sudėtį ir kiekvieno puslapio vizualinę išvaizdą bei dokumento rodymo ar spausdinimo atvaizdavimo taisykles. Ji išsaugo visą informaciją, kad būtų galima iš naujo sukurti dokumentą bet kurioje sistemoje, todėl jis nepriklauso nuo toje sistemoje turimų išteklių. Formatas iš esmės yra ZIP archyvas ir jei pervadinsite failo plėtinį į ZIP, pamatysite failus, kuriuose yra dokumento duomenų. Šie dokumentai apima:

* dokumento puslapio failai (.fpage) – yra dokumento turinio ir dokumento formato nustatymai. Kiekviename XPS dokumento puslapyje yra vienas FPAGE failas.

* Dokumento nustatymų failas (.fdoc) – saugo parametrus, įtrauktus į XPS archyvą.

* dokumento fragmentų failai (.frag) – apibrėžia tikrojo XPS failo nustatymus ir kiekvienas dokumento puslapis turi savo .frag failą.


{{< figure src="../XPS-1.png" alt="XPS failo formatas" >}}

Šiuose failuose dokumento turinys išsaugomas taip, kad jei, pavyzdžiui, kas nors savo kompiuteryje neįdiegė tų pačių šriftų, XPS peržiūros priemonė vis tiek pateiks tuos originalius šriftus. Tai reiškia, kad XML žymėjimo failas turi būti įtrauktas į kiekvieną:

* Puslapis

* Tekstas

* Įterptieji šriftai

* Rastriniai vaizdai

* 2D vektorinė grafika

* Skaitmeninių teisių valdymas


XPS dokumento formatas apima tiksliai apibrėžtą dalių ir ryšių rinkinį, kurių kiekviena atlieka tam tikrą dokumento paskirtį. Formatas taip pat išplečia paketo funkcijas, įskaitant skaitmeninius parašus, miniatiūras ir įterpimą.

Įprastas XPS dokumentas atrodo taip ir gali būti analizuojamas atsižvelgiant į XPS failo formatą [specifications](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard.pdf).

{{< figure src="../XPS-2.png" alt="XPS failo formatas" >}}


## Nuorodos Nr.

* [XPS failo formato specifikacijos](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/)

* [XPS – Vikipedija](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)


