{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhaid PS",
  "description": "Foghlaim faoi fhormáid comhaid PS agus APIs ar féidir leo comhaid PS a chruthú agus a oscailt.",
  "linktitle": "PS",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-p-gas"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad .PS ann? ##

PostScript (PS) is a general-purpose page description language used in the business of desktop and electronic publishing. The main focus of PostScript (PS) is to facilitate the two-dimensional graphic design. Most languages require a distinct compilation stage before the code execution while Post Script (PS) format support a runtime straight forward interpretation. Its early version defines the graphical shapes, different text appearances and modelled imageries on printed pages or displayed pages, following the rules of Adobe imaging model. A program of PS is able to intercommunicate a document description between a composition and printing system keeping the device independent and high-level. Moreover this program is also capable of governing the appearance of text and graphics on a display.

PostScript page description is available to be rendered, displayed on printer and other output device with the help of the PostScript interpreter of the device. As the commands to print characters, graphical shapes and images are executed by interpreter, for that specific device, the high-level PostScript description converts into the low level raster data format. Generally, different applications such as illustrators, document composition systems and computer-aided design (CAD) are automated to generate PostScript page descriptions. Generally programmers have to write PostScript programs at the time of new applications creation.  However, a programmer can take advantage of the capabilities of the PostScript language that are not accessible in any application by writing a PS a program for that special situation.

## Stair Ghearr ##

The concept of the PostScript language was first introduced by John Warnock. In 1966 he was working on a project of New York Harbor. He was trying to develop an interpreter for a large three-dimensional graphics for the database of that project. For processing these graphics, John Warnock conceived the Design System language. Meanwhile Xerox PARC were looking for a standard means of defining page images for their first laser printer. Though Bob Sproull and William Newman in 1975-76 developed the Press format (data format) to drive laser printers yet a language was needed for more flexibility. In 1978 Warnock joined Martin Newell in Xerox PARC and rewrote the interpretive language, JaM which was later grew and extended into the Interpress language. Warnock founded Adobe Systems in December 1982 with Chuck Geschke, Doug Brotz, Ed Taft and Bill Paxton. They started working on a simpler language called PostScript similar to Interpress, which released commercially in 1984. Thug Steve Jobs ó Apple cuairt orthu agus thug sé comhairle dóibh PostScript a oiriúnú chun printéirí léasair a thiomáint.

I mí an Mhárta 1985, ba é LaserWriter Apple an chéad phrintéir a raibh ateangaire PostScript leabaithe aige, rud a d'athraigh an foilsitheoireacht deisce (DTP). Mar gheall ar fóntacht theicniúil agus infhaighteacht fhorleathan PostScript, rogha teanga le haghaidh foilsitheoireacht deisce agus leictreonach. I rith 1990, bhí ateangaire don teanga PostScript ina chuid riachtanach de na printéirí léasair.

## Príomhghnéithe ##

The capabilities of the PostScript language to deal with interactive graphics and page description possess the following features:

**Cruthanna:** D'fhéadfadh línte díreacha, cuair, cearnóga agus cuair chiúbacha a bheith comhdhéanta de chineál treallach, ar féidir leo a bheith féin-trasnú agus dícheangailte (i gcodanna agus i bpoill).

**Oibreoirí péintéireachta:** cead a thabhairt don imlíne crutha d’aon tiús, dath, líonadh nó cead a thabhairt an cruth a tharraingt mar ghearrthóg chun aon ghrafaic eile a bhearradh.

Tá an éagsúlacht ag **Dathanna:** mar liathscála, RGB, CMYK, agus CIE. Múnlaítear cineálacha speisialta dathanna mar ghné dhifriúil: spotdathanna, mapáil dathanna, fiú patrúin a scáthú agus a athrá.

** Téacs:** comhtháite go hiomlán le grafaicí. Thairis sin, ceadaíonn múnla íomháithe adobe carachtair téacs a thaispeáint mar chruthanna grafacha a fhéadfaidh aon ghnáthoibreoirí grafaicí a oibriú.

**Íomhánna samplála**: bainte as foinsí bunaidh (grianghraif scanta) nó is féidir iad a tháirgeadh go sintéiseach. Cuireann an teanga PostScript bealaí éagsúla ar fáil chun íomhánna a athghiniúint ag aon taifeach agus de réir samhlacha dathanna éagsúla ar ghléas aschuir.

Is féidir le teanga ríomhchláraithe ghinearálta leas a bhaint as cumais ghrafaice teanga PostScript trí Ps a leabú ina creat. Na cineálacha sonraí primitive, amhail uimhreacha, carachtair, eagair agus teaghráin; primitives rialaithe, mar shampla, lúba, nósanna imeachta agus coinníollach; agus sonraítear roinnt gnéithe neamhchoitianta, mar fhoclóirí sa teanga. Éascaíonn na gnéithe seo ríomhchláraitheoirí chun orduithe a scríobh chun oibríochtaí ardleibhéil a agairt. Comhlíonann na hoibríochtaí ardleibhéil seo riachtanais iarratais chasta. Tá cleachtas den sórt sin níos dlúithe agus níos éifeachtaí seachas úsáid a bhaint as sraith sheasta de bhunoibríochtaí.

Is féidir cláir atá scríofa in PostScript a tháirgeadh, a chur in iúl, agus a léirmhíniú i bhfoirm téacs foinseach ASCII. Is féidir an teanga ar fad a shainmhíniú i bhfoirm carachtair inphriontáilte agus spás bán. Tacaíonn an léiriú seo le ríomhchláraitheoirí an teanga a chruthú, a ionramháil agus a thuiscint go héasca. Ina theannta sin, coinníodh stóráil agus tarchur comhad i measc ríomhairí agus córais oibriúcháin éagsúla áisiúil trí neamhspleáchas an mheaisín.

Is féidir foirmeacha ionchódaithe dénártha na teanga, nuair a ráthaítear go mbeidh bealach cumarsáide iomlán trédhearcach ag an gclár chuig an ateangaire PostScript. Moltar do Adobe comhleanúnachas docht maidir le hionadaíocht ASCII ar chláir PS le haghaidh malartú doiciméad nó stórála cartlainne.

## Leaganacha ##

PS(.ps) is the file extension for a PostScript document. UK National Archives categorize five chronological versions of PostScript file, defined in the DSC version: versions 1.0, 2.0, 2.1, 3.0, 3.1. Sainmhíníonn gach leagan tuairimí struchtúracha tábhachtacha. Is fochineál speisialta de chomhad PostScript é Comhad PostScript Encapsulated (EPS) a úsáideann an teanga chun grafach dronuilleogach a shonrú. Déanann Lámhleabhar Tagartha Teanga PostScript cur síos ar EPS mar, Is clár PostScript é comhad PostScript imcapsulated (EPS) a dhéanann cur síos ar leathanach amháin ar a mhéad i bhfoirm ar féidir le feidhmchláir eile a iompórtáil le neadú laistigh de dhoiciméad ina bhfuil. Is féidir le comhad doiciméid PostScript comhad EPS a chuimsiú ann. Luaitear úsáid bhreise PostScript mar Taispeáin PostScript (DPS). Gineann DPS grafaicí ar an scáileán trí inneall grafaice a bhaineann úsáid as samhail íomháithe PostScript agus teanga.

## Tagairtí ##

* [Teaghlach Formáid PostScript]( https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)


