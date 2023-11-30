{
"datum":"2023-10-11",
   "keywords":[
"mtl",
"mtl-fil",
"mtl obj material mall biblioteksfil",
"hur man öppnar en mtl-fil",
"fil",
"mtl filtillägg",
"förlängning",
"fil"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"utkast":"falskt",
"toc":true,
"title":"MTL-filformat - OBJ-materialmallbiblioteksfil",
   "description":"Lär dig om MTL OBJ Material Template Library filformat och API:er som kan skapa och öppna MTL-filer.",
"linktitle":"MTL",
   "menu":{
      "docs":{
         "identifier":"3d-mtl",
         "parent":"3d"
}
},
"lastmod":"2023-10-11"
}

## Vad är MTL fil?

MTL-fil, förkortning för **Material Template Library**, är ett kompletterande filformat som används i 3D-datorgrafik och -modellering. Det är ofta associerat med **Wavefront OBJ-filformat**, vilket är vanligt format för att lagra 3D-modeller och deras tillhörande material och texturer.

## Material mallbibliotek

Här är viktig information om MTL-filer:

1. **Materialdefinitioner**: ".mtl"-filen innehåller definitioner för material som tillämpas på 3D-objekt i motsvarande OBJ-fil. Varje materialdefinition specificerar olika egenskaper, såsom färg, glans, transparens och texturkartor.
    





2. **Textbaserat format**: ".mtl"-filer är vanligtvis vanliga textfiler, vilket innebär att de enkelt kan redigeras med textredigerare. Varje materialdefinition består av en uppsättning uttalanden och dessa uttalanden definierar materialets attribut.
    





3. **Texturmappning**: En av de viktigaste funktionerna för en ".mtl"-fil är att definiera hur texturer (bildfiler) mappas på 3D-modellens ytor. Den anger texturfilens sökväg och hur den ska lindas eller appliceras på modellen.
    





4. **Exempel på MTL-påståenden**: Här är några exempelpåståenden du kan hitta i en ".mtl"-fil:
    





- `newmtl MaterialName`: Detta definierar nytt material med namnet "MaterialName."
- `Ka rgb`: Omgivande färg på material, specificerad i RGB-värden.
- `Kd rgb`: Diffus färg på materialet, specificerad i RGB-värden.
- `Ks rgb`: Speglande färg på material, specificerad i RGB-värden.
- `Ns-värde`: Glans eller speglande exponent för materialet.
- `map_Kd texturefile.jpg`: Specificerar diffus texturkarta för material.
5. **Flera material**: En OBJ-fil kan referera till flera material och varje material definieras i ".mtl"-filen. Detta möjliggör komplexa 3D-modeller med olika material applicerade på olika delar.
    





6. **Kompatibilitet**: ".mtl"-filer stöds brett av 3D-modelleringsprogram och renderingsmotorer, vilket gör det möjligt att överföra 3D-modeller och deras material mellan olika programvaruapplikationer.

## Hur öppnar man filen MTL?

MTL-filer är textbaserade filer, så de kan öppnas med vilken textredigerare som helst inklusive

- Anteckningsblock (Windows)
- Notepad++ (Windows)
- Visual Studio Code
- Sublim text
- Atom
- TextEdit (macOS)

Program som öppnar eller refererar till MTL-filer inkluderar

- Adobe Photoshop 2023
- Autodesk Maya 2023
- MeshLab
- Cheetah3D

**SubTyp:** 3D-bildfiler

## Referenser
* [Wavefront .obj-fil](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

