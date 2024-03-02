{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhaid WMV",
  "description": "Foghlaim faoi fhormáid comhaid WMV agus APIs is féidir comhaid WMV a chruthú agus a oscailt.",
  "linktitle": "WMV",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-wm-gav"
}
},
  "lastmod": "2019-09-16"
}

## Cad is comhad WMV ann?

Is coimeádán digiteach ilmheán é Formáid Ardchórais (ASF) atá deartha go príomha chun sruthanna meán a stóráil agus a tharchur. Is é Microsoft Windows Media Video (WMV) an fhormáid físeán comhbhrúite agus is é Microsoft Windows Media Audio (WMA) an fhormáid fuaime comhbhrúite mar aon le meiteashonraí breise sa choimeádán ASF atá forbartha ag Microsoft. Chomh luath agus na comhaid WMV nó WMA atá ionchódaithe le Windows Media Video agus Windows Media Fuaime codecs ansin iad ionadaíocht le síneadh .asf. Déanann WMV comhaid mhóra a chomhbhrú le haghaidh ráta tarchurtha níos fearr thar líonra agus cáilíocht na físe á chothabháil. Tá WMV deartha go sonrach le rith ar gach feiste Windows. Tar éis an chaighdeánaithe ag Cumann na nInnealtóirí Pictiúr agus Teilifíse (SMPTE), meastar anois gur formáid chaighdeánach oscailte é WMV.

## Stair ##

With the help of Microsoft proprietary codecs new compressed video format was developed in 1999 known as WMV7 which was based on MPEG-4 Part 2. Cuireadh feabhsuithe in dhá leagan eile .i. WMV8 agus 9. Chuir Microsoft leagan 9^^ú^^ de WMV faoi bhráid SMPTE le haghaidh caighdeánaithe in 2003 a caighdeánaíodh faoi dheireadh in 2006 mar SMPTE 421M ar a dtugtar VC-1 freisin. Ba é an smaoineamh a bhí taobh thiar den WMV ná formáid meáin a fhorbairt a d'fhéadfadh na crua-earraí agus na bogearraí go léir a fhaigheann tacaíocht ó Microsoft a thacú. Ina theannta sin, ba mhórchuspóir eile é sruthanna físeáin a tharchur thar an idirlíon sa chás optamach. Tar éis an caighdeánaithe ó SMPTE, tháinig WMV freisin mar fhormáid físeáin do dioscaí Blu-ray.

## Sonraíochtaí Formáid Comhaid

### Coimeádán

Go ginearálta, déantar WMV a phacáil isteach i gcoimeádán ASF ach ina theannta sin, is féidir le coimeádán Matroska nó AVI tacú leis freisin le síntí .mkv agus .avi faoi seach.

### Físeán Windows Media 9

Cé go bhfuil codecs fuaime agus físe éagsúla ar fáil sa tsraith Windows Media Video 9 le haghaidh údarú agus athsheinm na meán digiteach, is é CODEC WMV-9 an CODEC físeáin is déanaí agus is fearr mar is féidir leis an comhbhrú is fearr a bhaint amach ó rátaí giotán an-íseal ie 160 x 120 ag 10 Kbps go 1920 x 1080 ag 4-8 Mbps le haghaidh éagsúlacht físeáin HD.

### Struchtúr an Chóid

Tá formáid datha inmheánach 8-giotán 4:2:0 ag WMV-9. Cosúil le gach caighdeán comhbhrú físe tóir eile MPEG-1 agus H.261, úsáideann WMV-9 scéim cúitimh tairiscint atá bunaithe ar bhloc agus claochlú spásúil. Go ginearálta, is féidir linn a rá go gcomhlíonann na caighdeáin seo cúiteamh tairiscint bloc-ar-bhloc ón bhfráma ath-thógtha roimhe seo le cabhair ó chainníocht 2-D ar a dtugtar an veicteoir tairiscint (MV) chun díláithriú spásúil a chur in iúl. Cruthaítear an bloc srutha le cabhair ó na luachanna a thuar ón bhfráma atógtha roimhe seo den mhéid chéanna a dhíláithrítear ón suíomh reatha ag an veicteoir gluaisne. Faoi dheireadh, ríomhtar an earráid iarmharach mar an difríocht idir an bloc tuartha tairiscint-chúitimh agus an bloc iarbhír. Déantar an earráid iarmharach seo a chlaochlú trí úsáid a bhaint as claochlú líneach comhdhlúthaithe fuinnimh ansin cainníochtaithe agus códaithe eantrópachta.

Quantized transform coefficients are entropy decoded, de-quantized, and inverse transformed to produce an approximation of the residual error on the decoder side, which is then added to the motion-compensated prediction to generate the reconstruction. The high-level description of the codec is shown in the following image.

Pléifidh an chuid eile den alt na feabhsuithe nua i WMV-9 a dhéanann idirdhealú idir é agus an chuid eile de na réitigh códaithe físeáin cosúil le caighdeáin MPEG. Tá frámaí laistigh (I), tuartha (P) agus frámaí déthreoracha (B) ag WMV-9. Is éard atá i bhfrámaí laistigh ná iad siúd atá códaithe go neamhspleách agus nach bhfuil ag brath ar fhrámaí eile. Is frámaí tuartha iad frámaí a bhraitheann ar fhráma amháin san am atá caite. Ní féidir fráma tuartha a dhíchódú ach amháin tar éis gach fráma tagartha roimh an bhfráma reatha a thosaíonn ón bhfráma is déanaí (I) a dhíchódú. Is frámaí iad frámaí B a bhfuil dhá thagairt acu—ceann san am atá thart agus ceann eile sa todhchaí ama. Tarchuirtear frámaí B tar éis a dtagairtí, rud a chiallaíonn go seoltar frámaí B as ord chun a chinntiú go bhfuil a dtagairtí ar fáil tráth an díchódaithe. Ní úsáidtear frámaí B i WMV-9 mar thagairt do fhrámaí ina dhiaidh sin. Cuireann sé seo frámaí B lasmuigh den lúb díchódaithe, rud a fhágann gur féidir aicearraí a ghlacadh le linn frámaí B a dhíchódú gan sruth nó artifacts amhairc fadtéarmacha. Coinníonn an sainmhíniú thuas ar fhrámaí I, P, agus B le haghaidh seichimh fhorásacha agus idirfhálaithe araon.

Cuirtear feidhmíocht na gcódaitheoirí físeáin i gcomparáid lena gcuid plota saobhadh ráta (RD). Is cuar 2-T é a thaispeánann an saobhadh a tháirgeann an comhbhrú ag ráta giotán áirithe.

Thug WMV-9 aghaidh ar an bhfadhb seo le tabhairt isteach teicnící éagsúla atá liostaithe thíos:

1. Claochlú méid bloc oiriúnaitheach

2. Claochlú beachtas teoranta

3. Cúiteamh tairiscint

4. Cainníochtú agus díchainníochtú

5. Ardchódú eantrópachta

6. Scagadh lúb

7. Ardchódú fráma B

8. Códú interlace

9. Smúdála forluí

10. Uirlisí le ráta íseal

11. Cúiteamh fading

## Tagairtí

* [ https://bytescout.com/blog/2018/02/windows-media-video-format.html ]( https://bytescout.com/blog/2018/02/windows-media-video-format.html )

* [ https://en.wikipedia.org/wiki/Windows_Media_Video ]( https://en.wikipedia.org/wiki/Windows_Media_Video )


