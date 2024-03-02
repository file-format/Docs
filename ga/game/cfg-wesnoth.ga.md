{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"comhad cfg",
"cfg comhad teanga marcála wesnoth",
"Cad is comhad cfg ann",
"Conas a oscailt cfg comhad",
"comhad",
"Síneadh comhad cfg",
"síneadh"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid CFG - Comhad Teanga Marcáil Wesnoth",
  "description": "Foghlaim faoi fhormáid Chomhaid Teanga Chomhad Marcáil CFG Wesnoth agus APIanna ar féidir leo comhaid CFG a chruthú agus a oscailt.",
  "linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth-ga",
      "parent": "game"
}
},
  "lastmod": "2023-09-27"
}

## Cad is comhad CFG ann?

Tugtar an **Teanga Mharcála Wesnoth (WML)** ar chomhad CFG freisin. Is teanga mharcála shaincheaptha í a úsáidtear go príomha sa chluiche Battle for Wesnoth, ar cluiche straitéise cas-bhunaithe é. Úsáidtear WML chun gnéithe éagsúla den chluiche a shainiú agus a shaincheapadh, lena n-áirítear cásanna, feachtais, aonaid, agus go leor eile. Is bealach é do modders agus forbróirí ábhar a chruthú don chluiche.

Tá sé scríofa i bhformáid atá cosúil le meascán de XML agus scriptiú simplí. Seo forbhreathnú ar roinnt gnéithe agus struchtúir choitianta a d'fhéadfá a fháil i gcomhad WML:

1.  **Clibeanna:** Úsáideann WML clibeanna chun gnéithe éagsúla den chluiche a shainiú. Tá clibeanna faoi iamh idir lúibíní uillinne. Mar shampla:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    
2.  **Tréithe:** Laistigh de chlibeanna, is féidir leat tréithe a shainiú chun airíonna nó luachanna a bhaineann leis an eilimint a shonrú. Sa sampla thuas, is tréithe iad cineál agus buailphointí.
    
3.  **Eagairlí agus Eagara:** Is féidir leat eagair de shonraí agus fiú eagair eagair a chruthú chun liostaí aonad, cineálacha tír-raon, nó eilimintí cluiche eile a shainiú.
    
4.  **Ráitis Choinníollacha:** Tacaíonn WML le ráitis choinníollacha chun sreabhadh an chluiche a rialú. Mar shampla:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    
5.  **Lúba:** Is féidir leat lúba a úsáid chun liostaí míreanna a aithris nó gníomhartha a dhéanamh arís agus arís eile.
    
6.  **Áirítear:** Is féidir leat comhaid WML eile a áireamh laistigh de phríomhchomhad WML chun d’inneachar a eagrú agus a mhodúlú.
    
7.  ** Láimhseálaithe Imeachtaí:** Is féidir leat láimhseálaithe imeachtaí a shainiú chun gníomhartha a spreagadh nuair a tharlaíonn imeachtaí sonracha sa chluiche.
    

Seo sampla simplithe de chomhad WML a shainíonn aonad saincheaptha:

```
[unit_type]
    id=my_custom_unit
    name="Custom Unit"
    description="A unit created using WML."
    image="units/my_custom_unit.png"
    hitpoints=30
    movement_type=foot
[/unit_type]
```

## An Cath do Wesnoth

Is cluiche straitéise cas-bhunaithe foinse oscailte é The Battle for Wesnoth. Tá sé ar fáil le haghaidh ardáin éagsúla, lena n-áirítear Mac, Windows, Linux, agus níos mó. Arna fhorbairt ag pobal tiomnaithe oibrithe deonacha, tá cáil ar an gcluiche mar gheall ar a gameplay domhain tarraingteach, chomh maith lena shaol saibhir fantaisíochta.

I measc na bpríomhghnéithe de The Battle for Wesnoth tá:

1.  **Socrú Fantasy: ** Tá an cluiche suite i ndomhan fantaisíochta le rásaí éagsúla, lena n-áirítear daoine, elves, áiteacha, orcs, agus go leor eile. Tá seanchas agus scéalaíocht an chluiche mar chuid lárnach dá tharraingt.
    
2.  **Straitéis Cas-Bhunaithe:** Tá gameplay bunaithe ar sheal, áit a thógann imreoirí a gcuid ama chun a gcuid gluaiseachtaí a phleanáil agus a dhéanamh ar ghreillí heicseagánacha. Nascann sé comhrac oirbheartaíochta le cinnteoireacht straitéiseach.
    
3.  **Feachtais:** Tairgeann an cluiche raon leathan feachtais aon-imreoir, gach ceann acu lena scéal-líne, carachtair agus dúshláin féin. Is féidir le himreoirí scéalta agus cásanna éagsúla a fhiosrú.
    
4.  ** Il-imreoir: ** Tacaíonn Wesnoth le il-imreora ar líne, rud a ligeann d'imreoirí dul san iomaíocht i gcoinne a chéile i gcathanna straitéiseacha. I measc na modhanna il-imreora tá súgradh comhoibríoch agus cluichí iomaíocha.

## Conas comhad CFG a oscailt?

Is féidir comhaid CFG, a bhaineann go coitianta leis an Wesnoth Markup Language (WML) a úsáidtear sa chluiche The Battle for Wesnoth, a chur in eagar go héasca le haon eagarthóir caighdeánach téacs. Tá cód inléite daonna scríofa i WML sna comhaid seo, a shainíonn gnéithe éagsúla den chluiche, lena n-áirítear cásanna, aonaid agus feachtais.

Cé gur féidir leat aon eagarthóir téacs a úsáid chun comhaid CFG a mhodhnú, tá forlíontáin aibhsithe comhréire WML ar fáil ag roinnt ard-eagarthóirí téacs ar nós Emacs agus Vi. Soláthraíonn na forlíontáin seo dathchódú agus formáidiú cabhrach chun é a dhéanamh níos éasca d’úsáideoirí idirdhealú a dhéanamh idir gnéithe agus struchtúir éagsúla laistigh den chód WML.

Áirítear le cláir a osclaíonn nó a thagraíonn comhaid CFG

- An Cath do Wesnoth (Saor in Aisce) le haghaidh (Windows, MAC, Linux)
- Microsoft Notepad

## Comhaid CFG eile

Seo cineálacha comhaid eile a úsáideann an síneadh comhad **.cfg**.

**Socruithe**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**Cluiche**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**Córas & Misc**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

## Tagairtí
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
