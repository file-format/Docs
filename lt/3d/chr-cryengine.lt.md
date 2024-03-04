{
   "date":"2023-10-11",
   "keywords":[
"chr",
"chr failą",
"chr cryengine simbolių failas",
"kaip atidaryti chr failą",
"failą",
"chr failo plėtinys",
"pratęsimas",
"failą"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"CHR failo formatas – CryENGINE simbolių failas",
   "description":"Sužinokite apie CHR CryENGINE simbolių failo formatą ir API, kurios gali kurti ir atidaryti CHR failus.",
   "linktitle":"CHR CryENGINE",
   "menu":{
      "docs":{
         "identifier":"3d-chr-cryengine-lt",
         "parent":"3d"
}
},
   "lastmod":"2023-10-11"
}

## Kas yra CHR failas?

CHR failas CryENGINE kontekste reiškia **CryENGINE simbolių failą**. CryENGINE yra žaidimų variklis, kurį sukūrė Crytek ir šie failai naudojami simbolių modeliams ir susijusiems duomenims saugoti, kad juos būtų galima naudoti vaizdo žaidimuose ir kitose realaus laiko programose.

## CryENGINE simbolių failas

CryENGINE simbolių failą paprastai sudaro šie komponentai:

1.  **Simbolių modelis**: tai 3D simbolio modelis, įskaitant jo geometriją, tekstūras ir animacijas. Šie modeliai dažnai kuriami naudojant programinę įrangą, pvz., Autodesk Maya arba Blender, ir tada importuojami į CryENGINE.
    
2.  **Animacijos duomenys**: CryENGINE palaiko sudėtingas simbolių animacijas, todėl .chr faile gali būti įvairių animacijų, tokių kaip ėjimas, bėgimas, šokinėjimas ir kt. Šios animacijos paprastai saugomos kaip pagrindinių kadrų duomenys.
    
3.  **Informacija apie takelavimą**: takelavimas reiškia simbolių modelio skeleto struktūros kūrimo procesą, kuris leidžia modeliui pritaikyti animaciją. .chr faile gali būti informacijos apie kaulų hierarchiją ir tai, kaip simbolio tinklelis yra prijungtas prie šio skeleto.
    
4.  **Medžiagos ir tekstūros duomenys**: informacija apie medžiagas, naudojamas simbolių modeliui ir susijusiems tekstūrų žemėlapiams, gali būti įtraukta į .chr failą. CryENGINE palaiko fiziškai pagrįstą atvaizdavimą, todėl šios medžiagos gali būti gana išsamios.
    
5.  **Fizikos duomenys**: jei simbolis skirtas sąveikauti su žaidimų pasauliu, .chr faile gali būti fizinių duomenų, pvz., susidūrimo formų arba ragdoll fizikos apribojimų.
    
6.  **Konfigūracijos nustatymai**: įvairūs konfigūracijos nustatymai, susiję su veikėjo elgesiu žaidimų pasaulyje, pvz., dirbtinio intelekto elgsena ar scenarijaus įvykiai, taip pat gali būti .chr failo dalis.

## CryENGINE

CryENGINE yra galingas žaidimų variklis, kurį sukūrė Crytek, Vokietijos vaizdo žaidimų kompanija. Jis žinomas dėl savo pažangiausių grafikos galimybių ir buvo naudojamas kuriant kai kuriuos vizualiai stulbinančius ir technologiškai pažangius vaizdo žaidimus. Štai keletas pagrindinių CryENGINE funkcijų ir informacijos:

1.  **Grafika ir atvaizdavimas**: CryENGINE garsėja pažangiomis grafikos galimybėmis. Jis palaiko tokias funkcijas kaip pasaulinis apšvietimas realiuoju laiku, aukštos kokybės dinaminis apšvietimas ir šešėliai, fiziškai pagrįstas atvaizdavimas (PBR) ir didelės raiškos tekstūros. Šios funkcijos padeda sukurti vizualiai stulbinančius ir tikroviškus žaidimų pasaulius.
    
2.  **Fizikos variklis**: CryENGINE turi integruotą fizikos variklį, leidžiantį realiai sąveikauti tarp žaidimų pasaulio objektų. Jis palaiko tokias funkcijas kaip standaus kūno fizika, minkšto kūno fizika ir ragdoll fizika, todėl tinka kurti dinamišką ir įtraukią aplinką.
    
3.  **Reljefas ir augmenija**: CryENGINE suteikia įrankius, leidžiančius sukurti didelę ir detalią lauko aplinką. Jis palaiko reljefo redagavimą, augmenijos išdėstymą ir dinamines oro sistemas, todėl kūrėjai gali sukurti plačius ir tikroviškus lauko nustatymus.
    
4.  **Personažo animacija**: CryENGINE apima patikimus personažų animacijos įrankius. Jis palaiko sudėtingas simbolių sistemas, veido animaciją ir mišinio medžio sistemą, leidžiančią kūrėjams sukurti tikroviškus veikėjų judesius ir animacijas.
    
5.  **AI sistema**: variklyje yra AI sistema, leidžianti sukurti išmaniuosius NPC (ne žaidėjų personažus) ir priešo AI. Kūrėjai gali sudaryti scenarijų AI elgsenai ir sąveikai, kad sukurtų sudėtingas ir įtraukias žaidimo patirtis.
       
6.  **Scenarijus**: CryENGINE naudoja scenarijų kalbą, vadinamą Schematyc, kuri leidžia kūrėjams kurti žaidimo logiką ir sąveikas. Be to, jis palaiko C++ sudėtingesniems programavimo poreikiams.

## CryENGINE naudojami failų formatai

Štai keletas dažniausiai naudojamų failų tipų, susijusių su CryENGINE:

1.  **cryproj**: CryENGINE projekto failai. Šiuose failuose saugomi konkretaus žaidimo projekto nustatymai ir konfigūracijos.
    
2.  **.level**: lygio failuose yra 3D žaidimų pasaulio duomenų, įskaitant reljefą, objektus, apšvietimą ir kitus konkretaus lygio nustatymus. Lygiai yra pagrindinė CryENGINE žaidimo dizaino sudedamoji dalis.
    
3.  **.cgf**: simbolių geometrijos formatas. Šiuose failuose yra simbolių, objektų ir kitų žaidimo išteklių 3D modelio duomenys. CGF failuose gali būti geometrijos, tekstūrų ir animacijos duomenų.
    
4.  **.chrparams**: simbolių parametrų failai. Šiuose failuose saugomi simbolių modelių ir jų animacijų nustatymai ir konfigūracijos.
    
5.  **.dds**: DirectX tekstūros formatas. CryENGINE paprastai naudoja DDS failus, kad saugotų tekstūras, įskaitant išsklaidytus žemėlapius, įprastus žemėlapius ir kitus tekstūrų tipus.
    
6.  **.cryshader**: CryENGINE Shader failai. Šie failai apibrėžia, kaip žaidimų pasaulyje pateikiamos medžiagos ir objektai, nurodant šešėlius, medžiagų savybes ir kt.
    
7.  **.crytif**: tekstūros informacijos failas. Šiuose failuose saugoma papildoma informacija apie tekstūras, pvz., glaudinimo parametrai, mipmaps ir kita su tekstūra susijusi informacija.
    
8.  **.cdf**: simbolių apibrėžimo failas. CDF failai naudojami simbolių turtui ir jų savybėms apibrėžti, įskaitant priedus, animacijos būsenas ir su simboliais susijusius nustatymus.
    
9.  **.dds**: CryENGINE taip pat naudoja DDS (DirectDraw Surface) failus įvairiems tekstūrų žemėlapiams, tokiems kaip įprasti žemėlapiai, veidrodiniai žemėlapiai ir difuziniai žemėlapiai.
    
10.  **.anim**: animacijos failai. Šiuose failuose saugomi simbolių ir objektų animacijos duomenys, įskaitant raktinius kadrus, kaulų padėtis ir animacijos sekas.
    
11.  **.xml**: XML failai gali būti naudojami įvairioms CryENGINE konfigūracijoms ir duomenų apibrėžimams, pvz., žaidimo logikai, AI elgesiui ir kt.
    
12.  **.pak**: [PAK files](/game/pak/) yra archyviniai failai, naudojami žaidimo ištekliams ir ištekliams supakuoti, todėl jie yra veiksmingesni žaidimams platinti ir įkelti.

## Kaip atidaryti CHR failą?

Programos, kurios atidaro CHR failus, apima

- **Crytek CryENGINE SDK** (nemokama bandomoji versija), skirta Windows.

## Kiti CHR failai

Štai kiti failų tipai, kuriuose naudojamas **.chr** failo plėtinys.

**3D**
- [CHR - CryENGINE Character File](/3d/chr-cryengine/)
- [CHR - 3ds Max Characters File](/3d/chr-3ds/)

**Šriftas ir žaidimas**
- [CHR - Borland Character Set](/font/chr/)
- [CHR - Doki Doki Literature Club! Character File](/game/chr-doki/)

## Nuorodos
- [CryEngine](https://en.wikipedia.org/wiki/CryEngine)

