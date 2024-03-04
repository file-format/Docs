{
   "date":"2023-11-01",
   "keywords":[
"paglostyti",
"pat failą",
"pat diskstation manager diegimo failas",
"kaip atidaryti pat failą",
"failą",
"pat failo plėtinys",
"pratęsimas",
"failą"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"PAT failo formatas – „DiskStation Manager“ diegimo failas",
   "description":"Sužinokite apie PAT DiskStation Manager diegimo failo formatą ir API, kurios gali kurti ir atidaryti PAT failus.",
   "linktitle":"PAT",
   "menu":{
      "docs":{
         "identifier":"system-pat-diskstation-lt",
         "parent":"system"
}
},
   "lastmod":"2023-11-01"
}

## Kas yra PAT failas?

PAT failas dažniausiai siejamas su **DiskStation Manager (DSM)**, operacine sistema, naudojama Synology Network-Attached Storage (NAS) įrenginiuose. PAT failas yra diegimo failas, naudojamas DSM atnaujinti arba įdiegti Synology NAS.

## PAT failo naudojimas

Here is how you typically use a PAT file to install or update DSM on Synology NAS:

1.  Atsisiųsti PAT failą: PAT failą galite gauti iš oficialios Synology svetainės arba kitų patikimų šaltinių.
    
2.  Prisijunkite prie savo NAS: pasiekite savo Synology NAS žiniatinklio vartotojo sąsają įvesdami jos IP adresą žiniatinklio naršyklėje. Norėdami atlikti šią operaciją, jums reikės administratoriaus teisių.
    
3.  Eikite į paketų centrą: žiniatinklio sąsajoje eikite į Paketų centras. Čia galite valdyti ir įdiegti programas savo NAS.
    
4.  Manual Installation: In Package Center, there should be an option for "Manual Installation" or "Install/Update" depending on version of DSM you are using. Choose this option.
    
5.  Naršykite PAT failą: būsite paraginti naršyti vietinius failus ir pasirinkti atsisiųstą PAT failą.
    
6.  Install or Update: After selecting PAT file, follow on-screen instructions to either install DSM (if it is a fresh installation) or update DSM (if you are upgrading to newer version).
    
7.  Wait for Completion: The installation or update process can take some time and your NAS may reboot as part of process. Be patient and wait for it to finish.
    
8.  Post-Installation Configuration: After installation or update, you may need to configure your NAS settings as per your preferences.

## DiskStation Manager

DiskStation Manager, dažnai sutrumpintai vadinama DSM, yra Synology sukurta operacinė sistema savo tinklo prijungtoms saugykloms (NAS). Ji tarnauja kaip Synology NAS serverių valdymo ir valdymo sąsaja. DiskStation Manager teikia patogią žiniatinklio sąsają, leidžiančią vartotojams konfigūruoti ir valdyti įvairius savo NAS aspektus, tokius kaip duomenų saugojimas, failų bendrinimas, atsarginių kopijų kūrimo sprendimai, daugialypės terpės paslaugos ir kt.

DSM yra žinomas dėl savo universalumo ir plačios paketų ekosistemos, leidžiančios vartotojams įdiegti ir paleisti įvairias programas ir paslaugas savo Synology NAS, paversdamos jį daugiafunkciu serveriu, skirtu naudoti tiek namuose, tiek versle. Kai kurios bendros DiskStation Manager funkcijos apima failų bendrinimą, duomenų atsarginę kopiją ir sinchronizavimą, medijos srautinį perdavimą, saugos funkcijas ir virtualizacijos palaikymą.

Synology reguliariai išleidžia naujinimus ir naujas DSM versijas, kad pagerintų saugumą, našumą ir funkcijas. Vartotojai gali rankiniu būdu atnaujinti DSM naudodami PAT failus arba sukonfigūruoti automatinius naujinimus, kad užtikrintų, jog jų NAS veikia naujausia ir saugiausia DiskStation Manager versija.

## Kaip atidaryti PAT failą

To manually update DiskStation Manager, you can use a PAT file that you have downloaded from Synology Download Center using the following steps:

1. Pasiekite DiskStation Manager valdymo skydelį.
2. Eikite į skyrių Atnaujinti ir atkurti ir pasirinkite DSM naujinimas.
3. Iš ten pasirinkite Rankinis DSM naujinimas.
4. Spustelėkite mygtuką Naršyti, tada suraskite ir pasirinkite atsisiųstą PAT failą.
5. Norėdami pradėti DiskStation Manager atnaujinimą, spustelėkite mygtuką Taikyti.

## Nuorodos
* [Synology](https://en.wikipedia.org/wiki/Synology)
