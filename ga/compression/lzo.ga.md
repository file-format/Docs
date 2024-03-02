{
  "date": "2021-06-16",
  "keywords": [
"LZO",
"Comhbhrúite",
"Comhad",
"Síneadh",
"Formáid Chomhaid",
"Lempel-Ziv-Oberhume"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid LZO",
  "description": "Foghlaim faoi fhormáid comhaid LZO agus APIs ar féidir leo comhaid LZO a chruthú agus a oscailt.",
  "linktitle": "LZO",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lz-gao"
}
},
  "lastmod": "2021-06-16"
}

## Cad is comhad LZO ann? ##

Comhcheanglaítear comhad le síneadh .lzo le gnéithe cartlannaithe comhad ar féidir leo méid comhaid uile an chomhaid chomhbhrúite a laghdú. Féadfaidh na comhaid comhbhrúite go léir a bheith comhdhéanta de chomhad amháin nó níos mó nó fiú grúpaí de cheangail le roinnt comhad de chineálacha agus de thoisí éagsúla. Tá méid comhaid chomhbhrúite níos lú i gcomparáid le comhmhéid na gcomhad agus na bhfillteán go léir atá stóráilte i gcomhad comhbhrúite LZO. Stóráiltear na comhaid LZO go léir i bhformáid LZO agus déantar iad a fhorghníomhú go sainráite le gnéithe comhbhrú a úsáideann bogearraí comhbhrú agus dí-chomhbhrúite LZOP. Cuirtear na sonraíochtaí comhbhrú go léir le chéile sa chlár comhbhrú agus dí-chomhbhrú comhad seo a tháinig ó leabharlann comhbhrú comhad Lempel-Ziv-Oberhume. Comhcheanglaítear luas dí-chomhbhrú níos tapúla agus cóimheasa comhbhrú forbartha sna comhaid LZO seo freisin.

## Sonraíocht LZO ##

Markus Franz Xaver Johannes Oberhumer developed the original "lzop" algorithm, based on earlier algorithms by Abraham Lempel and Jacob Ziv, in 1996. Cuireann an leabharlann seo éagsúlacht halgartaim i bhfeidhm leis na tréithe seo a leanas:

* Comhbhrú níos tapúla ná DEFLATE

* Dí-chomhbhrú tapa

* Maoláin bhreise a theastaíonn le linn comhbhrú (de mhéid 8KB nó 64KB, ag brath ar leibhéal an chomhbhrú)

* Is iad na maoláin foinse agus ceann scríbe an chuimhne go léir a theastaíonn le haghaidh dí-chomhbhrú

* Soláthraíonn rialú ar an dá chóimheas comhbhrú agus luas comhbhrú


Mar algartam comhbhrú bloc, déanann LZO comhbhrú forluiteach chomh maith le dí-chomhbhrú in-áit. Chun comhbhrú forluiteach a bhaint amach, ní mór méid bloc an chomhbhrú agus an dí-chomhbhrúite a mheaitseáil. Roinneann an t-algartam comhbhrú LZO na sonraí ionchuir ina meaitseanna (foclóir sleamhnáin) agus liteartha nach meaitseálann, ag tabhairt torthaí maithe le sonraí an-iomarcacha agus torthaí inghlactha le sonraí neamh-chomhbhrúite, ag méadú sonraí do-chomhbhrúite faoi 1/64 den bhunleagan méid.

## Fadhbanna le comhad LZO a oscailt ##

Seo a leanas na roinnt fadhbanna a d'fhéadfadh a bheith ina gcúis le droch-oibriú formáid comhaid LZO:
  
* Féadfaidh an comhad a bheith truaillithe. Chun an fhadhb seo a réiteach, íoslódáil an comhad arís nó iarr ar an seoltóir an comhad a sheoladh arís
* Is é an chúis dara comhad ionfhabhtaithe sa chás seo scanadh an comhad i gceart
* Naisc mhíchuí leis an gcomhad LZO
  *	 Removal of the description of the LZO 
* Níl go leor acmhainní crua-earraí
* Tiománaithe as dáta an trealaimh
  
## Tagairtí ##

* [LZO - Le Vicipéid]( https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)


