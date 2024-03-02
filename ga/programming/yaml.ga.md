{
  "date": "2019-10-11",
  "keywords": [
"yaml",
".yaml",
"cad is comhad yaml ann",
"Conas comhad yaml a oscailt",
"síneadh",
"comhad",
"comhad yaml",
"formáid comhaid yaml",
"síneadh .yaml",
"yaml vs json",
"Sampla comhad YAML",
"sampla comhad docker yaml"
],
  "author": {
    "display_name": "Muhammad Ahmad Chishti"
},
  "draft": "false",
  "toc": true,
  "description": " Foghlaim faoi fhormáid comhaid YAML agus APIs ar féidir leo comhad YAML a chruthú agus a oscailt.",
  "title": "Formáid Chomhaid YAML",
  "linktitle": "YAML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-yam-gal"
}
},
  "lastmod": "2021-05-05"
}

## Cad is comhad YAML ann? ##

Tá **comhad YAML** comhdhéanta de theanga YAML (Ní Teanga Mharcála í YAML) ar teanga í atá bunaithe ar Unicode le sraithiú sonraí; a úsáidtear le haghaidh comhaid cumraíochta, teachtaireachtaí idirlín, marthanacht réad, srl. Úsáideann YAML an síneadh .yaml dá chomhaid. Tá a chomhréir neamhspleách ar theanga ríomhchlárúcháin ar leith. Go bunúsach, tá an YAML deartha le haghaidh idirghníomhú daonna agus chun oibriú go maith le teangacha ríomhchlárúcháin nua-aimseartha. Mhéadaigh tacaíocht do shraithiú struchtúir sonraí dúchasacha treallach inléiteacht na gcomhad YAML, ach tá an próiseas parsála agus giniúna comhad beagán casta dá bharr.

## Stair Ghearr ##

Moladh YAML den chéad uair in 2001 agus d’fhorbair Clark Evans, Ingy döt Net, agus Oren Ben-Kiki é. Dúradh ar dtús go gciallaíonn YAML Teanga Mharcála Eile fós” chun a chuspóir mar theanga mharcála a chur in iúl. Athchóiríodh níos déanaí é mar YAML Aint Markup Language chun a chuspóir a léiriú mar chuspóir atá dírithe ar shonraí.


## Formáid Chomhaid YAML ##

Tá comhad YAML comhdhéanta de na cineálacha sonraí seo a leanas

- **Scalars**: Is luachanna iad scálaí cosúil le Teaghráin, Slánuimhreacha, Booles, etc.
- **Seichimh**: Is liostaí iad seichimh ina bhfuil gach mír ag tosú le fleiscín (-). Is féidir liostaí a neadú freisin.
- **Mappings**: Tugann an léarscáilíocht an cumas eochracha a liostú le luachanna.

### Comhréir ###

- **Spás Bán**: Úsáidtear eangú spás bán chun neadú agus struchtúr iomlán a léiriú.

``` yaml
ainm: John Smith
déan teagmháil le:
baile: 1012355532
oifig: 5002586256
seoladh:
sráid: |
123 Alley Tornado
Suite 16
Cathair : East Centerville
stát: KS
```

- **Tuairimí**: Scríobhtar tuairimí ag tosú leis an tsiombail #.

``` yaml
# Seo Trácht YAML
```

- **Liostaí**: Úsáidtear fleiscín (-) chun baill an liosta a chur in iúl agus gach ball ar líne ar leith. Is féidir baill an liosta a chur faoi iamh freisin idir lúibíní cearnacha ([...]) agus baill scartha le camóga (,).

``` yaml
  - "A"
  - "b"
  - "c"
```

``` yaml
[A, B, C]
```

- **Eagar Comhthiomsaitheach**: Tá eagar comhthiomsaitheach timpeallaithe ag lúibíní cuartha ({...}). Tá idirstad(:) scartha idir na heochracha agus na luachanna agus tá camóg (,) scartha ag gach péire.

``` yaml
{ainm: John Smith, aois: 20}
```

