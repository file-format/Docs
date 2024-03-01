{
   "date":"2023-11-01",
   "keywords":[
"pat",
"pat tiedosto",
"pat diskstation managerin asennustiedosto",
"kuinka avata pat-tiedosto",
"tiedosto",
"pat tiedostopääte",
"laajennus",
"tiedosto"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"PAT-tiedostomuoto - DiskStation Managerin asennustiedosto",
   "description":"Lisätietoja PAT DiskStation Manager -asennustiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata PAT-tiedostoja.",
   "linktitle":"PAT",
   "menu":{
      "docs":{
         "identifier":"system-pat-diskstation-fi",
         "parent":"system"
}
},
   "lastmod":"2023-11-01"
}

## Mikä on PAT-tiedosto?

PAT-tiedosto liitetään yleisesti **DiskStation Manageriin (DSM)**, joka on Synology Network-Attached Storage (NAS) -laitteiden käyttämä käyttöjärjestelmä. PAT-tiedosto on asennustiedosto, jota käytetään DSM:n päivittämiseen tai asentamiseen Synology NAS:iin.

## PAT-tiedoston käyttö

Here is how you typically use a PAT file to install or update DSM on Synology NAS:

1.  Lataa PAT-tiedosto: Voit hankkia PAT-tiedoston viralliselta Synology-sivustolta tai muista luotettavista lähteistä.
    
2.  Kirjaudu NAS:iin: Käytä Synology NAS:n verkkopohjaista käyttöliittymää kirjoittamalla sen IP-osoite verkkoselaimeen. Tarvitset järjestelmänvalvojan oikeudet suorittaaksesi tämän toiminnon.
    
3.  Siirry Package Centeriin: Siirry verkkokäyttöliittymässä kohtaan Pakettikeskus. Täällä voit hallita ja asentaa sovelluksia NAS-laitteeseen.
    
4.  Manual Installation: In Package Center, there should be an option for "Manual Installation" or "Install/Update" depending on version of DSM you are using. Choose this option.
    
5.  Selaa PAT-tiedostoa: Sinua pyydetään selaamaan paikallisia tiedostoja ja valitsemaan ladattu PAT-tiedosto.
    
6.  Install or Update: After selecting PAT file, follow on-screen instructions to either install DSM (if it is a fresh installation) or update DSM (if you are upgrading to newer version).
    
7.  Wait for Completion: The installation or update process can take some time and your NAS may reboot as part of process. Be patient and wait for it to finish.
    
8.  Post-Installation Configuration: After installation or update, you may need to configure your NAS settings as per your preferences.

## DiskStation Manager

DiskStation Manager, josta käytetään usein lyhennettä DSM, on Synologyn kehittämä käyttöjärjestelmä NAS-laitteilleen. Se toimii hallinta- ja ohjausliittymänä Synology NAS -palvelimille. DiskStation Manager tarjoaa käyttäjäystävällisen verkkopohjaisen käyttöliittymän, jonka avulla käyttäjät voivat määrittää ja hallita erilaisia NAS-ominaisuuksia, kuten tietojen tallennusta, tiedostojen jakamista, varmuuskopiointiratkaisuja, multimediapalveluita ja paljon muuta.

DSM tunnetaan monipuolisuudestaan ja laajasta pakettiekosysteemistään, jonka avulla käyttäjät voivat asentaa ja käyttää erilaisia sovelluksia ja palveluita Synology NAS -järjestelmäänsä tehden siitä monikäyttöisen palvelimen sekä koti- että yrityskäyttöön. Joitakin DiskStation Managerin yleisiä toimintoja ovat tiedostojen jakaminen, tietojen varmuuskopiointi ja synkronointi, median suoratoisto, suojausominaisuudet ja virtualisoinnin tuki.

Synology julkaisee säännöllisesti päivityksiä ja uusia DSM-versioita parantaakseen turvallisuutta, suorituskykyä ja ominaisuuksia. Käyttäjät voivat päivittää DSM:n manuaalisesti käyttämällä PAT-tiedostoja tai määrittää automaattiset päivitykset varmistaakseen, että heidän NAS-järjestelmänsä käyttää uusinta ja turvallisinta DiskStation Manager -versiota.

## Kuinka avata PAT-tiedosto

To manually update DiskStation Manager, you can use a PAT file that you have downloaded from Synology Download Center using the following steps:

1. Siirry DiskStation Managerin ohjauspaneeliin.
2. Siirry Päivitä ja palauta -osioon ja valitse DSM-päivitys.
3. Valitse sieltä Manuaalinen DSM-päivitys.
4. Napsauta Selaa -painiketta ja etsi ja valitse sitten lataamasi PAT-tiedosto.
5. Aloita DiskStation Managerin päivitys napsauttamalla Käytä-painiketta.

## Viitteet
* [Synology](https://en.wikipedia.org/wiki/Synology)
