{
  "date": "2020-08-20",
  "keywords": [
"comhad eot",
"formáid comhaid eot",
"cad is comhad eot",
"comhad",
"sampla eot",
"síneadh comhad eot",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EOT - Formáid Comhaid Cló TrueType",
  "description": "Foghlaim faoi Formáid Chomhaid EOT agus APIs chun comhaid EOT a chruthú agus a oscailt.",
  "linktitle": "EOT",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-eo-gat"
}
},
  "lastmod": "2020-10-21"
}

## Cad is comhad EOT ann?

Is cló OpenType é comhad le síneadh .eot atá leabaithe i ndoiciméad. Úsáidtear iad seo go príomha i gcomhaid gréasáin ar nós leathanach Gréasáin. Chruthaigh Microsoft é agus tacaítear leis ó Microsoft Products lena n-áirítear comhad léirithe PowerPoint [.pps](/presentation/pps/). Níl an comhad ina phríomhúsáid agus is cineál doiciméad é a ghabhann leis an bpríomhdhoiciméad nó leis an leathanach gréasáin. Cosúil le clónna OTF, tacaíonn EOT le imlíne Postscript agus TrueType do na glyphs. Tá comhaid EOT níos lú i méid ar an gcúis go bhfuil siad comhbhrúite ag baint úsáide as comhbhrú LZ. Úsáideann EOT uirlis Microsoft chun cló a chruthú ó chlónna TTF/OTF atá ann cheana féin.

## Stair Ghearr

Cuireadh an cló EOT faoi bhráid W3C in 2007 mar chuid de CSS3 ach mar gheall ar a riachtanais a bheith suiteáilte go buan ar chianchóras ba chúis leis an diúltú. Cuireadh isteach arís é i Márta 2008, ach sa deireadh roghnaigh W3C [Web Font Format](/font/woff/) (WOFF) a caighdeánaíodh an uair sin.

## Formáid Chomhaid EOT

