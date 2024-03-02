{
   "date":"2023-10-11",
   "keywords":[
"mtl",
"comhad mtl",
"Comhad leabharlainne ábhar mtl obj",
"Conas a oscailt comhad mtl",
"comhad",
"síneadh comhad mtl",
"síneadh",
"comhad"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"Formáid Chomhaid MTL - Comhad Leabharlainne Teimpléad Ábhar OBJ",
   "description":"Foghlaim faoi MTL OBJ Formáid comhaid Leabharlainne Teimpléad Ábhar agus APIs is féidir a chruthú agus a oscailt comhaid MTL.",
   "linktitle":"MTL",
   "menu":{
      "docs":{
         "identifier":"3d-mtl-ga",
         "parent":"3d"
}
},
   "lastmod":"2023-10-11"
}

## Cad is comhad MTL ann?

Comhad MTL, gearr do **Leabharlann Teimpléid Ábhar**, is formáid comhaid chompánach a úsáidtear i ngrafaicí agus samhaltú ríomhaire 3D. Is minic a bhaineann sé le **Formáid comhaid Wavefront OBJ**, atá ina fhormáid choiteann chun samhlacha 3D agus na hábhair agus na huigeachtaí a bhaineann leo a stóráil.

## Formáid Comhaid MTL

Baineann an **formáid comhaid MTL** le grafaicí ríomhaire 3D agus is minic a úsáidtear í in éineacht le formáid comhaid OBJ (Wavefront .obj). Sainmhíníonn comhaid OBJ céimseata 3D, agus sainíonn comhaid MTL airíonna ábhartha do na comhaid OBJ a bhaineann leo.

Seo sampla simplí de chomhad MTL:

```
newmtl MaterialName
Ka 0.6 0.6 0.6    # Ambient color
Kd 0.8 0.8 0.8    # Diffuse color
Ks 1.0 1.0 1.0    # Specular color
Ns 100            # Shininess
d  1.0            # Dissolve (transparency)
map_Kd texture.jpg  # Diffuse texture map
```

Sa sampla seo:

- Seasann `Ka` dath comhthimpeallach.
- Léiríonn `Kd` dath idirleata.
- Léiríonn `Ks` dath amhantrach.
- Seasann `Ns` shininess.
- Seasann `d` thuaslagadh (trédhearcacht).
- Sonraíonn `mapa_Kd` an léarscáil uigeachta idirleata.

Is féidir na hairíonna ábhartha seo a chur i bhfeidhm ar chodanna éagsúla den mhúnla 3D atá sainithe sa chomhad OBJ comhfhreagrach.

**Tá comhad MTL roghnach agus is féidir comhaid OBJ a úsáid gan na comhaid MTL gaolmhara**. Mar sin féin, trí úsáid a bhaint as comhaid MTL is féidir samhlacha 3D a dhéanamh níos mionsonraithe agus níos réadúla trí airíonna dromchla agus uigeachtaí a shonrú.

## Leabharlann Teimpléad Ábhar

Seo eolas tábhachtach faoi chomhaid MTL:

1.  **Sainmhínithe Ábhar**: Tá sainmhínithe sa chomhad .mtl d'ábhair a chuirtear i bhfeidhm ar réada 3D sa chomhad OBJ comhfhreagrach. Sonraíonn gach sainmhíniú ábhartha airíonna éagsúla, mar shampla léarscáileanna datha, shininess, trédhearcachta agus uigeachta.
    
2.  **Formáid Téacsbhunaithe**: De ghnáth is comhaid gnáth-théacs iad comhaid .mtl, rud a chiallaíonn gur féidir iad a chur in eagar go héasca le heagarthóir téacs. Tá sraith ráiteas i ngach sainmhíniú ábhartha agus sainíonn na ráitis seo tréithe an ábhair.
    
3.  **Mapáil Uigeachta**: Ceann d’fheidhmeanna riachtanacha comhad .mtl” is ea an chaoi a ndéantar uigeachtaí (comhaid íomhá) a mhapáil ar dhromchlaí samhlacha 3D a shainiú. Sonraíonn sé cosán an chomhaid uigeachta agus conas ba cheart é a fhilleadh nó a chur i bhfeidhm ar mhúnla.
    
4.  **Ráitis MTL Samplacha**: Seo roinnt ráitis shamplacha a d’fhéadfá a fháil i gcomhad .mtl”:
    
- `newmtl MaterialName`: Sainmhíníonn sé seo ábhar nua leis an ainm MaterialName.
- `Ka rgb`: Dath comhthimpeallach an ábhair, sonraithe i luachanna RGB.
- `Kd rgb`: Dath idirleata an ábhair, sonraithe i luachanna RGB.
- `Ks rgb`: Dath iontach an ábhair, sonraithe i luachanna RGB.
- `Ns luach`: Shinness nó easpónant specular ábhair.
- `map_Kd texturefile.jpg`: Sonraíonn sé léarscáil uigeachta idirleata don ábhar.
5.  **Ábhair Il**: Is féidir le comhad OBJ tagairt a dhéanamh d’ilábhair agus sainmhínítear gach ábhar laistigh de chomhad .mtl”. Ligeann sé seo samhlacha casta 3D le hábhair éagsúla curtha i bhfeidhm ar chodanna éagsúla.
    
6.  **Comhoiriúnacht**: tacaítear go forleathan le comhaid .mtl ó bhogearraí samhaltaithe 3D agus innill rindreála, rud a fhágann gur féidir samhlacha 3D agus a n-ábhar a aistriú idir feidhmchláir éagsúla bogearraí.

## Conas comhad MTL a oscailt?

Is comhaid téacs-bhunaithe iad comhaid MTL, ionas gur féidir iad a oscailt le haon eagarthóir téacs lena n-áirítear

- Notepad (Windows)
- Notepad++ (Windows)
- Cód Stiúideo Amharc
- Téacs sublime
- Adamh
- TextEdit (macOS)

Áirítear le cláir a osclaíonn nó a thagraíonn comhaid MTL

- Adobe photoshop 2023
- Autodesk Maya 2023
- MeshLab
- Cheetah 3D

## Tagairtí
* [Comhad Wavefront .obj]( https://en.wikipedia.org/wiki/Wavefront_.obj_file)


