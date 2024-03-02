{
  "date": "2019-10-11",
  "keywords": [
".mel",
"Maya teanga leabaithe",
"comhad",
"síneadh",
"formáid comhaid",
"Cluiche Maya 3D",
"Treoir Ríomhchlárúcháin"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MEL - Maya Formáid Chomhaid Teanga Leabaithe",
  "description": "Foghlaim faoi fhormáid comhaid MEL agus APIanna ar féidir leo comhaid MEL a chruthú agus a oscailt.",
  "linktitle": "MEL",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-me-gal"
}
},
  "lastmod": "2021-03-08"
}

## Cad is comhad MEL ann?

Is teanga scriptithe é comhad le síneadh .mel (Teanga Leabaithe Maya) a úsáideann Autodesk Maya chun comhéadain ghrafacha a chruthú. Ligeann sé duit cruthú eilimintí grafacha a uathoibriú ag baint úsáide as scripteanna inrite i dteannta le comhéadan grafach Maya. Cuireann MEL ar do chumas comhéadain ghrafacha a chruthú gan ríomhchlárú a fhoghlaim. Baintear é seo amach trí Macraí agus gníomhartha saincheaptha a chruthú a luasaíonn tascanna athchleachtacha. Ligeann na nósanna imeachta agus na scripteanna seo duit samhaltú saincheaptha, beochan, dinimic agus rindreáil tascanna a chruthú. Is féidir Autodesk Maya 2020 a úsáid chun inneachar comhaid EML a oscailt agus a fheiceáil.

## Formáid Chomhaid MEL - Tuilleadh Eolais

Tá [reference manual](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) ríomhchláraitheoir ar fáil d'fhorbróirí ar rannán doiciméadaithe Maya. Tá MEL bunaithe ar orduithe scriptithe sliogán, cosúil le UINX, chun rudaí a bhaint amach. De bharr na n-orduithe atá bunaithe ar scripteanna ní bhaineann sé le ríomhchlárú traidisiúnta agus atá dírithe ar oibiachtaí (OOP), rud a fhágann nach n-úsáidtear struchtúir sonraí, ag glaoch feidhmeanna, nó ag baint úsáide as OOP mar atá i dteangacha eile.

Seo a leanas roinnt de na príomhphointí faoi MEL.

`Tuairimí` - Ní mór deireadh a chur le gach ráiteas i MEL le leathstad (;), fiú ag deireadh bloc.

`Luachanna Filleadh` - Má luaitear slonn a thugann luach ar ais, ní phriontálann sé an luach i MEL go huathoibríoch. Ina áit sin is cúis le hearráid é.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`Orduithe Cruthaithe, Eagar agus Scrios` - Úsáidtear an t-ordú céanna chun rudaí a chruthú, rudaí a chur in eagar nó chun faisnéis a cheistiú faoi rudaí atá ann cheana féin. Mar sin féin, rialaíonn bratach cad a dhéanann an t-ordú (cruthaigh, cuir in eagar nó cuir ceist).

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`Luach ar ais ó Fheidhm` - Tugann comhréir feidhme luach ar ais go huathoibríoch. Chun luach aischuir a fháil ag baint úsáide as comhréir ordaithe, ní mór duit an t-ordú a chur faoi iamh i gcúlquotes.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## Tagairtí

 * [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

