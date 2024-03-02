{
  "date": "2020-01-10",
  "keywords": [
"comhad otg",
"formáid comhaid otg",
"cad is comhad otg ann",
"comhad",
"sampla otg",
"síneadh comhad otg",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OTG - Formáid Chomhaid Teimpléad Líníochta OpenDocument",
  "description": "Foghlaim faoi fhormáid comhaid OTG agus APIanna ar féidir leo comhaid OTG a chruthú agus a oscailt.",
  "linktitle": "OTG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ot-gag"
}
},
  "lastmod": "2020-01-10"
}

## Cad is comhad OTG ann?

Teimpléad líníochta is ea comhad OTG a chruthaítear leis an gcaighdeán OpenDocument a leanann Feidhmchláir Oifige OASIS [1.0 specification](https://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0-os.pdf). Léiríonn sé eagrú réamhshocraithe na n-eilimintí líníochta le haghaidh íomhá veicteora is féidir a úsáid chun a bhfuil sa chomhad a fheabhsú tuilleadh. Tá comhaid OTF cosúil le haon chomhaid eile atá bunaithe ar fhormáid OpenDocument atá bunaithe ar fhormáid XML chun ábhar an doiciméid a léiriú. Is féidir comhaid OTF a fheiceáil ach iad a oscailt in aon téacs nó in aon eagarthóir caighdeánach XML.

## Sonraíochtaí Formáid Chomhaid OTG ##

Tá formáid comhaid OTG bunaithe ar fhormáid OpenDocument XML a bhfuil scéimre seanbhunaithe aici. Léirítear struchtúr gach comhpháirte d’fhormáid OpenDocument ag eilimint a bhfuil tréithe gaolmhara aici agus atá coitianta do gach cineál doiciméad ar nós doiciméad téacs, scarbhileog, nó comhad líníochta. Úsáideann OTG, mar theimpléad líníochta, go forleathan na sonraíochtaí Ábhar Grafaice lena n-áirítear:

  * Gnéithe Leathanaigh Feabhsaithe le haghaidh Feidhmchláir Ghrafacha
  * Cruthanna Líníochta
  * Frámaí
  * Cruthanna 3D
  * Cruth an Chustaim
  * Cruthanna Cur i láthair
  * Beochan Cur i láthair
  * Beochan Cur i Láthair SMIL
  * Imeachtaí Cur i Láthair
  * Réimsí Téacs Láithreach
  * Ábhar Doiciméad Léirithe

### Gnéithe Leathanaigh Feabhsaithe le haghaidh Feidhmchláir Ghrafacha ###
#### Máistir Bileoga ####

Teimpléad is ea an eilimint Handout Master chun na leathanaigh bileoige a ghiniúint go huathoibríoch d’fheidhmchláir a thacaíonn le leathanaigh den sórt sin a phriontáil.
Is féidir na tréithe a bhaineann leis an `<style:handout-master> `eilimint are:

|Leagan Amach|Tréith|Cur Síos
---|---|---|
|Leagan Amach an Láithreoireachtaí|Láithreoireacht:Láithreoireachta-Leathanach-leagan-ainm|Naisc le `<style:presentation-page-layout> `tréith
| Leagan Amach an Leathanaigh|`stíl:leathanach-leagan amach-ainm` | Sonraíonn sé leagan amach leathanaigh ina bhfuil méideanna, teorainn agus treoshuíomh phríomhleathanach na bileoige.
|Stíl Leathanaigh|`tarraingt:stíl-ainm`| Sanntar tréithe formáidithe breise do mháistirleathanach bileoige trí stíl leathanaigh líníochta a shannadh.|
|Dearbhú Ceannteidil | `cur i láthair:use-header-name`| Sonraíonn sé ainm an dearbhaithe réimse ceanntásca a úsáidtear do na réimsí ceanntásc go léir a thaispeánfar ar an máistir-leathanach bileoga.
|Dearbhú Buntásc| cur i láthair:use-footer-name|Sonraíonn sé ainm dhearbhú réimse an bhuntásc a úsáidtear do gach réimse buntásc a thaispeánfar ar mháistirleathanach na bileoige.
|Dáta agus Ama|Dearbhú Dáta Úsáide-Am-Ainm|Sonraíonn sé ainm an dearbhaithe réimse dáta-am a úsáidtear do gach réimse dáta-ama a thaispeánfar ar an máistir-leathanach bileoga.

### Cruthanna Líníochta ###
Tacaíonn formáid OpenDocument le roinnt cruthanna líníochta ar féidir le haon chineál doiciméid a úsáid.

|Cruth|Tréithe Gaolmhara| eilimintí
---|---|---|
Dronuilleog - `<draw:rect> `|Suíomh, Méid, Stíl, Ciseal, Z-Innéacs, ID, Aitheantas Fotheidil, Ancaire téacs, cúlra tábla, tarraing suíomh deiridh, Coirnéil bhabhta | Teideal, Cur Síos Fada, Éisteoirí Imeachtaí, Pointí Gliú, Téacs
Líne `<draw:line> `| Stíl, Ciseal, Z-Innéacs, ID, Aitheantas Fotheidil agus Claochlú, Ancaire téacs, cúlra tábla, pointe tosaigh tarraingthe, Pointe deiridh | Teideal, Cur Síos Fada, Éisteoirí Imeachtaí, Pointí Gliú, Téacs
Polailín `<draw:polyline> `| Seasamh, Méid, Amharcbhosca, Stíl, Ciseal, Z-Innéacs, ID, Aitheantas Fotheideal agus Claochlú, Ancaire téacs, cúlra tábla, tarraingt suíomh deiridh, Pointí | Teideal, Cur Síos Fada, Éisteoirí Imeachtaí, Pointí Gliú, Téacs
Polagán `<draw:polygon> `|Suíomh, Méid, Amharcbhosca, Stíl, Ciseal, Z-Innéacs, ID, Aitheantas Fotheidil agus Claochlú, Ancaire téacs, cúlra tábla, suíomh deiridh na tarraingthe, Pointí|Teideal, Cur Síos Fada, Éisteoirí Imeachta, Pointí Gliú, Téacs
|Polagán Rialta`<draw:regular-polygon> `|Suíomh, Méid, Stíl, Ciseal, Z-Innéacs, ID, Aitheantas Fotheidil agus Claochlú, Ancaire téacs, cúlra tábla, suíomh deiridh na tarraingthe, Cuasach, Cúinní, Géire|Teideal, Cur Síos Fada, Éisteoirí Imeachtaí, Pointí Gliú, Téacs
|Pát`<draw:path> `|Suíomh, Méid, Amharcbhosca, Stíl, Ciseal, Z-Innéacs, ID, Aitheantas Fotheidil agus Claochlú,Ancaire téacs, cúlra tábla, suíomh deiridh tarraingthe, Sonraí cosáin| Teideal, Cur Síos Fada, Éisteoirí Imeachtaí, Pointí Gliú, Téacs

### frámaí ###
Is coimeádán dronuilleogach é fráma, i ndoiciméad líníochta, ina bhfuil boscaí téacs, íomhánna nó rudaí. Tacaíonn frámaí le gnéithe breise cosúil le comhrianta, léarscáileanna íomhá, agus hipearnaisc. Féadfaidh réad chomh maith le híomhá a bheith i bhfráma, rud a fhágann gur féidir illéirithe réad a bheith ann. Déanann na hiarratais an eilimint faoi seach bunaithe ar an tacaíocht is fearr.

Is féidir le frámaí a bheith ann:
  * Boscaí téacs
  * Oibiachtaí a léirítear i bhformáid OpenDocument nó i bhformáid dhénártha atá sainiúil do oibiachtaí
  * Íomhánna
  * Feidhmchláiríní
  * Breiseáin
  * Frámaí ar snámh

Tá fráma i ndoiciméad mar a thaispeántar thíos.

```
<define name=draw-frame>
<element name=draw:frame>
<ref name=common-draw-shape-with-text-and-styles-attlist/>
<ref name=common-draw-position-attlist/>
<ref name=common-draw-rel-size-attlist/>
<ref name=common-draw-caption-id-attlist/>
<ref name=presentation-shape-attlist/>
<ref name=draw-frame-attlist/>
<zeroOrMore>
<choice>
<ref name=draw-text-box/>
<ref name=draw-image/>
<ref name=draw-object/>
<ref name=draw-object-ole/>
<ref name=draw-applet/>
<ref name=draw-floating-frame/><ref name=draw-plugin/>
</choice>
</zeroOrMore>
<optional>
<ref name=office-event-listeners/>
</optional>
<zeroOrMore>
<ref name=draw-glue-point/>
</zeroOrMore>
<optional>
<ref name=draw-image-map/>
</optional>
<optional>
<ref name=svg-title/>
</optional>
<optional>
<ref name=svg-desc/>
</optional>
<optional>
<choice>
<ref name=draw-contour-polygon/><ref name=draw-contour-path/>
</choice>
</optional>
</element>
</define>
```

## Tagairtí ##
* [Formáid Doiciméid Oscailte OASIS le haghaidh Feidhmchláir Oifige](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)

* [Formáid OpenDocument - Vicipéid](https://ga.wikipedia.org/wiki/OpenDocument)


