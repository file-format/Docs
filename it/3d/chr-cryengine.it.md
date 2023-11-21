{
"data":"2023-10-11",
   "keywords":[
"chr",
"file chr",
"file di caratteri chr cryengine",
"come aprire un file chr",
"file",
"estensione file chr",
"estensione",
"file"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato file CHR - File di caratteri CryENGINE",
   "description":"Informazioni sul formato di file dei caratteri CHR CryENGINE e sulle API in grado di creare e aprire file CHR.",
"linktitle": "CHR CryENGINE",
   "menu":{
      "docs":{
         "identifier":"3d-chr-cryengine",
"parent": "3d"
}
},
"lastmod":"2023-10-11"
}

## Cos'è un file CHR?

Il file CHR nel contesto di CryENGINE si riferisce a un **file di caratteri CryENGINE**. CryENGINE è un motore di gioco sviluppato da Crytek e questi file vengono utilizzati per memorizzare modelli di personaggi e dati associati da utilizzare nei videogiochi e altre applicazioni in tempo reale.

## File di caratteri CryENGINE

Un file di caratteri CryENGINE contiene in genere i seguenti componenti:

1. **Modello del personaggio**: questo è il modello 3D del personaggio, inclusa la sua geometria, trame e animazioni. Questi modelli vengono spesso creati utilizzando software come Autodesk Maya o Blender e quindi importati in CryENGINE.
    




















2. **Dati di animazione**: CryENGINE supporta animazioni complesse per i personaggi, quindi il file ".chr" può includere varie animazioni come camminare, correre, saltare e altro. Queste animazioni vengono generalmente archiviate come dati di fotogrammi chiave.
    




















3. **Informazioni sul rigging**: il rigging si riferisce al processo di creazione della struttura scheletrica per il modello del personaggio, che consente di applicare le animazioni al modello. Il file ".chr" può contenere informazioni sulla gerarchia delle ossa e su come la mesh del personaggio è collegata a questo scheletro.
    




















4. **Dati sui materiali e sulle texture**: le informazioni sui materiali utilizzati sul modello del personaggio e le mappe delle texture associate possono essere incluse nel file ".chr". CryENGINE supporta il rendering basato sulla fisica, quindi questi materiali possono essere piuttosto dettagliati.
    




















5. **Dati fisici**: se il personaggio è destinato a interagire con il mondo di gioco, il file ".chr" potrebbe includere dati fisici come forme di collisione o vincoli per la fisica del ragdoll.
    




















6. **Impostazioni di configurazione**: varie impostazioni di configurazione relative al comportamento del personaggio nel mondo di gioco, come il comportamento dell'IA o gli eventi con script, possono anche far parte del file ".chr".

## CryENGINE

CryENGINE è un potente motore di gioco sviluppato da Crytek, società tedesca di videogiochi. È noto per le sue capacità grafiche all'avanguardia ed è stato utilizzato per creare alcuni videogiochi visivamente sbalorditivi e tecnologicamente avanzati. Ecco alcune caratteristiche e informazioni chiave su CryENGINE:

1. **Grafica e rendering**: CryENGINE è rinomato per le sue capacità grafiche avanzate. Supporta funzionalità come illuminazione globale in tempo reale, illuminazione e ombre dinamiche di alta qualità, rendering basato sulla fisica (PBR) e texture ad alta risoluzione. Queste funzionalità contribuiscono a creare mondi di gioco visivamente sbalorditivi e realistici.
    




















2. **Motore fisico**: CryENGINE include un motore fisico integrato che consente interazioni realistiche tra gli oggetti nel mondo di gioco. Supporta funzionalità come la fisica del corpo rigido, la fisica del corpo morbido e la fisica del ragdoll, rendendolo adatto alla creazione di ambienti dinamici e coinvolgenti.
    




















3. **Terreno e vegetazione**: CryENGINE fornisce strumenti per creare ambienti esterni vasti e dettagliati. Supporta la modifica del terreno, il posizionamento della vegetazione e i sistemi meteorologici dinamici, consentendo agli sviluppatori di creare ambientazioni esterne ampie e realistiche.
    




















4. **Animazione dei personaggi**: CryENGINE include strumenti robusti per l'animazione dei personaggi. Supporta rig di personaggi complessi, animazioni facciali e un sistema di alberi di fusione che consente agli sviluppatori di creare movimenti e animazioni dei personaggi realistici.
    




















5. **Sistema AI**: il motore è dotato di un sistema AI che consente la creazione di NPC intelligenti (personaggi non giocanti) e IA nemica. Gli sviluppatori possono programmare il comportamento e le interazioni dell'IA per creare esperienze di gioco stimolanti e coinvolgenti.
       





















6. **Scripting**: CryENGINE utilizza un linguaggio di scripting chiamato "Schematyc" che consente agli sviluppatori di creare logiche e interazioni di gioco. Inoltre, supporta C++ per esigenze di programmazione più avanzate.

## Formati di file utilizzati da CryENGINE

Ecco alcuni dei tipi di file più comuni associati a CryENGINE:

1. **cryproj**: file di progetto CryENGINE. Questi file memorizzano impostazioni e configurazioni specifiche del progetto per un particolare progetto di gioco.
    




















2. **.level**: i file di livello contengono dati del mondo di gioco 3D, inclusi terreno, oggetti, illuminazione e altre impostazioni specifiche del livello. I livelli sono una componente fondamentale del game design in CryENGINE.
    




















3. **.cgf**: formato della geometria dei caratteri. Questi file contengono dati di modelli 3D per personaggi, oggetti e altre risorse di gioco. I file CGF possono includere geometria, trame e dati di animazione.
    




















4. **.chrparams**: file dei parametri dei caratteri. Questi file memorizzano le impostazioni e le configurazioni per i modelli dei personaggi e le loro animazioni.
    




















5. **.dds**: formato trama DirectX. CryENGINE utilizza comunemente file DDS per archiviare texture, incluse mappe diffuse, mappe normali e altri tipi di texture.
    




















6. **.cryshader**: file shader CryENGINE. Questi file definiscono il modo in cui i materiali e gli oggetti vengono renderizzati nel mondo di gioco, specificando shader, proprietà dei materiali e altro.
    




















7. **.crytif**: file di informazioni sulla trama. Questi file memorizzano informazioni aggiuntive sulle texture, come impostazioni di compressione, mipmap e altri dettagli relativi alle texture.
    




















8. **.cdf**: file di definizione dei caratteri. I file CDF vengono utilizzati per definire le risorse dei personaggi e le loro proprietà, inclusi allegati, stati di animazione e impostazioni relative ai personaggi.
    




















9. **.dds**: CryENGINE utilizza anche file DDS (DirectDraw Surface) per varie mappe texture, come mappe normali, mappe speculari e mappe diffuse.
    




















10. **.anim**: file di animazione. Questi file memorizzano i dati di animazione per personaggi e oggetti, inclusi fotogrammi chiave, posizioni delle ossa e sequenze di animazione.
    




















11. **.xml**: i file XML possono essere utilizzati per varie configurazioni e definizioni di dati all'interno di CryENGINE, come logica di gioco, comportamento dell'IA e altro.
    




















12. **.pak**: [file PAK](/it/game/pak/) sono file di archivio utilizzati per impacchettare risorse e risorse del gioco, rendendolo più efficiente per la distribuzione e il caricamento del gioco.

## Come aprire il file CHR?

I programmi che aprono i file CHR includono

- **Crytek CryENGINE SDK** (prova gratuita) per Windows

**Sottotipo:** File di immagini 3D

## Altri file CHR

Di seguito sono riportati altri tipi di file che utilizzano l'estensione file **.chr**.

**3D**
- [CHR - File di caratteri CryENGINE](/it/3d/chr-cryengine/)
- [CHR - File di caratteri di 3ds Max](/it/3d/chr-3ds/)

**Carattere e gioco**
- [CHR - Set di caratteri Borland](/it/font/chr/)
- [CHR - Club di letteratura Doki Doki! File personaggio](/it/game/chr-doki/)

## Riferimenti
- [CryEngine](https://en.wikipedia.org/wiki/CryEngine)

