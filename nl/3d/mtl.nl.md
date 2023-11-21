{
"date":"2023-10-11",
   "keywords":[
"mtl",
"mtl-bestand",
"mtl obj materiaalsjabloonbibliotheekbestand",
"hoe een mtl-bestand te openen",
"bestand",
"mtl-bestandsextensie",
"verlenging",
"bestand"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title":"MTL-bestandsindeling - OBJ-materiaalsjabloonbibliotheekbestand",
   "description":"Meer informatie over de MTL OBJ Material Template Library-bestandsindeling en API's die MTL-bestanden kunnen maken en openen.",
"linktitle":"MTL",
   "menu":{
      "docs":{
         "identifier":"3d-mtl",
"parent":"3d"
}
},
"lastmod":"2023-10-11"
}

## Wat is een MTL-bestand?

MTL-bestand, een afkorting van **Material Template Library**, is een begeleidend bestandsformaat dat wordt gebruikt in 3D-computergraphics en -modellering. Het wordt vaak geassocieerd met het **Wavefront OBJ-bestandsformaat**, een gebruikelijk formaat voor het opslaan van 3D-modellen en de bijbehorende materialen en texturen.

## Materiaalsjabloonbibliotheek

Hier vindt u belangrijke informatie over MTL-bestanden:

1. **Materiaaldefinities**: het ".mtl"-bestand bevat definities voor materialen die worden toegepast op 3D-objecten in het overeenkomstige OBJ-bestand. Elke materiaaldefinitie specificeert verschillende eigenschappen, zoals kleur, glans, transparantie en textuurkaarten.
    





2. **Op tekst gebaseerd formaat**: ".mtl"-bestanden zijn doorgaans platte tekstbestanden, wat betekent dat ze gemakkelijk kunnen worden bewerkt met een teksteditor. Elke materiaaldefinitie bestaat uit een reeks uitspraken en deze uitspraken definiëren de eigenschappen van het materiaal.
    





3. **Textuurtoewijzing**: Een van de essentiële functies van een ".mtl"-bestand is het definiëren hoe texturen (afbeeldingsbestanden) worden toegewezen aan de oppervlakken van het 3D-model. Het specificeert het pad van het textuurbestand en hoe het moet worden ingepakt of op het model moet worden toegepast.
    





4. **Voorbeeld van MTL-instructies**: Hier zijn enkele voorbeeldinstructies die u mogelijk in een ".mtl"-bestand tegenkomt:
    





- `newmtl MaterialName`: Dit definieert nieuw materiaal met de naam "MaterialName."
- `Ka rgb`: omgevingskleur van het materiaal, gespecificeerd in RGB-waarden.
- `Kd rgb`: Diffuse kleur van materiaal, gespecificeerd in RGB-waarden.
- `Ks rgb`: Spiegelende kleur van het materiaal, gespecificeerd in RGB-waarden.
- `Ns-waarde`: Glans of spiegelende exponent van materiaal.
- `map_Kd texturefile.jpg`: Specificeert diffuse textuurkaart voor materiaal.
5. **Meerdere materialen**: een OBJ-bestand kan naar meerdere materialen verwijzen en elk materiaal wordt gedefinieerd in het ".mtl"-bestand. Dit maakt complexe 3D-modellen mogelijk waarbij verschillende materialen op verschillende onderdelen worden toegepast.
    





6. **Compatibiliteit**: ".mtl"-bestanden worden breed ondersteund door 3D-modelleringssoftware en rendering-engines, waardoor het mogelijk wordt om 3D-modellen en hun materialen over te dragen tussen verschillende softwaretoepassingen.

## Hoe open je een MTL-bestand?

MTL-bestanden zijn op tekst gebaseerde bestanden, dus ze kunnen met elke teksteditor worden geopend, inclusief

- Kladblok (Windows)
- Kladblok++ (Windows)
- Visuele studiocode
- Sublieme tekst
- Atoom
- Teksteditor (macOS)

Programma's die MTL-bestanden openen of ernaar verwijzen, omvatten

- Adobe Photoshop 2023
- Autodesk Maya 2023
- MeshLab
- Cheetah3D

**Subtype:** 3D-beeldbestanden

## Referenties
* [Wavefront .obj-bestand](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

