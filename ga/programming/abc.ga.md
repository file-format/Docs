
{
  "date": "2021-12-14",
  "keywords": [
".abc comhad",
"síneadh",
"formáid",
"Comhad Cód Beart ActionScript",
"conas comhad .abc a oscailt",
"Formáid comhaid abc saor in aisce,"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ABC - Comhad Cód ActionScript Beart",
  "description": "Foghlaim faoi cad is formáid comhaid ABC ann le sampla agus APIanna ar féidir comhaid ABC a chruthú agus a oscailt.",
  "linktitle": "ABC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ab-gac"
}
},
  "lastmod": "2021-12-14"
}

## Cad is comhad ABC ann?

Is Comhad Cód ActionScript Beart é comhad le síneadh .abc cruthaithe ag tiomsaitheoir Flash mar thoradh ar chomhaid script ActionScript a thiomsú. Déanann Meaisín Fíorúil ActionScript (AVM agus AVM2) an cód beart atá sa chomhad ABC a fhorghníomhú. Cuimsíonn an cód beart sonraí tairiseacha, treoracha ón tacar treoracha AVM2, agus cineálacha éagsúla meiteashonraí. Nuair a luchtaítear comhad ABC isteach san AVM nó san AVM2, déantar é a fhíorú. Mura gcloíonn sé le Forbhreathnú AVM2, diúltaítear dó. Is féidir comhaid ABC a oscailt in Adobe Flash Player a scoireadh i bhfad ó shin.

## Formáid Chomhaid ABC - Tuilleadh Eolais

Déantar comhaid ABC a shábháil ar diosca i bhformáid dhénártha comhaid atá inléite ag meaisíní fíorúla AVM nó AVM2. Léiríonn a struchtúr comhad inmheánach bloc cóid inrite lena sonraí seasta go léir, a thuairisceoirí cineáil, cód agus meiteashonraí.

## Struchtúr Comhad ABC

Tá struchtúr comhaid ABC mar a thaispeántar thíos.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### Réimsí Comhad ABC

|Ainm Réimse|Cur Síos|
---|---|
|mion-leagan, major_version|Is iad na luachanna a bhaineann le major_version agus minor_version na huimhreacha móra agus mionleaganacha san fhormáid abcFile.|
|constant_pool|Is struchtúr faid athraitheach é an constant_pool comhdhéanta de shlánuimhreacha, dúbailt, teaghráin, spásanna ainm, tacair ainmspáis agus ilainmneacha.|
|method_count, modh|Is é luach method_count ná líon na n-iontrálacha san eagar modhanna. Is struchtúr fad athraitheach method_info é gach iontráil san eagar modhanna.|
|metadata_count, meiteashonraí|Is é luach meiteashonraí_chuntais ná líon na n-iontrálacha san eagar meiteashonraí. Is éard atá i ngach iontráil meiteashonraí ná meiteashonraí_infostructure a mhapálann ainm chuig sraith luachanna teaghrán. |
|rang_count, mar shampla, rang|Is é luach an chomhaireamh ranga ná líon na n-iontrálacha sa chás agus na heagair ranga. |
|script_count, script|Is é luach script_count ná líon na n-iontrálacha san eagar scripte. Struchtúr script_info is ea gach iontráil scripte a shainíonn tréithe scripte amháin sa chomhad seo. |
|method_body_count, method_body|Is é luach method_body_count ná líon na n-iontrálacha san eagar method_body. Tá struchtúr fad athraitheach method_body_info i ngach method_bodyentry ina bhfuil na treoracha do mhodh nó d'fheidhm aonair.|

## Tagairtí

 * [Robust ABC (ActionScript Bytecode) [Dis-]Cóimeálaí - Github](https://github.com/CyberShadow/RABCDAsm)

