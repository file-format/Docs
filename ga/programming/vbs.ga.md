{
  "date": "2021-08-24",
  "keywords": [
"vbs",
"comhad",
"síneadh",
"formáid comhaid",
"Script amhairc bhunúsach",
"Treoir Ríomhchlárúcháin",
"vbs sampla",
"Microsoft visual basic",
"VBScript"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "VBS - Comhad Script Visual Basic",
  "description": "Foghlaim faoi fhormáid comhaid VBS agus APIs ar féidir leo comhaid VBS a chruthú agus a oscailt.",
  "linktitle": "VBS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vb-gas"
}
},
  "lastmod": "2021-08-24"
}

## Cad is comhad VBS ann?

Tá baint ag VBS nó VBScript leis an eagrán scripte de Microsoft Visual Basic. Sa timpeallacht ríomhaireachta, tá cead ag an úsáideoir go leor gnéithe de a rochtain agus a rialú. Tá cead ag VBScript múnla darb ainm **Component Object Model** a úsáid chun leas a bhaint as gnéithe agus uirlisí na timpeallachta. Tá an timpeallacht seo sonraithe chun VBScript a oibriú agus a rith.

Feidhmíonn sé cosúil le Javascript nuair a bhíonn rochtain ag an gcliant air i réimse na forbartha Gréasáin. Úsáideann na freastalaithe é freisin chun leathanaigh ghréasáin a phróiseáil. Is féidir é a chur san áireamh i roinnt cineálacha comhaid scriptithe eile ar nós feidhmchláir [HTML](/web/html/).


## Stair Ghearr ##

Seoladh é den chéad uair i 1996, mar chuid de na teicneolaíochtaí atá sonraithe ag Microsoft le haghaidh Windows Scripts. Forbraíodh é go sonrach le cabhair ó fhorbróirí Gréasáin ar dtús. Sa bhliain chéanna, scaoileadh taiscéalaí Microsoft Windows darb ainm Internet Explorer mar aon le gnéithe Visual Basic Script.

Leis an dul chun cinn sa teicneolaíocht agus i bhforbairt gréasáin, seoladh go leor leaganacha de VBScript mar aon le go leor ardghnéithe. Thairis sin, sa bhliain amach romhainn, beidh an teanga scriptithe seo mar chuid de Microsoft Windows le gnéithe nua.

## Sonraíocht Theicniúil ##

Maidir leis na leathanaigh ghréasáin ar thaobh an fhreastalaí, úsáidtear na huirlisí ar nós **Leathanach Freastalaí Gníomhach** in éineacht le VBScript. Is féidir an teanga scriptithe seo a úsáid freisin sa chomhpháirt scripte de Windows. Stóráiltear comhaid na teanga seo le síneadh .vbs i Windows.

Tá go leor struchtúir rialaithe cosúil le lúba a úsáidtear i gcód na teanga seo. Áiríonn sé freisin argóintí atá ina n-orduithe agus a d'fhéadfaí a ainmniú nó gan ainm. Is féidir comhaid na teanga seo a stóráil go simplí i bhfillteáin nó ar dheasc chóras oibriúcháin Windows. Cé nach bhfuil aon timpeallacht forbartha chomhtháite ar leith ann do chláir VBScript mar Microsoft Script Editor, cuireann siad áis chun an teanga seo a fhorbairt.

When VBScript is hosted by the Script host of Windows, it provides various features that are quite common to the languages of scripting but are not available in Visual Basic 6.0. Is éard atá i gceist leis na gnéithe a bhaineann le rochtain éasca nó díreach ná Printéirí Líonra, argóintí ordú-líne gan ainm agus ainmnithe, stdout, agus stdin, Scaireanna Líonra, Ionstraimíocht Bainistíochta Windows, faisnéis úsáideora líonraí cosúil le ballraíocht grúpa, agus go leor eile. 

## Formáid Comhaid VBS Sampla ##

```
<% Option Explicit %>
 <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
 <html>
 	<head>
 		<title>VBScript Example</title>
 	</head>
 	<body>
 		<div><% 
 			' Grab current time from Now() function.
 			' An '=' sign occurring after a context switch (<%) is shorthand 
 			' for a call to the Write() method of the Response object.
 			Dim timeValue : timeValue = Now %>
 			The time, in 24-hour format, is 
 			<%=Hour(timeValue)%>:<%=Minute(timeValue)%>:<%=Second(timeValue)%>.
 		</div>
 	</body>
 </html>
```

## Tagairt ##

* [VBS - le Vicipéid]( https://en.wikipedia.org/wiki/VBScript)




