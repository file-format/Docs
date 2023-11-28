{
"data": "27-09-2023",
  "keywords": [
"cfg",
"file CFG",
"file del linguaggio di markup cfg wesnoth",
"cos'è un file cfg",
"come aprire il file CFG",
"file",
"estensione file CFG",
"estensione"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato file CFG - File Wesnoth Markup Language",
  "description":"Informazioni sul formato file CFG Wesnoth Markup Language e sulle API in grado di creare e aprire file CFG.",
"linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth",
"parent" : "game"
}
},
"lastmod": "27-09-2023"
}

## Cos'è un file CFG?

Il file CFG è anche conosciuto come **"Wesnoth Markup Language" (WML)**. È un linguaggio di markup personalizzato utilizzato principalmente nel gioco "Battle for Wesnoth", che è un gioco di strategia a turni. WML viene utilizzato per definire e personalizzare vari aspetti del gioco, inclusi scenari, campagne, unità e altro. È un modo per modder e sviluppatori di creare contenuti per il gioco.

È scritto in un formato che assomiglia a una combinazione di XML e script semplici. Ecco una panoramica di alcuni elementi e strutture comuni che potresti trovare in un file WML:

1. **Tag:** WML utilizza i tag per definire diversi elementi nel gioco. I tag sono racchiusi tra parentesi angolari. Per esempio:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    










2. **Attributi:** all'interno dei tag è possibile definire attributi per specificare proprietà o valori associati all'elemento. Nell'esempio sopra, "tipo" e "hitpoint" sono attributi.
    










3. **Array e array di array:** puoi creare array di dati e persino array di array per definire elenchi di unità, tipi di terreno o altri elementi di gioco.
    










4. **Dichiarazioni condizionali:** WML supporta istruzioni condizionali per controllare il flusso del gioco. Per esempio:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    










5. **Loop:** puoi utilizzare i loop per scorrere elenchi di elementi o eseguire azioni ripetutamente.
    










6. **Include:** puoi includere altri file WML all'interno di un file WML principale per organizzare e modularizzare i tuoi contenuti.
    










7. **Gestori di eventi:** puoi definire gestori di eventi per attivare azioni quando si verificano eventi specifici nel gioco.
    











Ecco un esempio semplificato di un file WML che definisce un'unità personalizzata:

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

## La battaglia per Wesnoth

"The Battle for Wesnoth" è un gioco di strategia a turni popolare e open source. È disponibile per più piattaforme, tra cui Mac, Windows, Linux e altro. Sviluppato da una community dedicata di volontari, il gioco è noto per il suo gameplay profondo e coinvolgente, nonché per il suo ricco mondo fantasy.

Le caratteristiche principali di "La battaglia per Wesnoth" includono:

1. **Ambientazione fantasy:** il gioco è ambientato in un mondo fantastico con varie razze, tra cui umani, elfi, nani, orchi e altro ancora. La tradizione e la narrazione del gioco sono parte integrante del suo fascino.
    










2. **Strategia a turni:** Il gioco è a turni, in cui i giocatori si prendono il tempo necessario per pianificare ed eseguire le proprie mosse su griglie esagonali. Combina il combattimento tattico con il processo decisionale strategico.
    










3. **Campagne:** il gioco offre un'ampia gamma di campagne per giocatore singolo, ciascuna con la propria trama, personaggi e sfide. I giocatori possono esplorare diverse narrazioni e scenari.
    










4. **Multigiocatore:** "Wesnoth" supporta il multiplayer online, consentendo ai giocatori di competere l'uno contro l'altro in battaglie strategiche. Le modalità multiplayer includono il gioco cooperativo e le partite competitive.

## Come aprire il file CFG?

I file CFG, comunemente associati al Wesnoth Markup Language (WML) utilizzato nel gioco "The Battle for Wesnoth", possono essere facilmente modificati utilizzando qualsiasi editor di testo standard. Questi file contengono codice leggibile scritto in WML, che definisce vari aspetti del gioco, inclusi scenari, unità e campagne.

Sebbene sia possibile utilizzare qualsiasi editor di testo per modificare i file CFG, alcuni editor di testo avanzati come Emacs e Vi dispongono di plug-in per l'evidenziazione della sintassi WML. Questi plugin forniscono utili codici colore e formattazione per rendere più semplice per gli utenti distinguere i diversi elementi e strutture all'interno del codice WML.

I programmi che aprono o fanno riferimento a file CFG includono

- La battaglia per Wesnoth (gratuito) per (Windows, MAC, Linux)
-Blocco note di Microsoft

## Altri file CFG

Di seguito sono riportati altri tipi di file che utilizzano l'estensione file **.cfg**.

**Impostazioni**
- [CFG - File di configurazione di Celestia](/it/settings/cfg-celestia/)
- [CFG - File di connessione al server Citrix](/it/settings/cfg-citrix/)
- [CFG - File di configurazione MAME](/it/settings/cfg-mame/)
- [CFG - File di configurazione LightWave](/it/settings/cfg-lightwave/)

**Gioco**
- [CFG - File Wesnoth Markup Language](/it/game/cfg-wesnoth/)
- [CFG - File di configurazione MUGEN](/it/game/cfg-mugen/)
- [CFG - File di configurazione del motore di origine](/it/game/cfg-sourceengine/)

**Sistema e varie**
- [CFG - File CFG](/it/system/cfg/)
- [CFG - File di configurazione del modello Cal3D](/it/misc/cfg-cal3d/)

## Riferimenti
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
