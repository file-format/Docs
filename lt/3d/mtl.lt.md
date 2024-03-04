{
   "date":"2023-10-11",
   "keywords":[
"mtl",
"mtl failą",
"mtl obj medžiagos šablono bibliotekos failas",
"Kaip atidaryti mtl failą",
"failą",
"mtl failo plėtinys",
"pratęsimas",
"failą"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"MTL failo formatas – OBJ medžiagos šablono bibliotekos failas",
   "description":"Sužinokite apie MTL OBJ medžiagų šablonų bibliotekos failų formatą ir API, kurios gali kurti ir atidaryti MTL failus.",
   "linktitle":"MTL",
   "menu":{
      "docs":{
         "identifier":"3d-mtl-lt",
         "parent":"3d"
}
},
   "lastmod":"2023-10-11"
}

## Kas yra MTL failas?

MTL failas, trumpinys **Material Template Library**, yra papildomo failo formatas, naudojamas 3D kompiuterinėje grafikoje ir modeliavime. Jis dažnai siejamas su **Wavefront OBJ failo formatu**, kuris yra įprastas 3D modelių ir su jais susijusių medžiagų bei tekstūrų saugojimo formatas.

## MTL failo formatas

**MTL failo formatas** siejamas su trimate kompiuterine grafika ir dažnai naudojamas kartu su OBJ (Wavefront .obj) failo formatu. OBJ failai apibrėžia 3D geometriją, o MTL failai apibrėžia susijusių OBJ failų medžiagų savybes.

Štai paprastas MTL failo pavyzdys:

```
newmtl MaterialName
Ka 0.6 0.6 0.6    # Ambient color
Kd 0.8 0.8 0.8    # Diffuse color
Ks 1.0 1.0 1.0    # Specular color
Ns 100            # Shininess
d  1.0            # Dissolve (transparency)
map_Kd texture.jpg  # Diffuse texture map
```

Šiame pavyzdyje:

- Ka reiškia aplinkos spalvą.
- Kd reiškia išsklaidytą spalvą.
- Ks reiškia įspūdingą spalvą.
- Ns reiškia blizgesį.
- d reiškia ištirpimą (skaidrumą).
- `map_Kd` nurodo išsklaidytą tekstūros žemėlapį.

Šios medžiagos savybės gali būti taikomos skirtingoms 3D modelio dalims, apibrėžtoms atitinkamame OBJ faile.

**MTL failas yra neprivalomas, o OBJ failus galima naudoti be susijusių MTL failų**. Tačiau naudojant MTL failus galima detaliau ir tikroviškiau atvaizduoti 3D modelius, nurodant paviršiaus savybes ir tekstūras.

## Medžiagų šablonų biblioteka

Čia yra svarbi informacija apie MTL failus:

1.  **Medžiagų apibrėžimai**: .mtl faile yra medžiagų, kurios taikomos 3D objektams atitinkamame OBJ faile, apibrėžimai. Kiekvienas medžiagos apibrėžimas nurodo įvairias savybes, tokias kaip spalva, blizgesys, skaidrumas ir tekstūros žemėlapiai.
    
2.  **Teksto formatas**: .mtl failai paprastai yra paprasto teksto failai, o tai reiškia, kad juos galima lengvai redaguoti naudojant teksto rengyklę. Kiekvienas medžiagos apibrėžimas susideda iš teiginių rinkinio ir šie teiginiai apibrėžia medžiagos atributus.
    
3.  **Tekstūros atvaizdavimas**: viena iš pagrindinių .mtl failo funkcijų yra apibrėžti, kaip tekstūros (vaizdo failai) priskiriamos 3D modelio paviršiams. Jame nurodomas tekstūros failo kelias ir kaip jis turi būti apvyniotas arba pritaikytas modeliui.
    
4.  **MTL teiginių pavyzdžiai**: štai keli teiginių pavyzdžiai, kuriuos galite rasti .mtl faile:
    
- newmtl MaterialName: tai apibrėžia naują medžiagą pavadinimu MaterialName.
- Ka rgb: medžiagos aplinkos spalva, nurodyta RGB reikšmėmis.
- Kd rgb: išsklaidyta medžiagos spalva, nurodyta RGB reikšmėmis.
- Ks rgb: ryški medžiagos spalva, nurodyta RGB reikšmėmis.
- Ns vertė: medžiagos blizgesys arba veidrodinis eksponentas.
- `map_Kd texturefile.jpg`: nurodo medžiagos išsklaidytą tekstūros žemėlapį.
5.  **Kelios medžiagos**: OBJ faile gali būti nuoroda į kelias medžiagas ir kiekviena medžiaga yra apibrėžta .mtl faile. Tai leidžia sukurti sudėtingus 3D modelius su skirtingomis medžiagomis, pritaikytomis skirtingoms dalims.
    
6.  **Suderinamumas**: .mtl failus plačiai palaiko 3D modeliavimo programinė įranga ir atvaizdavimo varikliai, todėl 3D modelius ir jų medžiagas galima perkelti iš vienos programinės įrangos į kitą.

## Kaip atidaryti MTL failą?

MTL failas yra teksto failai, todėl juos galima atidaryti naudojant bet kurį teksto rengyklę, įskaitant

- Užrašų knygelė (Windows)
- Notepad++ (Windows)
- Visual Studio kodas
- Puikus tekstas
- Atomas
– Teksto redagavimas (MacOS)

Programos, kurios atidaro arba nurodo MTL failus, apima

- Adobe Photoshop 2023
- Autodesk Maya 2023.
- MeshLab
- Cheetah3D

## Nuorodos
* [Wavefront .obj failas](https://en.wikipedia.org/wiki/Wavefront_.obj_file)


