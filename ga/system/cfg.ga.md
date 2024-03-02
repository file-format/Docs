{
  "date": "2021-06-29",
  "keywords": [
"CFG",
"síneadh",
"comhad",
"formáid",
"córas",
"cumraíocht",
"socruithe",
"cláir",
"ríomhaire",
"iarratas"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CFG - Formáid Chomhaid",
  "description": "Foghlaim faoi fhormáid comhaid CFG agus APIanna ar féidir leo comhaid CFG a chruthú agus a oscailt.",
  "linktitle": "CFG",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-cf-gag"
}
},
  "lastmod": "2021-06-29"
}

## Cad is comhad CFG ann? ##

Is cineál comhaid socruithe é comhad le síneadh .cfg. Is cineál comhaid é a úsáidtear go coitianta agus a úsáidtear chun faisnéis a stóráil maidir le cumraíocht agus socruithe do chláir ríomhaire. Stóráiltear an chuid is mó de chomhaid CFG i bhformáid téacs agus níor cheart iad a oscailt de láimh, ina ionad sin, ba cheart iad a oscailt ag baint úsáide as eagarthóir téacs. Mar sin féin, tá cineálacha éagsúla comhad CFG ann, atá difriúil san fhormáid ina stóráiltear an fhaisnéis. Athraíonn na gnéithe a thairgeann comhaid CFG ó fheidhm go feidhmchlár. Cuireann roinnt feidhmchlár ríomhaire ar chumas na n-úsáideoirí comhréir a gcomhaid chumraíochta a mhodhnú nó a fhorbairt trí úsáid a bhaint as trasnaíochtaí grafacha, agus ní cheadaíonn cuid eile ach modhnuithe trí úsáid a bhaint as eagarthóir téacs. Tar éis na comhaid seo a mhodhnú, féadfaidh na húsáideoirí treoir a thabhairt don fheidhmchlár na comhaid seo a léamh arís agus na modhnuithe a chur i bhfeidhm ar an gcóras.


## Formáid Chomhaid CFG ##

CFG files are supported by various operating systems such as Unix and Unix-like operating systems, MS-DOS, macOS, Microsoft Windows, and IBM OS/2. Athraíonn an fhormáid a stóráiltear agus a úsáidtear na comhaid seo i ngach ceann de na córais oibriúcháin seo. Úsáideann formhór na gcóras agus stórálann siad na comhaid seo i bhformáid gnáth-théacs atá inléite ag an duine agus in eagar, agus stórálann cinn eile ann formáid níos casta, ag brath ar úsáid na gcomhad agus riachtanas an chórais oibriúcháin.

I gcórais oibriúcháin atá cosúil le Unix agus Unix, baintear úsáid as stíleanna éagsúla formáide don chuid is mó de chomhaid CFG do chomhaid CFG, áfach, is é an fhormáid is coitianta ná gnáth-théacs atá inléite go héasca, agus ceadaíonn beagnach gach formáid tuairimí a dhéanamh agus a chur in eagar. Is iad na síntí comhad is coitianta do chomhaid CFG sna córais oibriúcháin seo ná CNF, CONF, CF, agus INI.

I gcóras oibriúcháin MS-DOS ní raibh ach formáid comhaid cumraíochta amháin ar dtús, eadhon, gnáth-théacs, áfach, MS-DOS 6, a thug isteach formáid comhaid cumraíochta INI leis.

úsáideann macOS comhad cumraíochta stíl formáid liosta maoine caighdeánach.

I Microsoft Windows, bhí comhaid cumraíochta gnáth-théacs INI ina bhfoinse thábhachtach chun faisnéis a stóráil agus a chur in eagar, áfach, tugadh isteach córas bunachar sonraí nua i 1993, rud a d’fhág gur tháinig laghdú ar úsáid na gcomhad cumraíochta i Microsoft Windows tar éis 1993.


## Sampla CFG ##

Tá comhad CFG samplach le feiceáil thíos:

```
#########################
## Settings
##

genome_dir = ~/genome/hg18/

> reads_list1
fastq_100k_1_1.txt
fastq_100k_3_1.txt
<

> reads_list2
fastq_100k_1_2.txt
fastq_100k_3_2.txt
<

read_format = FASTQ
quality_format = phred-33
mapper = bowtie
annotations = all.gene.refFlat.txt
out_path = output
max_intron = 400000
max_multi_hit = 10

```

## Comhaid CFG eile

Seo cineálacha comhaid eile a úsáideann an síneadh comhad **.cfg**.

**Socruithe**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**cluiche**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**Córas & Misc**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

