{
  "date": "2020-08-20",
  "keywords": [
"eot failą",
"eot failo formatas",
"kas yra eot failas",
"failą",
"eot pavyzdys",
"eot failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EOT – „TrueType“ šrifto failo formatas",
  "description": "Sužinokite apie EOT failo formatą ir API, kad sukurtumėte ir atidarytumėte EOT failus.",
  "linktitle": "EOT",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-eo-ltt"
}
},
  "lastmod": "2020-10-21"
}

## Kas yra EOT failas?

Failas su plėtiniu .eot yra OpenType šriftas, įdėtas į dokumentą. Jie dažniausiai naudojami žiniatinklio failuose, tokiuose kaip tinklalapis. Jį sukūrė Microsoft ir palaiko Microsoft produktai, įskaitant PowerPoint pristatymo failą [.pps](/presentation/pps/). Failas nėra pagrindinis naudojimas ir yra tarsi lydimasis dokumentas su pagrindiniu dokumentu arba tinklalapiu. Panašiai kaip OTF šriftai, EOT palaiko ir Postscript, ir TrueType kontūrus, skirtus glifams. EOT failai yra mažesnio dydžio dėl to, kad jie suglaudinami naudojant LZ glaudinimą. EOT naudoja Microsoft įrankį, kad sukurtų šriftą iš esamų TTF/OTF šriftų.

## Trumpa istorija

EOT šriftas buvo pateiktas W3C 2007 m. kaip CSS3 dalis, tačiau dėl jo reikalavimų būti nuolat įdiegtam nuotolinėje sistemoje tapo jo atmetimo priežastimi. Jis buvo pakartotinai pateiktas 2008 m. kovo mėn., tačiau W3C galiausiai pasirinko [Web Font Format](/font/woff/) (WOFF), kuris tada buvo standartizuotas.

## EOT failo formatas

