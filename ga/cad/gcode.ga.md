{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"Comhad GCODE - Cad is comhad .gcode ann agus conas é a oscailt?",
   "description":"Foghlaim faoi fhormáid comhaid GCODE agus APInna ar féidir leo comhaid GCODE a chruthú agus a oscailt.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-ga",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## Cad is comhad GCODE ann?

Is comhad gnáth-théacs é **comhad GCODE** ina bhfuil treoracha chun meaisín-uirlisí ríomhairithe agus printéirí 3D a rialú; Is teanga é G-cód, nó Cód Geoiméadrach, a úsáidtear chun gluaiseachtaí agus gníomhartha meaisíní **CNC (Rialú Uimhriúil Ríomhaireachta)** a rialú; I measc na meaisíní CNC tá meaisíní muilleoireachta, deileanna, ródairí agus printéirí 3D.

Scríobhtar orduithe G-chód i gcomhréir ar leith arb é atá ann de ghnáth litreacha agus uimhreacha; tugann gach ordú treoir don mheaisín gníomh sonrach a dhéanamh mar uirlis a bhogadh go dtí suíomh áirithe, uirlis a athrú nó luas a choigeartú.

Is minic a ghineann bogearraí **CAM (Déantúsaíocht Ríomhchuidithe)** G-cód; Glacann bogearraí CAM samhail 3D nó dearadh 2T agus gineann siad cosáin uirlisí comhfhreagracha agus treoracha G-chód; luchtaítear an comhad G-chód ansin isteach i meaisín CNC nó printéir 3D lena chur i gcrích.

De ghnáth bíonn iarmhír comhaid .nc nó .gcode ag comhaid G-chód mar shampla, program.nc nó print.gcode.

## Struchtúr Comhad GCODE:

Comhaid gnáth-théacs is ea comhaid GCODE agus bíonn ordú sonrach i ngach líne; Cuimsíonn na horduithe seo ó ghluaiseacht an mheaisín a rialú go dtí teocht, luas agus paraiméadair eile atá ríthábhachtach chun réad a dhéanamh a choigeartú.

Baineann comhréir GCODE le teaglaim de litreacha agus uimhreacha; léiríonn gach ceann acu gníomh nó paraiméadar ar leith; I measc na n-orduithe coitianta tá G0 agus G1 le haghaidh gluaiseachta, M3 agus M5 le haghaidh rialú fearsaidí, agus S agus F le haghaidh coigeartuithe ráta luais agus beatha faoi seach.

## Giniúint GCODE:

Déanann bogearraí slisnithe ar nós **Simplify3D** agus **Slic3r**, líníochtaí Dearaidh Ríomhchuidithe (CAD) a aistriú go GCODE; Úsáidtear bogearraí CAD chun samhlacha 3D a chruthú, a onnmhairítear ansin i bhformáidí cosúil le STL; tógann na bogearraí slisnithe na samhlacha seo agus gineann siad comhad GCODE ina sonraítear sonraí mar airde ciseal, luas priontála, agus socruithe teochta.

## GCODE Sampla

Seo sampla simplí de G-chód le haghaidh meaisín CNC a bhogadh:

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## Conas comhad GCODE a oscailt?

Chun comhad G-cód a oscailt is féidir leat cineálacha éagsúla bogearraí a úsáid ag brath ar do chuid riachtanas.

Má ghin tú G-cód le haghaidh printéir 3D; is féidir leat é a oscailt ag baint úsáide as bogearraí a tháinig le do printéir 3D nó bogearraí slicing tiomnaithe; I measc na samplaí tá **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** nó **Repetier-Host**; is minic a bhíonn comhéadan atá éasca le húsáid ag na cláir seo a ligeann duit G-cód a luchtú agus a shamhlú.

Is gnáth-théacs comhaid GCODE ionas gur féidir leat iad a oscailt le haon eagarthóir téacs; I measc na n-eagarthóirí téacs coitianta tá ** Notepad (ar Windows)**, **TextEdit (ar macOS)**, nó **Gedit (ar Linux)**; go simplí **cliceáil ar dheis** ar an gcomhad G-cód, roghnaigh **Oscail le,** agus roghnaigh eagarthóir téacs.

