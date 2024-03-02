{
  "date" : "2019-10-11",
  "keywords" : [ "xbrl","xbrl file", "xbrl file format", "xbrl file type", "file", "type", "what is an xbrl file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XBRL - Formáid Comhaid Tuairiscithe Gnó agus Airgeadais",
  "description":"Foghlaim faoi fhormáid comhaid XBRL agus APIs ar féidir leo comhaid XBRL a chruthú agus a oscailt.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl-ga",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Cad is comhad XBRL ann?

Is creat domhanda atá ar fáil saor in aisce é comhad le síneadh .xbrl (Teanga Tuairiscithe Gnó InteXtensible) chun faisnéis ghnó a mhalartú. Úsáidtear go forleathan anois é mar cheann de na formáidí caighdeánacha a tháinig in ionad na dtuarascálacha páipéir níos sine le taifid dhigiteacha níos úsáidí agus níos cruinne. Áirítear le sonraí a mhalartaítear ag baint úsáide as na comhaid XBRL mórleabhair, sonraí airgeadais, agus cláir chomhardaithe. Tacaíonn sé le clibeanna sonraí a cheadaíonn próiseáil sonraí ó ullmhú go céim anailíse ar fhaisnéis ghnó de gach cineál. Is féidir comhaid XBRL a oscailt le bogearraí ar nós Rivet Software Dragon View XBRL Viewer agus APInna ar nós [Aspose.Finance](https://products.aspose.com/finance/).

## Formáid Chomhaid XBRL

Is caighdeán oscailte idirnáisiúnta é XBRL do thuairisciú gnó digiteach a úsáidtear go forleathan ar fud an domhain. Is teanga í atá bunaithe ar [XML](/web/xml/) a úsáideann eilimintí XBRL, ar a dtugtar clibeanna, chun cur síos a dhéanamh ar gach mír de shonraí gnó chun sonraí a fhoirmiú le haghaidh sórtáil agus anailísiú tuairiscí. Déanann XBRL International, Inc sonraíochtaí formáid comhaid XBRL a fhorbairt agus a fhoilsiú agus tá [XBRL version 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) ar fáil d'úsáideoirí faoi láthair.

### Struchtúr Doiciméad XBRL

Is féidir le ríomhchláraitheoirí faisnéis iomlán faoin [XBRL 2.1 tags](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html) a tharchur chun feidhmchláir a scríobh chun an fhormáid comhaid seo a oibriú. Is éard atá in XBRL ná shampla XBRL, agus bailiúchán tacsanomaíochtaí.

**`Cás XBRL`** - Tosaíonn an ásc XBRL leis an<xbrl> eilimint fréimhe. Is féidir le doiciméad mór XML níos mó ná sampla XBRL amháin leabaithe ann.

**`Tacsanomaíocht XBRL`** - Sainmhínítear an {{ HYPERLINK1}} mar struchtúir scéimre XML agus sraith d'eilimint naisc sheachtracha a ndéantar tagairt dhíreach dóibh. Seo a leanas scéimre tacsanomaíochta inscálaithe a thaispeánann na tagairtí basebase.

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## Tagairtí ##

* [XBRL - Le Vicipéid](https://ga.wikipedia.org/wiki/XBRL)

* [Teanga Tuairiscithe Gnó Leathnaithe (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected- errata-2013-02-20.html)