Išsamią EOT failo formato informaciją galite rasti adresu [W3 submission page](https://www.w3.org/Submission/EOT/#FileFormat). Čia išsamiai aprašoma šio šrifto formato naudojama struktūra. EOT sudaro viena EMBEDDEDFONT struktūra, kuri suteikia pakankamai pagrindinės informacijos apie hte šrifto pavadinimą ir palaikomus simbolius. Šios informacijos supakavimas leidžia naudotojo agentams neišpakuoti, išspausti arba neįdiegti šrifto, jei jis jau yra įrenginyje.

### EMBEDDEDFONT Struktūra
EMBEDDEDFONT struktūra buvo peržiūrėta tris kartus, o kiekvienos peržiūros pabaigoje struktūros pabaigoje buvo pridėta papildomų duomenų. Paskutinė EMBEDDEDFONT struktūros peržiūra yra tokia, kaip parodyta toliau.

|Duomenų tipas|Įrašo pavadinimas|Aprašymas|
---|---|---|
|unsigned long|EOTSize|Bendras struktūros ilgis baitais (įskaitant eilutės ir šrifto duomenis)|
|unsigned long|FontDataSize|OpenType šrifto ilgis (FontData) baitais|
|unsigned long|Versija|Šio formato versijos numeris - 0x00020002|
|nepasirašytas ilgas|Vėliavos|Apdorojamos vėliavėlės|
|byte[10]|FontPANOSE|Šio šrifto PANOSE reikšmė – žr. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#pan|
|byte|Charset|Windows sistemoje tai gaunama iš TEXTMETRIC.tmCharSet. Ši reikšmė nurodo šrifto simbolių rinkinį. DEFAULT_CHARSET (0x01) nerodo pirmenybės. – Žr. https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Italic|Jei ITALIC bitas nustatytas OS/2.fsSelection, reikšmė bus 0x01 – žr. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fss|
|unsigned long|Weight|Šio šrifto svorio reikšmė – žr. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#wtc|
|unsigned short|fsType|Tipo vėliavėlės, teikiančios informaciją apie įterpimo leidimus – žr. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fst|
|nepasirašytas trumpas|MagicNumber|Magiškas EOT failo numeris – 0x504C. Naudojamas patikrinti, ar nėra duomenų sugadinimo.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (bitai 0–31) – žr. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (32–63 bitai) – žr. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (64–95 bitai) – žr. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (96–127 bitai) – žr. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|CodePageRange1|CodePageRange1 (bitai 0–31) – žr. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (32–63 bitai) – žr. https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|nepasirašytas ilgas|CheckSumAdjustment|head.CheckSumAdjustment – žr. https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|nepasirašytas ilgas|Rezervuotas1|Rezervuotas – turi būti 0|
|nepasirašytas ilgas|Rezervuotas2|Rezervuotas – turi būti 0|
|nepasirašytas ilgas|Rezervuotas3|Rezervuotas – turi būti 0|
|nepasirašytas ilgas|Rezervuotas4|Rezervuotas – turi būti 0|
|unsigned short|Padding1|Padding, siekiant išlaikyti ilgą lygiavimą. Užpildymo reikšmė visada turi būti nustatyta į 0x0000.|
|unsigned short|FamilyNameSize|FamilyName masyve naudojamų baitų skaičius|
|byte|FamilyName[FamilyNameSize]|UTF-16 simbolių masyvas, kurio ilgis yra FamilyNameSize baitų. Tai anglų kalbos šriftų šeimos eilutė, rasta šrifto pavadinimo lentelėje (pavadinimo ID = 1) – žr. https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding2|Padding vertė visada turi būti nustatyta į 0x0000.|
|unsigned short|StyleNameSize|StyleName naudojamų baitų skaičius|
|byte|StyleName[StyleNameSize]|UTF-16 simbolių masyvas, kurio ilgis yra StyleNameSize baitų. Tai anglų kalbos šriftų pogrupio eilutė, rasta šrifto pavadinimo lentelėje (pavadinimo ID = 2) – žr. https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding3|Padding vertė visada turi būti nustatyta į 0x0000.|
|unsigned short|VersionNameSize|VersionName naudojamų baitų skaičius|
|baitai|VersionName[VersionNameSize]|UTF-16 simbolių masyvas, kurio ilgis yra VersionNameSize baitų. Tai anglų kalbos versijos eilutė, rasta šrifto pavadinimų lentelėje (pavadinimo ID = 5) – žr. https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding4|Padding vertė visada turi būti nustatyta į 0x0000.|
|unsigned short|FullNameSize|FullName naudojamų baitų skaičius|
|byte|FullName[FullNameSize]|UTF-16 simbolių masyvas, kurio ilgis yra FullNameSize baitų. Tai anglų kalbos viso pavadinimo eilutė, esanti šrifto pavadinimų lentelėje (pavadinimo ID = 4) – žr. https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding5|Padding vertė visada turi būti nustatyta į 0x0000.|
|unsigned short|RootStringSize|Baitų, naudojamų RootString masyvo, skaičius|
|byte|RootString[RootStringSize]|UTF-16 simbolių masyvas, kurio ilgis yra RootStringSize baitų.|
|unsigned long|RootStringCheckSum|RootString CheckSum reikšmė. Žemiau žr. algoritmą RootStringChecksum apdorojimui.|
|unsigned long|EUDCCodePage|Kodo puslapio reikšmė reikalinga EUDC šrifto palaikymui.|
|unsigned short|Padding6|Padding vertė visada turi būti nustatyta į 0x0000.|
|unsigned short|SignatureSize|Signature masyvo naudojamų baitų skaičius. Šiuo metu rezervuota ir turėtų būti nustatyta į 0x0000.|
|baitas|Parašas[SignatureSize]|Šiuo metu rezervuotas. Jei SignatureSize yra 0x0000, šio masyvo ilgis nėra.|
|nepasirašytas ilgas|EUDCFlags|Apdorojamos EUDC šrifto vėliavėlės. Įprastos reikšmės gali būti TTEMBED_XORENCRYPTDATA ir TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|Parašo masyvo naudojamų baitų skaičius.|
|baitas|EUDCFontData[EUDCFontSize]|Baitų, naudojamų EUDC šrifto duomenims, skaičius. Jei EUDCFontSize yra 0x00000000, šio masyvo ilgis nėra.|
|byte|FontData[FontDataSize]|Šio EOT failo šrifto duomenys. Duomenys gali būti suspausti arba XOR užšifruoti, kaip nurodo apdorojimo vėliavėlės.|

## Nuorodos

 * [EOT failo formatas](https://www.w3.org/Submission/EOT/)
 * [Embedded OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
 * [Šrifto įterpimas](https://en.wikipedia.org/wiki/Font_embedding)

