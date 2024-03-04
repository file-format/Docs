{
   "date":"2023-07-06",
   "keywords":[
"KATĖ",
"CAT failas",
"CAT langai",
"failą",
"cat failo plėtinys",
"pratęsimas",
"failą"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"CAT failo formatas – „Windows“ katalogo failas",
   "description":"Sužinokite apie CAT formatą ir API, kurios gali kurti ir atidaryti CAT failus.",
   "linktitle":"CAT",
   "menu":{
      "docs":{
         "identifier":"system-cat-lt",
         "parent":"system"
}
},
   "lastmod":"2023-07-06"
}

## Kas yra CAT failas?

Windows katalogo failas, taip pat žinomas kaip .cat failas, Windows operacinėje sistemoje atlieka lemiamą vaidmenį užtikrindamas įvairių failų vientisumą ir autentiškumą. Iš esmės jis naudojamas kaip skaitmeniniu parašu pasirašytas failas, kuriame yra kriptografinės maišos reikšmės failams, kuriuos jis kataloguoja, taip pat patikimos institucijos skaitmeninis parašas.

Pagrindinis .cat failo tikslas yra leisti patikrinti sistemos failus, tvarkykles arba programinės įrangos komponentus diegiant arba kai sistema veikia. Kai įdiegiate tvarkyklę arba programinės įrangos paketą, Windows patikrina atitinkamo .cat failo skaitmeninį parašą, siekdama įsitikinti, kad failai, į kuriuos ji nurodo, nebuvo sugadinti arba modifikuoti nuo tada, kai buvo pasirašyti. Naudodama .cat failus, Windows gali patikrinti failų autentiškumą ir aptikti bet kokius neteisėtus pakeitimus. Ši saugos priemonė padeda užkirsti kelią galimai kenkėjiškų ar pažeistų failų diegimui arba vykdymui Windows sistemoje.

## CAT sistemoje Windows

**CAT komanda sistemoje Windows** naudojama teksto failo turiniui rodyti tiesiai komandų eilutės lange. Tačiau vietinėje Windows komandų eilutėje nėra integruotos katės komandos, kaip Unix sistemose.

Norėdami pasiekti panašias funkcijas sistemoje Windows, galite naudoti komandą tipas. Štai pavyzdys, kaip naudoti komandą type Windows CMD:

```
C:\>type filename.txt
```

Pakeiskite failo pavadinimas.txt tikruoju tekstinio failo, kurį norite rodyti, keliu ir pavadinimu. Komanda išves failo turinį tiesiai komandų eilutės lange.

Arba, jei naudojate PowerShell, joje yra komandos Get-Content slapyvardis katė. Štai vienas pavyzdys:

```
PS C:\>cat filename.txt
```

Vėlgi, pakeiskite filename.txt teksto failo, kurį norite rodyti, keliu ir pavadinimu.

Atminkite, kad jei dirbate su dvejetainiais failais arba netekstiniu turiniu, komandų tipas arba katė naudojimas gali nesuteikti prasmingų rezultatų, nes jie pirmiausia skirti tekstiniams failams rodyti.

## Kas yra „Unix“ komandos katės „Windows“ atitikmuo?

Windows komanda tipas yra lygiavertė komandai cat Unix, kaip minėta aukščiau.

## „PowerShell“ naudojimas norint imituoti CAT komandą sistemoje „Windows“.

** Pagal numatytuosius nustatymus komanda cat nėra gimtoji Windows komandų eilutėje (CMD) arba PowerShell. Tačiau panašias funkcijas galite pasiekti naudodami PowerShell cmdlet Get-Content.** Štai pavyzdys:

```
Get-Content C:\Path\To\File.txt
``` 

Ši komanda parodys nurodyto failo turinį (šiame pavyzdyje Failas.txt). Jei norite sujungti ir rodyti kelių failų turinį, galite nurodyti kelis failų kelius:

```
Get-Content C:\Path\To\File1.txt, C:\Path\To\File2.txt
```

Jei vis tiek jums labiau patinka Unix tipo patirtis su komanda cat sistemoje Windows, galite naudoti trečiųjų šalių įrankius, pvz., **Cygwin arba Git Bash**, kurie suteikia Unix tipo aplinką sistemoje Windows ir apima cat. ` komanda.

**Additionally, starting with Windows 10 version 1903 (May 2019 Update), you can enable the Windows Subsystem for Linux (WSL) and use Linux commands, including `cat`.** To do this, follow these steps:

1.  Atidarykite PowerShell kaip administratorių ir paleiskite šią komandą, kad įjungtumėte WSL:
    
`dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
    
2.  Įgalinkite virtualios mašinos platformos funkciją:
    
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
    
3.  Įdiekite Linux platinimą iš Microsoft Store (pvz., Ubuntu).
    
4.  Nustatykite savo Linux platinimą (sukurkite vartotojo abonementą ir slaptažodį).
    
5.  Atidarykite įdiegtą Linux paskirstymą (pvz., Ubuntu) ir paleiskite komandą cat, kaip tai darytumėte įprastoje Linux aplinkoje.

## Koks yra CAT failo formatas?

Dvejetainis