- **Teaghráin**: Is féidir teaghrán a scríobh le nó gan Sleachta dúbailte (”) nó Sleachta singil (').

``` yaml
Teaghrán Samplach
"Teaghrán Samplach"
Teaghrán Samplach
```

- **Ábhar an Bhloic Scálaigh**: Is féidir ábhar scálach a scríobh i mblocnodaireacht trí úsáid a bhaint as an méid seo a leanas:
  - "********: Tá gach sos beo suntasach."
  - "**>**: Tá gach briseadh líne fillte go spás. Baineann sé amach an spás bán tosaigh do gach líne."

``` yaml
sonraí: |
YAML
(Ní Teanga Mharcála í YAML)
is teanga sraitheach sonraí
```

``` yaml
sonraí: ?
YAML (Ní Teanga Mharcála í YAML)
is teanga sraitheach sonraí
```

- **Cáipéisí Iolracha**: Déantar ildhoiciméad a dheighilt le trí thréithe (---) in aon sruth amháin. Léiríonn fleiscíní tús an doiciméid. Úsáidtear fleiscíní freisin chun treoracha a scaradh ó ábhar doiciméad. Léirítear deireadh an doiciméid le trí phonc (...).

``` yaml
  ---
Doiciméad 1
  ---
Doiciméad 2
...
```

- **Cineál**: Chun an cineál luacha a shonrú, úsáidtear marcanna dúbailte (!!).

``` yaml
a:!!snámh 123
b:!!str 123
```

- **Clib**: Chun clib a shannadh do nóta, úsáidtear ampersand (&) agus chun tagairt a dhéanamh don nód sin, úsáidtear réiltín (*).

``` yaml
ainm: John Smith
bille chuig: &id01
sráid: |
123 Alley Tornado
Suite 16
Cathair : East Centerville
stát: KS

long-chuig: * id01
```

- **Treoracha**: Is féidir treoracha i sruth a chur roimh dhoiciméid YAML. Tosaíonn treoracha le comhartha faoin gcéad (%) agus an t-ainm ina dhiaidh sin agus ansin na paraiméadair scartha le spásanna.

``` yaml
YAML 1.2
  ---
Ábhar an doiciméid
```
## Sampla comhad YAML
Anseo is féidir leat sampla ** docker yaml file** a fheiceáil thíos:

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML vs JSON
Go bunúsach, déantar JSON agus YAML a fhorbairt chun formáid idirmhalartaithe sonraí atá inléite ag an duine a sholáthar. Déantar an YAML a fhíorú mar shárthacar d'fhormáid JSON. Ciallaíonn sé gur féidir linn JSON a pharsáil ag baint úsáide as parsálaí YAML. Cé go bhfuil cur i bhfeidhm praiticiúil an teoiric seo beag tricky. Mar sin, tugtar roinnt bundifríochtaí idir YAML agus JSON thíos:

|YAML| JSON|
---|---|
|Próiseas casta agus am-íditheach chun sonraí sraitheacha a pharsáil |Parsáil go tapa agus go héasca sonraí sraitheach JSON lena dhearadh níos simplí|
|Níos lú tacaíochta pobail| Tacaíocht agus éileamh pobail níos mó|
|Tacaíonn sé le tuairimí| Ní thacaíonn sé le tuairimí|
|Cumas tagairt do réada sonraí eile a úsáid| Dodhéanta struchtúir chasta a shraithiú le tagairtí réad |
|Déantar ordlathas a úsáid le carachtair spáis dhúbailte. Ní cheadaítear carachtair chluaisín|Tá Réada agus Eagar sainithe idir lúibíní agus lúibíní.|
|Tá comharthaí athfhriotail teaghrán roghnach ach tacaíonn sé le comharthaí athfhriotail singil agus dúbailte.|Caithfidh na teaghráin a bheith i Sleachta dúbailte.|
|Is féidir le nód fréimhe a bheith in aon cheann de na cineálacha sonraí bailí|Caithfidh nód fréamhaithe a bheith ina eagar nó ina réad.|


## Tagairtí ##

- [YAML - Wikipedia](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)

