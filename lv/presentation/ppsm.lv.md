{
  "date": "2019-10-11",
  "keywords": [
"ppsm failu",
"ppsm faila formātā",
"kas ir ppsm fails",
"failu",
"ppsm piemērs",
"ppsm faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PPSM — PowerPoint prezentācijas fails ar iespējotu makro",
  "description": "Uzziniet par PPSM faila formātu un API, kas var izveidot un atvērt PPSM failus.",
  "linktitle": "PPSM",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-pps-lvm"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir PPSM fails?

Faili ar PPSM paplašinājumu ir ar makro iespējotu slaidrādes faila formātu, kas izveidots ar Microsoft PowerPoint 2007 vai jaunāku versiju. Vēl viens līdzīgs faila formāts ir [PPTM](/presentation/pptm/), kas atšķiras ar Microsoft PowerPoint atvēršanu rediģējamā formātā, nevis kā slaidrādi. Palaižot kā slaidrādi, PPSM fails parāda prezentācijas slaidus ar neskartu saturu slaidrādē un pēc noklusējuma ir tikai lasīšanas režīmā. PPSM failus joprojām var rediģēt programmā Microsoft PowerPoint, atverot to programmā PowerPoint.

## Faila formāts ##

PPSM faila formāts tika ieviests programmā PowerPoint 2007, un tā pamatā ir OpenXML faila formāts, kas satura glabāšanai izmanto XML un [ZIP](/compression/zip/) kombināciju. Faili, kas ģenerēti, izmantojot Office Open XML failu formātu, ir XML failu kolekcija kopā ar citiem failiem, kas nodrošina saites starp visiem veidojošajiem failiem. Šī kolekcija faktiski ir saspiests arhīvs, ko var izvilkt, lai skatītu tās saturu. Lai to izdarītu, vienkārši pārdēvējiet PPSM faila paplašinājumu ar zip un izņemiet to, lai novērotu tā saturu.

Turpmākajās sadaļās ir sniegta skaidrība par katru no tām.

### [Satura_veidi].xml ###

Šis ir vienīgais fails, kas tiek atrasts bāzes līmenī, kad tiek izvilkts zip. Tajā ir norādīti pakotnes daļu satura veidi. Visas atsauces uz pakotnē iekļautajiem XML failiem ir norādītas šajā XML failā. Tālāk ir norādīts slaida daļas satura tips.
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Ja pakotnei jāpievieno jaunas daļas, to var izdarīt, pievienojot jauno daļu un atjauninot visas attiecības .rels failos. Jāpatur prātā, ka, lai veiktu šādas izmaiņas, ir jāatjaunina arī Content_Types.xml.

### \_rels (mape) ###

Attiecības starp pārējām daļām un resursiem ārpus paketes uztur attiecību daļa. Mapē Relācijas ir viens XML fails, kurā tiek saglabātas pakotnes līmeņa attiecības. Saites uz prezentācijas failu galvenajām daļām ir ietvertas šajā failā kā URI. Šie URI identificē katras galvenās daļas attiecību veidu ar pakotni. Tas ietver saistību ar primāro biroja dokumentu, kas atrodas kā ppt/presentation.xml, un citām docProps daļām kā pamata un paplašinātos rekvizītus.
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
#### Netiešās attiecības ####

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

* [OpenXML prezentācijas faila formāts](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)


