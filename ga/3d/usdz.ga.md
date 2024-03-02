{
  "date": "2021-02-01",
  "keywords": [
"usdz",
"comhad usdz",
"formáid comhaid usdz",
"formáid comhaid",
"3d",
"Íosluchtaigh comhad usdz"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "USDZ - Formáid ZIP Cur síos ar an Radharc Uilíoch",
  "description": "Foghlaim faoi fhormáid comhaid USDZ agus APIs is féidir comhaid USDZ a oscailt agus a chruthú.",
  "linktitle": "USDZ",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-usd-gaz"
}
},
  "lastmod": "2021-02-01"
}

## Cad is comhad USDZ ann?

Is cartlann ZIP neamh-chomhbhrúite agus neamhchriptithe é comhad le .usdz don fhormáid comhaid [USD](/3d/usd/) (Universal Scene Description) ina bhfuil agus seachfhreastalaí do chomhaid de bhformáidí eile (amhail uigeachtaí agus beochana) leabaithe sa chartlann agus a ritheann iad go díreach le ham rite USD gan aon ghá le díphacáil. Is pacáistí iad comhaid USDZ a bhfuil a ndearadh bunaithe ar astarraingt nua Ar-leibhéal de phacáiste. Cláraíodh Usdz le IANA agus tá ainm cineál meán na samhla aige agus ainm fochineál vnd.usd+zip agus is féidir a shonraí a fháil amhail ar [IANA registration page](https://www.iana.org/assignments/media-types/model/vnd.usdz+zip).

## Formáid Comhaid USDZ

USDZ files are based on the ZIP file format that archive individual files in its container. This enables the receiver end to just unzip the contents and use the normal USD scene description files to work with and inspect. Almost all operating systems provide builtin support for the ZIP file formats and choosing this archiving format over any custom method makes it easy for USDZ files to be useful as a simple transport protocol.

### Srianta ZIP

Úsáideann formáid comhaid USDZ an fhormáid comhaid ZIP gan aon `chomhbhrú` agus `criptiúchán`. Bhí sé seo dírithe ar dhearadh chun dhá riachtanas a chomhlíonadh:

 * I gcás pacáiste atá luchtaithe sa chuimhne cheana féin nó mar chomhad singil ar dhiosca, tá na APIanna ar fáil i USD chun rochtain a fháil ar na sonraí atá san íomhá
 * Níor cheart go mbeadh aon ghá comhaid a bhaint as an diosca nó níos mó stórais chairn a leithdháileadh

Le USDZ, comhlíontar an dá riachtanas seo toisc go gceadaíonn an chuid is mó de na formáidí íomhá iad féin scéimeanna comhbhrú inmheánacha, rud a fhágann go bhfuil dlúthmhéid comhaid ann.

### Riachtanais Leagan Amach

USDZ packages require the layout of files within the package is that the data for each file should begin at a multiple of 64 bytes from the beginning of the package. However, the package should start with a native [USD](/3d/usd/) file in case of targeting the package with a simple reference. In such a case, this first USD file is referred as the Default Layer. Clients wishing to deliver streamable content may wish to consider other layout constraints, as well.

## Íoslódáil an clár do USDZ
Ós rud é go bhfuil na comhaid usdz pacáilte le híomhánna ardchaighdeáin eile agus comhaid usd, is féidir leo stóráil diosca níos mó a áitiú. Anseo is féidir leat comhad samplach USDZ simplí agus níos lú a fháil le híoslódáil:

- [Sample.usdz](../sample.usdz)

## Tagairtí

* [Sonraíochtaí Formáid Chomhaid USDZ](https://openusd.org/release/spec_usdz.html)


