{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TNEF",
  "description": "Opi TNEF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata TNEF-tiedostoja.",
  "linktitle": "TNEF",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-tne-fif"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on TNEF-tiedosto?

Transport Neutral Encapsulation Format (TNEF) on Microsoftin kehittämä sähköpostin liitetiedostojen kapseloimiseen Messaging Application Programming Interface (**MAPI**) -pohjaiseen viestintäsovellusliittymään. Microsoft Outlook ja Microsoft Exchange Server tukevat täysin TNEF:ää, mutta myöhemmin purkaa TNEF:n MAPI:ksi ja näyttää muotoillut sähköpostit. TNEF-koodatulla sähköpostiliitteellä on MIME-tyyppinen MS-TNEF ja se tallennetaan nimellä winmail/win.dat. Winmail .dat -tiedoston liite sisältää seuraavat tiedot:


|Viesti|OLE-objektit|Outlook-ominaisuudet
---|---|---|
|<ul><li> Alkuperäisen viestin liitteet</li><li> Alkuperäinen muotoiltu versio</li><li> fontit, tekstin koot ja tekstin värit</li></ul> |<ul><li> upotettuja kuvia</li><li> upotetut Office-asiakirjat</li></ul> |<ul><li> mukautettuja lomakkeita</li><li> äänestyspainikkeita</li><li> kokouspyynnöt</li></ul>


Muut sähköpostipalvelut, jotka eivät tue TNEF:ää, esittävät pelkkää tekstiä TNEF-muotoisille viesteille. Outlook upottaa monimuotoisen viestin TNEF-tiedostoihin (OLE) tai tiettyihin Outlookin ominaisuuksiin (lomakkeet, kyselypainikkeet ja neuvottelupyynnöt). Eksplisiittisen TNEF-koodauksen sanktio Outlook-sähköpostiohjelmassa ei ole mahdollista, mutta RTF-muodon valitseminen sähköpostin lähettämiseen helpottaa epäsuorasti TNEF-koodausta.

## TNEF-tiedostomuoto

TNEF-datalgoritmi muodostaa litteän rakenteen rikkaista hierarkkisista viestin ominaisuuksista. Näitä litistettyjä rakenteita käytetään sitten edustamaan sarjatietovirtaa, joka koostuu tietyistä ominaisuuksista.

Joissakin tilanteissa, joissa ominaisuudet esiintyvät ryhmissä tai niillä on useita arvoja, stream saattaa sisältää laskelmia ja täyttöjä tietyn datan tasauksen pakottamiseksi. Erityinen tilanne, jossa tämän algoritmin käyttö on edullista, on ei-tuettu viestintäympäristö. Tällaisissa ympäristöissä TNEF Writer koodaa runsaan viestin ominaisuuden sarjatietovirtaan. Lisäksi ne ominaisuudet, jotka eivät kuulu taustalla olevaan TNEF:ään, voidaan kapseloida lähetyksen aikana. Nämä kapseloidut ominaisuudet asetetaan sitten saataville dekoodaamalla TNEF:n kautta, jotta varmistetaan alkuperäisen viestin kaikkien ominaisuuksien saatavuus asiakassovellukselle.

TNEF:ssä kaikki numeeriset tietotyypit ovat pienimuotoisia ja niiden koko on suurempi kuin yksi tavu. Näiden numeeristen arvojen käsittely ei-pikku-endian-alustoilla edellyttää asianmukaisten muunnosten suorittamista oikeiden arvojen saamiseksi. Merkkijonoarvot esitetään Augmented Backus-Naur Form (ABNF) -muodossa [RFC5234]-määritysten mukaisesti. Kun merkkijono päättyy tyhjään merkkiin, se sisällytetään myös; esimerkiksi `työntekijä@näyte.com %x00`.

{{< figure src="../TNEF.png" alt="TNEF-tiedostomuoto" >}}

## TNEF-attribuutit ja käsittelysäännöt ##

TNEF:n tietovirta alkaa vanhalla versionumerolla, allekirjoituksella, primitiivisen avaimen arvolla ja attribuutilla, joka edustaa koodisivua. Tämä koodisivu luodaan, kun kooderi tallentaa ANSI-attribuutteja ja ominaisuuksia. Sen jälkeen virrasta tuli sarja attribuutteja, joissa viestin attribuutit rivitettiin ensin ja sitten liiteattribuutit. Erilaiset viesti- ja liiteominaisuudet sisältyvät erityisiin määritteisiin, kuten attMsgProps, attAttachment ja attRecipTable. Attribuutit, jotka näkyvät TNEF-virrassa, sisältävät rakenteen, viestin ominaisuudet ja muunnokset, jotka ovat tarpeen niiden sitomiseksi viestin ominaisuuksiin. Jokainen attribuutti koostuu tunnuksesta, attribuutin koosta ja tiedoista, tarkistussummasta ja tasosta sen sovelluksen mukaan.

## Suhde protokolliin ja muihin algoritmeihin ##

Järjestelmät, joilla on huono mekanismi runsaan viestimuodon näyttämiseen natiivisti, tarvitsevat TNEF-tietoalgoritmin siirtoa varten. Mediatyyppiä ms-TNEF käytettäessä algoritmin tulos koostuu liitetiedostosta (winmail.dat) ja [RFC2045]:ssä määritetystä MIME:n runko-osasta. Pelkkä tekstiviestin runko lähetetään käyttämällä UUENCODEa [MSDN-UAF]-määrityksen mukaisesti ja tämä viestirunko tai vastaava menetelmä dekoodataan vastaanottajapäässä. Lisäksi TNEF voi lähettää viestidataa käyttämällä erilaisia Internet-protokollia, kuten SMTP, POP3, IMAP4 ja RFC2045-standardin mukaisia MIME-integroituja protokollia.

## Soveltuvuuslausunto ##

Yksinkertaisen viestinvälityksen lisäksi alkuperäinen TNEF-sovellus oli tarkoitus luoda käyttämään viestiluokkia ja tukemaan lisäominaisuuksia, joilla ei ole alkuperäistä tukea siirtoprotokollassa. Tätä sovellusta jalostettiin edelleen monipuolisten viestiominaisuuksien ja nimettyjen ominaisuuksien lähettämiseen, joita nykyaikaiset viestintäasiakkaat käyttävät nykyään. Alkuperäisen toteutuksen noudattamiseksi alkuperäinen määritteen syntaksi säilyy ja erityinen attribuutti pitää uuden viestin ominaisuudet erikseen.

## Viitteet

* [Transport Neutral Encapsulation Format](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)

* [Sähköpostiosoitteet ja osoitekirjat Exchange Serverissä](https://learn.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)

* [[MS-OXTNEF]: Transport Neutral Encapsulation Format (TNEF) -dataalgoritmi](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)


