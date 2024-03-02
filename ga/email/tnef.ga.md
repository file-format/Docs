{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TNEF",
  "description": "Foghlaim faoi fhormáid comhaid TNEF agus APIanna ar féidir leo comhaid TNEF a chruthú agus a oscailt.",
  "linktitle": "TNEF",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-tne-gaf"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad TNEF ann?

Is dílseánach de chuid Microsoft í Iompar Neodrach Formáid Iontrála (TNEF), chun ceangaltáin ríomhphoist a chuimsiú bunaithe ar Chomhéadan Ríomhchláraithe Feidhmchláir Teachtaireachtaí (**MAPI**). Tacaíonn Microsoft Outlook agus Microsoft Exchange Server go hiomlán le TNEF agus díchódaíonn TNEF níos déanaí isteach i MAPI agus taispeánann sé na ríomhphoist formáidithe. Tá cineál MIME de MS-TNEF i gceangaltán ríomhphoist le hionchódú TNEF agus stórálann sé mar winmail/win.dat. Cuimsíonn an ceangaltán in winmail .dat an fhaisnéis seo a leanas:


|Teachtaireacht|Réada OLE|Gnéithe Outlook
---|---|---|
|<ul><li> Ceangaltáin teachtaireachta bunaidh</li><li> Bunleagan formáidithe</li><li> clónna, méideanna téacs, agus dathanna téacs</li></ul> |<ul><li> pictiúir leabaithe</li><li> doiciméid Oifige leabaithe</li></ul> |<ul><li> foirmeacha saincheaptha</li><li> cnaipí vótála</li><li> iarratais cruinnithe</li></ul>


Cuireann seirbhísí ríomhphoist eile nach dtacaíonn TNEF leo, gnáth-théacs i láthair do theachtaireachtaí formáidithe TNEF. Leabaíonn Outlook formáid shaibhir na teachtaireachta i gcomhaid TNEF (OLE) nó i ngnéithe áirithe Outlook (foirmeacha, cnaipí vótaíochta, agus iarratais comhdhála). Ní féidir ionchódú sainráite TNEF a cheadú laistigh de chliant ríomhphoist Outlook, áfach, éascaítear go hintuigthe ionchódú TNEF má roghnaíonn tú formáid RTF chun ríomhphost a sheoladh.

## Formáid Chomhaid TNEF

Bunaíonn algartam sonraí TNEF struchtúr leata ó airíonna teachtaireachtaí ordlathacha saibhre. Úsáideann na struchtúir leacaithe seo ansin chun sraith sraitheach sonraí comhdhéanta d’airíonna áirithe a léiriú.

I gcásanna áirithe, nuair a tharlaíonn airíonna i ngrúpaí nó nuair a bhíonn illuachanna acu, d’fhéadfadh comhaireamh agus stuáil a bheith san áireamh i sruth chun ailíniú sonraí ar leith a fhorfheidhmiú. Cás ar leith ina bhfuil buntáiste ag baint le húsáid an algartam seo ná i dtimpeallacht teachtaireachtaí nach dtacaíonn. I dtimpeallachtaí den sórt sin, déanann Scríbhneoir TNEF maoin shaibhir teachtaireachta a ionchódú i sruth sraitheach sonraí. Ina theannta sin, is féidir na hairíonna nach mbaineann leis an TNEF bunúsach a chuimsiú le linn tarchuir. Cuireadh na hairíonna cuimsithe seo ar fáil ansin trí dhíchódú trí TNEF chun a chinntiú go raibh fáil ar gach maoin den teachtaireacht bhunaidh chuig an bhfeidhmchlár cliant.

In TNEF is beag deireadh a bhíonn le gach cineál sonraí uimhriúil agus bíonn a méid níos mó ná beart amháin. Chun na luachanna uimhriúla seo a láimhseáil ar ardáin neamhbheaga, ní mór na claochluithe cuí a chur i gcrích chun luachanna cearta a fháil. Léirítear luachanna teaghráin i bhformáid Fhoirm Mhéadaithe Backus-Naur (ABNF) de réir sonraíochtaí [RFC5234]. Nuair a chríochnaíonn an teaghrán le carachtar nialasach, tá sé san áireamh freisin; mar shampla, `worker@specimen.com %x00`.

{{< figure src="../TNEF.png" alt="Formáid Chomhaid TNEF" >}}

## Tréithe TNEF agus rialacha Próiseála ##

Tosaíonn an sruth sonraí in TNEF le huimhir leagáide leagáide, síniú, eochairluach primitive, agus tréith a léiríonn leathanach cóid. Gintear an leathanach cóid seo nuair a thaifeadann an t-ionchódóir tréithe agus airíonna ANSI. Ina dhiaidh sin, tháinig an sruth chun bheith ina sraith tréithe inar líneáil tréithe teachtaireachta ar dtús agus ansin tréithe ceangaltáin ina dhiaidh sin. Tá tréithe éagsúla teachtaireachta agus ceangaltáin le fáil i tréithe speisialta amhail attMsgProps, AttAttachment, agus attRecipTable. Sna tréithe atá le feiceáil i sruth TNEF, tá an struchtúr, na hairíonna teachtaireachta agus na tiontuithe atá riachtanach chun iad a chur i ngleic le hairíonna teachtaireachta. Is éard atá i ngach tréith aitheantais, méid agus sonraí an tréith, seiceam agus leibhéal de réir a fheidhmithe.

## Gaol le Prótacail agus Algartam Eile ##

Teastaíonn algartam sonraí TNEF le haghaidh iompair ó na córais a bhfuil drochmheicníocht acu chun formáid shaibhir teachtaireachta a thaispeáint. Ag baint úsáide as an gcineál meán ms-TNEF, is éard atá in aschur an algartam ná comhad ceangaltáin (winmail.dat) agus cuid de choirp MIME atá sonraithe in [RFC2045]. Tarchuirtear corp na teachtaireachta gnáth-théacs trí úsáid a bhaint as UUENCODE de réir sonraíochta [MSDN-UAF] agus díchódaítear an corp teachtaireachta seo nó modh coibhéiseach ag deireadh an fhaighteora. Thairis sin, is féidir le TNEF sonraí teachtaireachtaí a tharchur ag baint úsáide as prótacail idirlín éagsúla cosúil le SMTP, POP3, IMAP4, agus na cinn, MIME a chomhtháthú de réir chaighdeán RFC2045.

## Ráiteas Infheidhmeachta ##

I dteannta le tarchur teachtaireachta simplí, bhí feidhmchlár bunaidh TNEF le cruthú chun ranganna teachtaireachtaí a úsáid agus chun tacú le gnéithe breise nach bhfuil aon tacaíocht bhunaidh acu i bprótacal iompair. Rinneadh tuilleadh scagtha ar an bhfeidhmchlár seo maidir le hairíonna saibhre teachtaireachta agus airíonna ainmnithe a úsáideann cliaint teachtaireachtaí nua-aimseartha anois le lá a tharchur. Chun comhlíonadh an bhunfheidhmithe, coinnítear comhréir na n-airíonna bunaidh agus coimeádann tréith speisialta airíonna na teachtaireachta nua ar leithligh.

## Tagairtí

* [Formáid Iompar Neodrach um Imchochlú](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)

* [Seoltaí ríomhphoist agus leabhair seoltaí in Exchange Server](https://learn.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# seachfhreastalaí-2019)

* [[MS-OXTNEF]: Algartam Sonraí Formáid Imchlúdaithe Neodrach Iompar (TNEF)](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)


