{
  "date": "2020-11-11",
  "keywords": [
"DTSX",
"síneadh",
"comhad",
"formáid comhaid",
"Cineál Comhaid Bunachar Sonraí",
"Formáid Comhaid Bunachar Sonraí",
"Comhaid Bunachar Sonraí"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid DTSX agus APIanna ar féidir leo comhaid DTSX a chruthú agus a oscailt.",
  "title": "Formáid Chomhaid DTSX - Comhad Socruithe DTS Freastalaí SQL",
  "linktitle": "DTSX",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dts-gax"
}
},
  "lastmod": "2020-08-12"
}

## Cad is comhad DTSX ann?

Comhad le síneadh .dtsx (Pacáiste Seirbhísí Trasfhoirmithe Sonraí XML) is ea comhad Seirbhísí Trasfhoirmithe Sonraí (DTS) a úsáideann Microsoft SQL chun tagairt a dhéanamh do chéimeanna/rialacha aistrithe sonraí chun sonraí a aistriú ó bhunachar sonraí amháin go ceann eile. Áirítear leis sin na claochluithe agus aon chéimeanna próiseála roghnacha a d’fhéadfadh a bheith ag teastáil le linn an aistrithe sonraí idir na pointí tionscnaimh agus na cinn scríbe. Úsáideann SQL Server Integration Services (SSIS), comhpháirt de Microsoft SQL Server, na comhaid DTSX chun na céimeanna a aithint chun sonraí a phróiseáil idir freastalaithe bunachair shonraí. Is féidir comhaid DTSX a oscailt le Microsoft SQL Server 2019.

## Formáid Chomhaid DTSX

Éilíonn gluaiseacht sonraí idir freastalaithe bunachair shonraí rialacha agus céimeanna próiseála chun sláine na sonraí a áirithiú le linn na hoibríochta seo. Cinntíonn SSIS go dtarlaíonn na gníomhaíochtaí seo go léir, chun sonraí ó fhoinsí éagsúla i bhfiontar a bhogadh agus a chomhlíonadh go caothúil. Is é sin an áit a dtagann DTSX a shainíonn na struchtúir atá le húsáid ag SSIS chun na céimeanna a bhunú inar féidir na sonraí a phróiseáil de réir mar a leanann sé trí na céimeanna seo.

Tá an sreabhadh sonraí a thuairiscítear ag DTSX mar a thaispeántar san íomhá seo a leanas.

{{< figure src="../DataFlowDTSX.png" alt="Sreabhadh Sonraí DTSX" >}}

DTSX is [XML](/web/xml/)-based and is documented in [MS-DTSX](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd). The enhanced refactoring of DTSX XML is DTSX 2.0 that includes new attributes to the structures, replacement of named properties as parent XML attributes, specifies defaults for most attribute values, and placement of repeated elements inside a parent element. DTSX structures are described using these [XML Schemas](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc) and the structural format is celar-text XML.

## Tagairtí

 * [Formáid DTSX - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
 * [Formáid DTSX 2 - Le Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

