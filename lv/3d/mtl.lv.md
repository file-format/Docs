{
   "date":"2023-10-11",
   "keywords":[
"mtl",
"mtl failu",
"mtl obj materiāla veidnes bibliotēkas fails",
"kā atvērt mtl failu",
"failu",
"mtl faila paplašinājums",
"pagarinājumu",
"failu"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"MTL faila formāts — OBJ materiāla veidnes bibliotēkas fails",
   "description":"Uzziniet par MTL OBJ materiālu veidņu bibliotēkas failu formātu un API, kas var izveidot un atvērt MTL failus.",
   "linktitle":"MTL",
   "menu":{
      "docs":{
         "identifier":"3d-mtl-lv",
         "parent":"3d"
}
},
   "lastmod":"2023-10-11"
}

## Kas ir MTL fails?

MTL fails, saīsinājums no **Material Template Library**, ir pavadfaila formāts, ko izmanto 3D datorgrafikā un modelēšanā. Tas bieži tiek saistīts ar **Wavefront OBJ faila formātu**, kas ir izplatīts formāts 3D modeļu un ar tiem saistīto materiālu un faktūru glabāšanai.

## MTL faila formāts

**MTL faila formāts** ir saistīts ar 3D datorgrafiku un bieži tiek izmantots kopā ar OBJ (Wavefront .obj) faila formātu. OBJ faili nosaka 3D ģeometriju, un MTL faili nosaka saistīto OBJ failu materiāla īpašības.

Šeit ir vienkāršs MTL faila piemērs:

```
newmtl MaterialName
Ka 0.6 0.6 0.6    # Ambient color
Kd 0.8 0.8 0.8    # Diffuse color
Ks 1.0 1.0 1.0    # Specular color
Ns 100            # Shininess
d  1.0            # Dissolve (transparency)
map_Kd texture.jpg  # Diffuse texture map
```

Šajā piemērā:

- Ka apzīmē apkārtējās vides krāsu.
- Kd apzīmē izkliedētu krāsu.
- Ks apzīmē spožu krāsu.
- `Ns` apzīmē spīdumu.
- d apzīmē izšķīšanu (caurspīdīgumu).
- `map_Kd' norāda izkliedētās tekstūras karti.

Šīs materiāla īpašības var izmantot dažādām 3D modeļa daļām, kas definētas attiecīgajā OBJ failā.

**MTL fails nav obligāts, un OBJ failus var izmantot bez saistītajiem MTL failiem**. Tomēr MTL failu izmantošana ļauj detalizētāk un reālistiskāk atveidot 3D modeļus, norādot virsmas īpašības un faktūras.

## Materiālu veidņu bibliotēka

Šeit ir svarīga informācija par MTL failiem:

1.  **Materiālu definīcijas**: failā .mtl ir ietvertas definīcijas materiāliem, kas tiek lietoti 3D objektiem attiecīgajā OBJ failā. Katra materiāla definīcija nosaka dažādas īpašības, piemēram, krāsu, spīdumu, caurspīdīgumu un tekstūras kartes.
    
2.  **Teksta formāts**: .mtl faili parasti ir vienkārša teksta faili, kas nozīmē, ka tos var viegli rediģēt, izmantojot teksta redaktoru. Katra materiāla definīcija sastāv no apgalvojumu kopas, un šie apgalvojumi definē materiāla atribūtus.
    
3.  **Tektūras kartēšana**: viena no galvenajām .mtl faila funkcijām ir definēt, kā tekstūras (attēlu faili) tiek kartētas uz 3D modeļa virsmām. Tas norāda tekstūras faila ceļu un to, kā tas jāiesaiņo vai jāpiemēro modelim.
    
4.  **MTL paziņojumu piemēri**: šeit ir daži paziņojumu piemēri, ko varat atrast failā .mtl.
    
- newmtl MaterialName: tas definē jaunu materiālu ar nosaukumu MaterialName.
- Ka rgb: materiāla apkārtējā krāsa, kas norādīta RGB vērtībās.
- Kd rgb: materiāla difūzā krāsa, kas norādīta RGB vērtībās.
- Ks rgb: materiāla spoža krāsa, kas norādīta RGB vērtībās.
- Ns vērtība: materiāla spīdums vai spožuma eksponents.
- `map_Kd texturefile.jpg`: norāda materiāla difūzās tekstūras karti.
5.  **Vairāki materiāli**: OBJ failā var būt atsauces uz vairākiem materiāliem, un katrs materiāls ir definēts failā .mtl. Tas ļauj izveidot sarežģītus 3D modeļus ar dažādiem materiāliem, kas pielietoti dažādām daļām.
    
6.  **Saderība**: .mtl failus plaši atbalsta 3D modelēšanas programmatūra un renderēšanas programmas, kas ļauj pārsūtīt 3D modeļus un to materiālus starp dažādām lietojumprogrammām.

## Kā atvērt MTL failu?

MTL fails ir teksta faili, tāpēc tos var atvērt ar jebkuru teksta redaktoru, ieskaitot

- Notepad (Windows)
- Notepad++ (Windows)
- Visual Studio kods
- Cildens teksts
- Atoms
- TextEdit (macOS)

Programmas, kas atver MTL failus vai atsaucas uz tiem, ietver

- Adobe Photoshop 2023
- Autodesk Maya 2023
- MeshLab
- Cheetah3D

## Atsauces
* [Wavefront .obj fails](https://en.wikipedia.org/wiki/Wavefront_.obj_file)