Is féidir sonraí formáid comhaid EOT a fháil ar [W3 submission page](https://www.w3.org/Submission/EOT/#FileFormat) agus mionsaothraítear an struchtúr a úsáideann an fhormáid chló seo. Is éard atá san EOT struchtúr amháin EMBEDDEDFONT a sholáthraíonn faisnéis bhunúsach go leor faoi ainm cló hte agus carachtair tacaithe. Ligeann pacáil na faisnéise seo do Ghníomhairí Úsáideora díphacáil, dí-chomhbhrú nó suiteáil an chló a sheachaint má tá sé ar an meaisín cheana féin.

### Struchtúr EMBEDDEDFONT
Rinneadh trí athbhreithniú ar struchtúr EMBEDDEDFONT, agus cuireadh sonraí breise ag deireadh an struchtúir le gach athbhreithniú. Tá an t-athbhreithniú deireanach ar struchtúr EMBEDDEDFONT léirithe thíos.

|Cineál Sonraí|Ainm Iontrála|Cur Síos|
---|---|---|
|fad gan síniú|Méid EOTS|Fad iomlán an struchtúir i mbearta (lena n-áirítear sonraí teaghrán agus cló)|
|fad gan síniú|ClómhéidData|Fad an chló OpenType (FontData) i mbearta|
|fada gan síniú|Leagan|Uimhir leagain na formáide seo - 0x00020002|
|fada gan síniú|Bratacha|Bratacha Próiseála|
|byte[10]|FontPANOSE|An luach PANOSE don chló seo - Féach https://learn.microsoft.com/en-us/typography/opentype/spec/os2#pan|
|beart|Charset|In Windows díorthaítear é seo ó TEXTMETRIC.tmCharSet. Sonraíonn an luach seo tacar carachtar an chló. Ní thugann DEFAULT_CHARSET (0x01) aon rogha le fios. - Féach https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Iodálach|Má tá an giotán don IODÁIL socraithe in OS/2.fsSelection, beidh an luach cothrom le 0x01 - Féach https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fss|
|fada gan síniú|Meáchan|An luach meáchain don chló seo - Féach https://learn.microsoft.com/en-us/typography/opentype/spec/os2#wtc|
|gearr gan síniú|fsType|Cineál bratacha a sholáthraíonn faisnéis faoi cheadanna neadaithe - Féach https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fst|
|gearr gan síniú|Uimhir Dhraíochta|Uimhir draíochta don chomhad EOT - 0x504C. Úsáidtear é chun éilliú sonraí a sheiceáil.|
|fada gan síniú|UnicodeRange1|os/2.UnicodeRange1 (giotán 0-31) - Féach https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|fada gan síniú|UnicodeRange2|os/2.UnicodeRange2 (giotán 32-63) - Féach https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|fada gan síniú|UnicodeRange3|os/2.UnicodeRange3 (giotán 64-95) - Féach https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|fada gan síniú|UnicodeRange4|os/2.UnicodeRange4 (giotán 96-127) - Féach https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|fada gan síniú|CodePageRange1|CodePageRange1 (giotán 0-31) - Féach https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|fada gan síniú|CodePageRange2|CodePageRange2 (giotán 32-63) - Féach https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|fad gan síniú|CheckSumAdjustment|head.CheckSumAdjustment - Féach https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|gan síniú fada|Forchoimeád1|Forchoimeádta - caithfidh sé a bheith 0|
|gan síniú fada|Forchoimeád2|In áirithe - caithfidh sé a bheith 0|
|gan síniú fada|Forchoimeád3|Forchoimeádta - caithfidh sé a bheith 0|
|gan síniú fada|Forchoimeád4|In áirithe - caithfidh sé a bheith 0|
|gearr gan síniú|Stadáil1|Stadáil chun ailíniú fada a choinneáil. Ní mór luach stuála a shocrú go 0x0000 i gcónaí.|
|gearr gan síniú|Méid Ainm Teaghlaigh|Líon na mbeart a úsáideann an eagar FamilyName|
|beart|Ainm Teaghlaigh[FamilyNameSize]|Eagar de charachtair UTF-16 fad beart FamilyNameSize. Seo é an teaghrán Béarla Cló Teaghlaigh atá le fáil i gclár ainmneacha na cló (ainm ID = 1) - Féach https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|gearr gan síniú|Stadáil2|Ní mór an luach stuála a shocrú go 0x0000 i gcónaí.|
|gearr gan síniú|StyleNameSize|Líon na mbeart a úsáideann an StyleName|
|beart|StyleName[StyleNameSize]|Eagar de charachtair UTF-16 fad beart StyleNameSize. Seo é an teaghrán Fotheaghlach Cló Béarla atá le fáil i gclár ainmneacha na cló (ainm ID = 2) - Féach https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|gearr gan síniú|Stadáil3|Ní mór an luach stuála a shocrú go 0x0000 i gcónaí.|
|gearr gan síniú|MéidAinm an Leagan|Líon na mbeart a úsáideann an VersionName|
|bearta|VersionName[VersionNameSize]|Eagar de charachtair UTF-16 fad beart VersionNameSize. Seo teaghrán an leagain Bhéarla atá le fáil i gclár ainmneacha na cló (ainm ID = 5) - Féach https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|gearr gan síniú|Stadáil4|Ní mór an luach stuála a shocrú go 0x0000 i gcónaí.|
|gearr gan síniú|Méid Lánainm|Líon na mbeart a úsáideann an Lánainm|
|beart|Ainm Lán[FullNameSize]|Eagar de charachtair UTF-16 fad beart FullNameSize. Seo é an teaghrán ainm iomlán Béarla atá le fáil i dtábla ainmneacha an chló (ainm ID = 4) - Féach https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|gearr gan síniú|Stadáil5|Ní mór an luach stuála a shocrú go 0x0000 i gcónaí.|
|gearr gan síniú|Méid an FhréamhString|Líon na mbeart a úsáideann an t-eagar RootString|
|beart|RootString[RootStringSize]|Eagar de charachtair UTF-16 fad beart RootStringSize.|
|fad gan síniú|RootStringCheckSum|Luach Sheiceála RootString. Féach ar algartam chun RootStringChecksum a phróiseáil thíos.|
|fada gan síniú|Leathanach Cód EUDC|Luach an chóid de dhíth le haghaidh tacaíocht cló EUDC.|
|gearr gan síniú|Stadáil6|Ní mór an luach stuála a shocrú go 0x0000 i gcónaí.|
|gearr gan síniú|Méid an Chomhartha|Líon na mbeart a úsáideann an t-eagar Sínithe. In áirithe faoi láthair agus ba cheart é a shocrú go 0x0000.|
|beart|Síniú[Méid an Chomhartha]|Áirithe faoi láthair. Más é 0x0000 an SignatureSize níl aon fhad leis an eagar seo.|
|fada gan síniú|Bratacha EUDC|Bratacha a phróiseáil don chló EUDC. Seans gurb iad na gnáthluachanna ná TTEMBED_XORENCRYPTDATA agus TTEMBED_TTCOMPRESSED.|
|fad gan síniú|EUDCFontSize|Líon na mbeart a úsáideann an t-eagar Sínithe.|
|beart|Sonraí EUDCFont[EUDCFontSize]|Líon na mbeart a úsáidtear do shonraí cló EUDC. Más é 0x00000000 an EUDCFontSize, níl aon fhad leis an eagar seo.|
|byte|FontData[FontDataSize]|Na sonraí cló don chomhad EOT seo. Is féidir na sonraí a chomhbhrúite nó XOR a chriptiú mar atá léirithe ag na bratacha próiseála.|

## Tagairtí

 * [Formáid Comhaid EOT]( https://www.w3.org/Submission/EOT/)
 * [Embedded OpenType]( https://en.wikipedia.org/wiki/Embedded_OpenType)
 * [Leabú Cló]( https://en.wikipedia.org/wiki/Font_embedding )

