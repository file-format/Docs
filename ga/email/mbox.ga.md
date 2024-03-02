{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MBOX - Comhad Bosca Poist Ríomhphost",
  "description": "Foghlaim faoi fhormáid comhaid MBOX agus APIanna ar féidir leo comhaid MBOX a chruthú agus a oscailt.",
  "linktitle": "MBOX",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-mbo-gax"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad MBOX ann?

Téarma cineálach is ea formáid comhaid MBox a léiríonn coimeádán chun teachtaireachtaí ríomhphoist a bhailiú. Stóráiltear na teachtaireachtaí laistigh den choimeádán mar aon lena gceangaltán. Déantar teachtaireachtaí ó fhillteán iomlán a shábháil i gcomhad bunachar sonraí amháin agus cuirtear teachtaireachtaí nua i gceangal le deireadh an chomhaid. Soláthraíonn go leor feidhmchlár agus API tacaíocht d’fhormáid comhaid MBox ar nós Apple Mail agus Mozilla Thunderbird.

## Formáid Chomhaid MBOX ##

The MBox file format remained non-standardized for quite long time until 2005 when the application/mbox  was standardized as [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Messages, in RFC 2822 format, are concatenated inside MBox file format one after another. Each message begins with a separator line that identifies the message sender, and also identifies the date and time at which the message was received by the final recipient (either the last-hop system in the transfer path, or the system which serves as the recipient's mailstore). Each message is typically terminated by an empty line. The end of the database is usually recognized by either the absence of any additional data, or by the presence of an explicit end-of-file marker.

## Teachtaireacht ó Chomhad MBox á léamh ##

Scanann léitheoir trí chomhad mbox ag lorg línte From_. Marcálann aon líne From_ tús teachtaireachta. Níor cheart don léitheoir iarracht leas a bhaint as an bhfíric go bhfuil gach líne From_ (thar éis tús an chomhaid) bán. Nuair a aimsíonn an léitheoir teachtaireacht, bainfidh sé seoltóir clúdaigh (truaillithe b’fhéidir) agus dáta seachadta as an líne From_. Léann sé ansin go dtí an chéad líne From_ eile nó deireadh comhaid, cibé acu is túisce. Scriosann sé an líne bhán deiridh agus scriosann sé na línte >From_ agus línte >>From_ agus mar sin de. Is é an toradh ná teachtaireacht RFC 822.

## Cúrsaí Ionchódaithe ##

Is féidir inneachar an chomhaid MBox a mheascadh go dochúlaithe nuair a bhíonn comhad Mbox mar cheangaltán i ríomhphost a fhaightear agus go ndéantar é a shábháil i gcomhad Mbox eile. Chun é seo a sheachaint, ní mór do chórais teachtaireachtaí bunachar sonraí mbox a ionchódú le hionchódú aistrithe neamhthrédhearcach (amhail BASE64 nó Inphriontáilte Athfhriotail) aon uair a aistrítear a leithéid de réad trí phrótacail teachtaireachtaí. Ba cheart go mbeadh feidhmitheoirí ullamh freisin chun sonraí mbox a ionchódú go háitiúil má fhaightear sonraí neamhchomhlíontacha.

## Tagairtí ##

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)

* [Mbox - Vicipéid](https://en.wikipedia.org/wiki/Mbox)


