{
"date":"2023-10-11",
   "keywords":[
"chr",
"chr-bestand",
"chr cryengine-tekenbestand",
"hoe open ik een chr-bestand",
"bestand",
"chr bestandsextensie",
"verlenging",
"bestand"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title":"CHR-bestandsindeling - CryENGINE-tekenbestand",
   "description":"Leer meer over de CHR CryENGINE-tekenbestandsindeling en API's waarmee CHR-bestanden kunnen worden gemaakt en geopend.",
"linktitle":"CHR CryENGINE",
   "menu":{
      "docs":{
         "identifier":"3d-chr-cryengine",
"parent":"3d"
}
},
"lastmod":"2023-10-11"
}

## Wat is een CHR-bestand?

CHR-bestand in de context van CryENGINE verwijst naar een **CryENGINE-tekenbestand**. CryENGINE is een game-engine ontwikkeld door Crytek en deze bestanden worden gebruikt voor het opslaan van karaktermodellen en bijbehorende gegevens voor gebruik in videogames en andere realtime toepassingen.

## CryENGINE-tekenbestand

Een CryENGINE-tekenbestand bevat doorgaans de volgende componenten:

1. **Karaktermodel**: dit is een 3D-karaktermodel, inclusief de geometrie, texturen en animaties. Deze modellen worden vaak gemaakt met software als Autodesk Maya of Blender en vervolgens geïmporteerd in CryENGINE.
    




















2. **Animatiegegevens**: CryENGINE ondersteunt complexe animaties voor karakters, dus het ".chr"-bestand kan verschillende animaties bevatten, zoals lopen, rennen, springen en meer. Deze animaties worden doorgaans opgeslagen als keyframegegevens.
    




















3. **Rigging-informatie**: Rigging verwijst naar het proces van het creëren van een skeletstructuur voor het karaktermodel, waardoor animaties op het model kunnen worden toegepast. Het ".chr"-bestand kan informatie bevatten over de bothiërarchie en hoe de mesh van het personage met dit skelet is verbonden.
    




















4. **Materiaal- en textuurgegevens**: Informatie over materialen die worden gebruikt in het karaktermodel en de bijbehorende textuurkaarten kan worden opgenomen in het ".chr"-bestand. CryENGINE ondersteunt fysiek gebaseerde weergave, dus deze materialen kunnen behoorlijk gedetailleerd zijn.
    




















5. **Fysische gegevens**: als het personage bedoeld is om te communiceren met de gamewereld, kan het ".chr"-bestand natuurkundige gegevens bevatten, zoals botsingsvormen of beperkingen voor de ragdoll-fysica.
    




















6. **Configuratie-instellingen**: Verschillende configuratie-instellingen die verband houden met het gedrag van personages in de gamewereld, zoals AI-gedrag of scriptgebeurtenissen, kunnen ook deel uitmaken van het ".chr"-bestand.

## CryENGINE

CryENGINE is een krachtige game-engine ontwikkeld door Crytek, een Duits videogamebedrijf. Het staat bekend om zijn geavanceerde grafische mogelijkheden en is gebruikt om een aantal visueel verbluffende en technologisch geavanceerde videogames te maken. Hier zijn enkele belangrijke functies en informatie over CryENGINE:

1. **Grafiek en weergave**: CryENGINE staat bekend om zijn geavanceerde grafische mogelijkheden. Het ondersteunt functies zoals realtime globale verlichting, hoogwaardige dynamische verlichting en schaduwen, fysiek gebaseerde weergave (PBR) en texturen met hoge resolutie. Deze functies dragen bij aan het creëren van visueel verbluffende en realistische spelwerelden.
    




















2. **Physics Engine**: CryENGINE bevat een ingebouwde fysica-engine die realistische interacties tussen objecten in de gamewereld mogelijk maakt. Het ondersteunt functies zoals rigide lichaamsfysica, zachte lichaamsfysica en ragdoll-fysica, waardoor het geschikt is voor het creëren van dynamische en meeslepende omgevingen.
    




















3. **Terrein en vegetatie**: CryENGINE biedt hulpmiddelen voor het creëren van uitgestrekte en gedetailleerde buitenomgevingen. Het ondersteunt terreinbewerking, plaatsing van vegetatie en dynamische weersystemen, waardoor ontwikkelaars uitgestrekte en realistische buitenomgevingen kunnen creëren.
    




















4. **Characteranimatie**: CryENGINE bevat robuuste tools voor karakteranimatie. Het ondersteunt complexe personage-rigs, gezichtsanimatie en een blend tree-systeem waarmee ontwikkelaars levensechte karakterbewegingen en animaties kunnen creëren.
    




















5. **AI-systeem**: De engine beschikt over een AI-systeem waarmee intelligente NPC's (niet-spelerpersonages) en vijandelijke AI kunnen worden gemaakt. Ontwikkelaars kunnen AI-gedrag en -interacties scripten om uitdagende en meeslepende gameplay-ervaringen te creëren.
       





















6. **Scripting**: CryENGINE gebruikt scripttaal genaamd "Schematyc" waarmee ontwikkelaars gameplay-logica en interacties kunnen creëren. Bovendien ondersteunt het C++ voor meer geavanceerde programmeerbehoeften.

## Bestandsformaten gebruikt door CryENGINE

Hier zijn enkele veelvoorkomende bestandstypen die verband houden met CryENGINE:

1. **cryproj**: CryENGINE-projectbestanden. Deze bestanden slaan projectspecifieke instellingen en configuraties op voor een bepaald gameproject.
    




















2. **.level**: Niveaubestanden bevatten 3D-spelwereldgegevens, inclusief terrein, objecten, verlichting en andere niveauspecifieke instellingen. Niveaus zijn een fundamenteel onderdeel van het spelontwerp in CryENGINE.
    




















3. **.cgf**: Tekengeometrie-indeling. Deze bestanden bevatten 3D-modelgegevens voor personages, objecten en andere spelmiddelen. CGF-bestanden kunnen geometrie-, texturen- en animatiegegevens bevatten.
    




















4. **.chrparams**: tekenparameterbestanden. Deze bestanden slaan instellingen en configuraties op voor personagemodellen en hun animaties.
    




















5. **.dds**: DirectX-textuurformaat. CryENGINE gebruikt gewoonlijk DDS-bestanden om texturen op te slaan, inclusief diffuse kaarten, normale kaarten en andere textuurtypen.
    




















6. **.cryshader**: CryENGINE Shader-bestanden. Deze bestanden definiëren hoe materialen en objecten worden weergegeven in de gamewereld, waarbij shaders, materiaaleigenschappen en meer worden gespecificeerd.
    




















7. **.crytif**: textuurinformatiebestand. Deze bestanden slaan aanvullende informatie op over texturen, zoals compressie-instellingen, mipmaps en andere textuurgerelateerde details.
    




















8. **.cdf**: tekendefinitiebestand. CDF-bestanden worden gebruikt om karaktermiddelen en hun eigenschappen te definiëren, inclusief bijlagen, animatiestatussen en karaktergerelateerde instellingen.
    




















9. **.dds**: CryENGINE gebruikt ook DDS-bestanden (DirectDraw Surface) voor verschillende textuurkaarten, zoals normale kaarten, spiegelende kaarten en diffuse kaarten.
    




















10. **.anim**: animatiebestanden. Deze bestanden slaan animatiegegevens op voor personages en objecten, inclusief keyframes, botposities en animatiesequenties.
    




















11. **.xml**: XML-bestanden kunnen worden gebruikt voor verschillende configuraties en datadefinities binnen CryENGINE, zoals gamelogica, AI-gedrag en meer.
    




















12. **.pak**: [PAK-bestanden](/nl/game/pak/) zijn archiefbestanden die worden gebruikt om game-items en -bronnen te verpakken, waardoor het efficiënter wordt voor de distributie en het laden van games.

## Hoe open je een CHR-bestand?

Programma's die CHR-bestanden openen, omvatten

- **Crytek CryENGINE SDK** (gratis proefversie) voor Windows

**Subtype:** 3D-beeldbestanden

## Andere CHR-bestanden

Hier volgen andere bestandstypen die de bestandsextensie **.chr** gebruiken.

**3D**
- [CHR - CryENGINE-tekenbestand](/nl/3d/chr-cryengine/)
- [CHR - 3ds Max. tekenbestand](/nl/3d/chr-3ds/)

**Lettertype en spel**
- [CHR - Borland-tekenset](/nl/font/chr/)
- [CHR - Doki Doki Literatuurclub! Karakterbestand](/nl/game/chr-doki/)

## Referenties
- [CryEngine](https://en.wikipedia.org/wiki/CryEngine)

