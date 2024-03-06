{
  "date": "2019-10-11",
  "keywords": [
"potx fails",
"potx faila formāts",
"kas ir potx fails",
"failu",
"potx piemērs",
"potx faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "POTX — Microsoft PowerPoint prezentācijas veidne",
  "description": "Uzziniet par POTX faila formātu un API, kas var izveidot un atvērt POTX failus.",
  "linktitle": "POTX",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-pot-lvx"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir POTX fails?

Faili ar paplašinājumu .POTX ir Microsoft PowerPoint veidņu prezentācijas, kas izveidotas ar Microsoft PowerPoint 2007 un jaunākām versijām. Šis formāts tika izveidots, lai aizstātu [POT](/presentation/pot/) faila formātu, kura pamatā ir binārais faila formāts un ko atbalsta PowerPoint 97-2003. Ģenerētos failus var izmantot, lai izveidotu prezentācijas, kurām ir tāds pats izkārtojums un citi iestatījumi, kas jāpiemēro jauniem failiem. Šie iestatījumi var ietvert stilus, fonus, krāsu paleti, fontus un noklusējuma iestatījumus. Šādi faili tiek ģenerēti, lai izveidotu lietošanai gatavus veidņu failus oficiālai lietošanai.

## Īsa vēsture ##

Tas bija 2000. gada sākumā, kad Microsoft nolēma veikt izmaiņas, lai pielāgotos **Office Open XML** standartam. Dažādu veidu dokumenti saskaņā ar šo jauno standartu tika identificēti, to paplašinājumos pievienojot X, kur X ir XML. Līdz 2007. gadam šis jaunais faila formāts kļuva par Office 2007 daļu un tiek izmantots arī jaunajās Microsoft Office versijās. Jaunajam faila tipam ir pievienotas priekšrocības: mazi failu izmēri, mazākas bojājumu izmaiņas un labi formatētu attēlu attēlojums.

## Faila formāta specifikācijas ##

Faili, kas ģenerēti, izmantojot Office Open XML failu formātu, ir XML failu kolekcija kopā ar citiem failiem, kas nodrošina saites starp visiem veidojošajiem failiem. Šī kolekcija faktiski ir saspiests arhīvs, ko var izvilkt, lai skatītu tās saturu. Lai to izdarītu, vienkārši pārdēvējiet POTX faila paplašinājumu ar zip un izņemiet to, lai novērotu tā saturu.

Turpmākajās sadaļās ir sniegta neliela informācija par katru no tiem.

### [Satura_veidi].xml ###

Šis ir vienīgais fails, kas tiek atrasts bāzes līmenī, kad tiek izvilkts zip. Tajā ir norādīti pakotnes daļu satura veidi. Visas atsauces uz pakotnē iekļautajiem XML failiem ir norādītas šajā XML failā. Tālāk ir norādīts slaida daļas satura veids:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Ja pakotnei ir jāpievieno jaunas daļas, to var izdarīt, pievienojot jauno daļu un atjauninot visas attiecības .rels failos. Jāpatur prātā, ka, lai veiktu šādas izmaiņas, ir jāatjaunina arī Content_Types.xml.

### \_rels (mape) ###

Attiecības starp pārējām daļām un resursiem ārpus paketes uztur attiecību daļa. Mapē Relācijas ir viens XML fails, kurā tiek saglabātas pakotnes līmeņa attiecības. Saites uz galvenajām PPTX failu daļām ir ietvertas šajā failā kā URI. Šie URI identificē katras galvenās daļas attiecību veidu ar pakotni. Tas ietver saistību ar primāro biroja dokumentu, kas atrodas kā ppt/presentation.xml, un citām docProps daļām kā pamata un paplašinātos rekvizītus.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Katrai dokumenta daļai, kas ir vienas vai vairāku attiecību avots, būs sava attiecību daļa, kur katra šāda attiecību daļa atrodas daļas apakšmapē \_rels un tiek nosaukta, pievienojot '.rels' faila nosaukumam. daļa. Galvenajai satura daļai (presentation.xml) ir sava attiecību daļa (presentation.xml.rels). Tajā ir ietvertas attiecības ar citām satura daļām, piemēram, slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, kā arī ārējo saišu URI.

#### Skaidras attiecības ####

Skaidrām attiecībām uz resursu tiek norādīta atsauce, izmantojot a atribūtu Id<Relationship> elements. Tas nozīmē, ka Id avotā tiek kartēts tieši uz relācijas vienuma ID ar skaidru atsauci uz mērķi.

Piemēram, slaidā var būt šāda hipersaite:
```
<a:hlinkClick r:id#"rId2">
```
R:id#rId2 norāda uz tālāk norādītajām attiecībām slaida attiecību daļā (slide1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Netiešas attiecības ####

Netiešām attiecībām šādas tiešas atsauces uz ` nav<Relationship> Id`. Tā vietā atsauce tiek saprasta.

### ppt mape ###

Šī ir galvenā mape, kurā ir visa informācija par prezentācijas saturu. Pēc noklusējuma tai ir šādas mapes:

* \_rels

* tēma

* slaidi

* slideLayouts

* slideMasters


un šādi xml faili:

* prezentācija.xml

* presProps.xml

* tableStyles.xml

* viewProps.xml


## Atsauces Nr.

* [[MS-PPTX] — PPTX faila formāts](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)


