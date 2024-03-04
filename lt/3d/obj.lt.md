{
  "date": "2019-10-11",
  "keywords": [
"obj failą",
"obj failo formatas",
"kas yra obj failas",
"failą",
"obj pavyzdys",
"obj failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OBJ failo formatas",
  "description": "Sužinokite apie OBJ failo formatą ir API, kurios gali atidaryti ir kurti OBJ failus.",
  "linktitle": "OBJ",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-ob-ltj"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra OBJ failas?

**OBJ** failus naudoja Wavefront Advanced Visualizer programa geometriniams objektams apibrėžti ir saugoti. Per OBJ failus galima perduoti geometrinius duomenis atgal ir pirmyn. OBJ formatu palaiko tiek daugiakampę geometriją, kaip taškai, linijos, tekstūros viršūnės, paviršiai ir laisvos formos geometrija (kreivės ir paviršiai). Šis formatas nepalaiko animacijos ar informacijos, susijusios su šviesa ir scenų padėtimi.

OBJ failas paprastai yra galutinis 3D modeliavimo proceso produktas, sugeneruotas naudojant CAD (kompiuterinį projektavimą). Numatytoji viršūnių saugojimo tvarka yra prieš laikrodžio rodyklę, vengiant aiškaus veido normalių deklaravimo. Nors OBJ failai komentarų eilutėje deklaruoja mastelio informaciją, OBJ koordinatėms nebuvo deklaruoti jokie vienetai.

## 3D OBJ formato istorija

Wavefront Technologies created OBJ file format for its Advanced Visualizer application to store geometric objects and 3D data. Its version 2.11 is superseded by a newly documented version 3. Failo formatas yra atviras ir jį įdiegė kiti pardavėjai savo 3D grafikos programai. Wavefront Technologies išlaikė šį failo formatą atviro kodo ir neutralų.

## OBJ failo formatas

3D objektuose paviršiaus geometrijos kodavimas yra sudėtingas darbas, kurį labai gerai atliko OBJ failo formatas. Šis formatas yra gana universalus, nes siūlo daugybę pasirinkimų, kaip koduoti paviršiaus geometriją. Toliau pateikiami trys leidžiami formatai, turintys savo privalumų ir trūkumų:

### Teseliacija su daugiakampiais paviršiais

OBJ failo formatas leidžia vartotojui sudaryti 3D modelio paviršių, naudojant paprastas arba sudėtingas geometrines figūras. Modelio paviršiaus geometrijos koduotėje faile saugomos kiekvieno daugiakampio viršūnės ir normaliosios. Nors teseliacija padidina modelio šiurkštumą, tačiau būtina atrasti teisingą failo dydžio ir spausdinimo kokybės pusiausvyrą.

### Laisvos formos kreivė

OBJ failo formatas leidžia vartotojo apibrėžtoms laisvos formos paviršiaus kreivėms nurodyti modelio paviršiaus geometriją. Kadangi laisvos formos kreivės yra sudėtingesnės nei daugiakampiai paviršiai, nes, turint keletą matematinių parametrų, lenktas linijas geriausiai galima apibrėžti laisvos formos kreivėmis. Todėl naudojant mažiau duomenų, palyginti su daugiakampiais teseliacijomis, laisvos formos kreivės naudojamos aukštos kokybės bet kokio 3D modelio kodavimui nedidinant failo dydžio.

### Laisvos formos paviršiai

OBJ failo formatas taip pat nurodo paviršiaus geometrijos plyteles su laisvos formos paviršiaus lopais. Tokio tipo laisvos formos paviršiaus lopai (NURBS) labai tinka paviršiams be standžių radialinių matmenų, pavyzdžiui, sunkvežimio kėbului, sraigtasparnio sparnams ar valties korpusui. Laisvos formos paviršių naudojimas yra labai naudingas, nes jie yra tikslesni, kad failų dydis būtų mažesnis ir didesnis tikslumas. Šie paviršiai yra svarbi aviacijos ir automobilių pramonės dalis, kur mažas tikslumas yra negailestingas.

Šie raktiniai žodžiai yra išdėstyti pagal duomenų tipą, siekiant apibrėžti paviršiaus geometriją.


|Elementai|Laisvos formos kreivės / paviršiaus korpuso teiginiai|Laisvos formos kreivės / paviršiaus atributai
---|---|---|
|p|Taškas|parm|Parametrų reikšmės|deg|Laipsnis
|l|Line|trim|Išorinė apkarpymo kilpa|bmat|Pagrindinė matrica
|f|Veidelis|skylė|Vidinė kirpimo kilpa|žingsnis|Žingsnio dydis
|kreivė|kreivė|scrv|speciali kreivė|cstype|kreivė arba paviršiaus tipas
|curv2|2D curve|sp|Specialus taškas|**Sujungimas ir paviršių grupavimas**
|surf|Paviršius|pabaiga|Pabaigos sakinys|sujungti
|**Rodyti / pateikti atributus**|g|Grupės pavadinimas
|nuožulnis|Kūgio interpoliacija|shadow_obj|Šešėlių užmetimas|s|Lyginimo grupė
|lod|Išsamumo lygis|trace_obj|Ray tracing|mg|Sujungiama grupė
|d_interp|Išspręskite interpoliaciją|ctech|Kreivės aproksimacijos metodas|o|Objekto pavadinimas
|c_interp|Spalvų interpoliacija|stech|Paviršiaus aproksimacijos technika|
|usemtl|Medžiagos pavadinimas|mtllib|Medžiagų biblioteka|
|**Geometrinės viršūnės**|
|v|Geometrinės viršūnės|vn|Viršūnių normaliosios|
|vt|Tekstūros viršūnės|vp|Parametrų erdvės viršūnės|

### Spalva ir tekstūra

OBJ failas leidžia išsaugoti informaciją apie spalvą ir tekstūrą susijusiu failo formatu, vadinamu Medžiagos šablonų biblioteka (MTL). Daugiaspalviai geometriniai modeliai atvaizduojami naudojant šiuos du failus kartu. MTL failai yra pagrįsti ASCII ir palengvina kompiuterinį atvaizdavimą, aprašydami paviršiaus šviesą atspindinčias savybes naudojant Phong atspindžio modelį. Standartą priėmė daug programinės įrangos pardavėjų, kurie naudojasi jo pranašumais keičiantis medžiagomis. MTL formatas yra šiek tiek pasenęs, nes nepalaiko naujausių technologijų, tokių kaip veidrodiniai ir paralaksiniai žemėlapiai.

## Nuorodos

* [Wavefront .obj failas](https://en.wikipedia.org/wiki/Wavefront_.obj_file)


