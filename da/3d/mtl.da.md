{
   "date":"2023-10-11",
   "keywords":[
"mtl",
"mtl fil",
"mtl obj materiale skabelon bibliotek fil",
"hvordan man åbner en mtl-fil",
"fil",
"mtl filtypenavn",
"udvidelse",
"fil"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"MTL-filformat - OBJ-materialeskabelonbiblioteksfil",
   "description":"Lær om MTL OBJ Material Template Library filformat og API'er, der kan oprette og åbne MTL filer.",
   "linktitle":"MTL",
   "menu":{
      "docs":{
         "identifier":"3d-mtl-da",
         "parent":"3d"
}
},
   "lastmod":"2023-10-11"
}

## Hvad er en MTL fil?

MTL-fil, forkortelse for **Material Template Library**, er ledsagende filformat, der bruges i 3D-computergrafik og -modellering. Det er ofte forbundet med **Wavefront OBJ-filformat**, som er almindeligt format til lagring af 3D-modeller og deres tilknyttede materialer og teksturer.

## MTL filformat

**MTL-filformatet** er forbundet med 3D-computergrafik og bruges ofte sammen med filformatet OBJ (Wavefront .obj). OBJ-filer definerer 3D-geometri, og MTL-filer definerer materialeegenskaber for de tilknyttede OBJ-filer.

Her er et simpelt eksempel på en MTL-fil:

```
newmtl MaterialName
Ka 0.6 0.6 0.6    # Ambient color
Kd 0.8 0.8 0.8    # Diffuse color
Ks 1.0 1.0 1.0    # Specular color
Ns 100            # Shininess
d  1.0            # Dissolve (transparency)
map_Kd texture.jpg  # Diffuse texture map
```

I dette eksempel:

- `Ka` repræsenterer den omgivende farve.
- `Kd` repræsenterer diffus farve.
- `Ks` repræsenterer spejlende farve.
- `Ns` repræsenterer glans.
- `d` repræsenterer dissolve (gennemsigtighed).
- `map_Kd` specificerer det diffuse teksturkort.

Disse materialeegenskaber kan anvendes på forskellige dele af 3D-modellen defineret i den tilsvarende OBJ-fil.

**MTL-fil er valgfri, og OBJ-filer kan bruges uden tilknyttede MTL-filer**. Brug af MTL-filer giver dog mulighed for mere detaljeret og realistisk gengivelse af 3D-modeller ved at specificere overfladeegenskaber og teksturer.

## Materiale skabelonbibliotek

Her er vigtig information om MTL filer:

1.  **Materialedefinitioner**: .mtl-filen indeholder definitioner for materialer, der anvendes på 3D-objekter i tilsvarende OBJ-fil. Hver materialedefinition specificerer forskellige egenskaber, såsom farve, glans, gennemsigtighed og teksturkort.
    
2.  **Tekstbaseret format**: .mtl-filer er typisk almindelige tekstfiler, hvilket betyder, at de nemt kan redigeres med teksteditor. Hver materialedefinition består af sæt udsagn, og disse udsagn definerer materialets egenskaber.
    
3.  **Teksturkortlægning**: En af de væsentlige funktioner i en .mtl-fil er at definere, hvordan teksturer (billedfiler) kortlægges på 3D-modellens overflader. Den specificerer teksturfilens sti, og hvordan den skal pakkes ind eller anvendes på modellen.
    
4.  **Eksempel på MTL-udsagn**: Her er nogle eksempler på udsagn, du kan finde i en .mtl-fil:
    
- `newmtl MaterialName`: Dette definerer nyt materiale med navnet MaterialName.
- `Ka rgb`: Omgivende farve på materialet, angivet i RGB-værdier.
- `Kd rgb`: Diffus farve på materialet, angivet i RGB-værdier.
- `Ks rgb`: Spekulær farve på materiale, angivet i RGB-værdier.
- `Ns-værdi`: Materialets glans eller spejlende eksponent.
- `map_Kd texturefile.jpg`: Specificerer diffust teksturkort for materiale.
5.  **Flere materialer**: En OBJ-fil kan referere til flere materialer, og hvert materiale er defineret i .mtl-filen. Dette giver mulighed for komplekse 3D-modeller med forskellige materialer anvendt på forskellige dele.
    
6.  **Kompatibilitet**: .mtl-filer understøttes bredt af 3D-modelleringssoftware og gengivelsesmotorer, hvilket gør det muligt at overføre 3D-modeller og deres materialer mellem forskellige softwareapplikationer.

## Hvordan åbner jeg en MTL fil?

MTL-filer er tekstbaserede filer, så de kan åbnes med enhver teksteditor, inklusive

- Notesblok (Windows)
- Notesblok++ (Windows)
- Visual Studio Code
- Sublim tekst
- Atom
- TextEdit (macOS)

Programmer, der åbner eller refererer til MTL filer inkluderer

- Adobe Photoshop 2023
- Autodesk Maya 2023
- MeshLab
- Cheetah3D

## Referencer
* [Wavefront .obj-fil](https://en.wikipedia.org/wiki/Wavefront_.obj_file)


