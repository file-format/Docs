{
  "date": "2021-06-21",
  "keywords": [
"UDL",
"pratęsimas",
"udl failą",
"udl failo formatas",
"Duomenų bazės failo tipas",
"Duomenų bazės failo formatas",
"kas yra udl failas"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie UDL failo formatą ir API, kurios gali kurti ir atidaryti UDL failus.",
  "title": "UDL – „Microsoft“ universaliųjų duomenų nuorodos failas",
  "linktitle": "UDL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ud-ltl"
}
},
  "lastmod": "2021-06-21"
}

## Kas yra UDL failas?
Failas su plėtiniu .udl vadinamas Microsoft Universal Data Link failu; nurodant ryšio atributus; naudoja Windows programėlės ryšiui su duomenų baze užmegzti. UDL faile yra OLE DB duomenų šaltinio ryšio eilutė; su vartotojo vardu ir slaptažodžiu bei pagrindinėmis ryšio eilutės savybėmis. Kad ypatybės nebūtų tiesiogiai nurodytos ranka ryšio eilutėje, kaip alternatyvą galima naudoti dialogo langą Duomenų nuorodos ypatybės, kad būtų išsaugota ryšio informacija .udl faile.

## UDL failo formatas
Iš esmės UDL (Universal Data Link) failas yra paprastas tekstinis failas, kurį sudaro duomenų bazės ryšio eilutė su tam tikrais atributais arba savybėmis. Sukūrus UDL failą, jį galima išbandyti naudojant SQL Server Management Studio, kad būtų patikrintas ryšys.

### Ryšio eilutės savybės
Norint užtikrinti tinkamą ryšį, UDL galima nustatyti šias savybes:

- **Serverio pavadinimas**: serverio vieta, kurioje yra norima pasiekti duomenų bazė.
- **Autentifikavimo parinktys**
– **Windows autentifikavimas**: SQL serverio autentifikavimas naudojant šiuo metu prisijungusio vartotojo Windows paskyros kredencialus.
- **SQL serverio autentifikavimas**: autentifikavimas naudojant prisijungimo ID ir slaptažodį.
- **Active Directory – Integrated**: integruotas autentifikavimas naudojant Azure Active Directory tapatybę; taip pat gali būti naudojamas Windows autentifikavimui SQL serveryje.
– **Active Directory – Slaptažodis**: vartotojo ID ir slaptažodžio autentifikavimas naudojant Azure Active Directory tapatybę.
– **Active Directory – universalus su MFA palaikymu**: interaktyvus autentifikavimas naudojant Azure Active Directory tapatybę.
– **Active Directory – pagrindinis paslaugos adresas**: autentifikavimas naudojant Azure Active Directory paslaugos pagrindinį adresą.
- **Serverio SPN**: jei naudojate patikimą ryšį, galite nurodyti serverio pagrindinį paslaugos pavadinimą (SPN).
– **Vartotojo vardas**: įveskite vartotojo ID, kurį naudosite autentifikavimui, kai prisijungiate prie duomenų šaltinio.
- **Slaptažodis**: įveskite slaptažodį, kurį naudosite autentifikavimui, kai prisijungiate prie duomenų šaltinio.
- **Tuščias slaptažodis**: kai pažymėta, nurodytam teikėjui leidžiama naudoti tuščią slaptažodį ryšio eilutėje.
- **Leisti išsaugoti slaptažodį**: leidžia išsaugoti slaptažodį su ryšio eilute.
- **Naudokite tvirtą duomenų šifravimą**: duomenys, perduodami per ryšį, bus užšifruoti.
- **Trust server certificate**: The server's certificate will be validated.
- **Duomenų bazė**: duomenų bazės, kurią norite pasiekti, pavadinimas.
- **Pridėkite duomenų bazės failą kaip duomenų bazės pavadinimą**: nurodo prisegamos duomenų bazės pirminio failo pavadinimą.

## Nuorodos Nr.

* [Microsoft Data Access Components](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)

* [Universal Data Link (UDL) konfigūracija](https://learn.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)


