{
  "date": "2023-03-21",
  "keywords": [
"ovpn failą",
"kas yra ovpn failas",
"Kaip atidaryti ovpn failą",
"failą",
"ovpn failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "OVPN failo formatas – OpenVPN konfigūracijos failas",
  "description": "Sužinokite apie OVPN formatą ir API, kurios gali kurti ir atidaryti OVPN failus.",
  "linktitle": "OVPN",
  "menu": {
    "docs": {
      "identifier": "settings-ovpn-lt",
      "parent": "settings"
}
},
  "lastmod": "2023-03-21"
}

## Kas yra OVPN failas?

Ovpn failas yra konfigūracijos failas, naudojamas OpenVPN, populiarios atvirojo kodo VPN (virtualaus privataus tinklo) programinės įrangos. Jame yra nustatymai ir instrukcijos, reikalingos OpenVPN klientui prisijungti prie VPN serverio.

Priklausomai nuo VPN paslaugų teikėjo, ovpn failo turinys gali keistis, tačiau paprastai jame yra ši informacija:

– VPN serverio IP adresas arba pagrindinio kompiuterio pavadinimas
- Prievado numeris, naudojamas VPN ryšiui
- Naudojamas protokolas (TCP arba UDP)
- Naudoti šifravimo ir autentifikavimo algoritmai
- Vartotojo sertifikato ir privataus rakto failų vieta
– Bet kokie papildomi nustatymai ar nurodymai, būdingi VPN paslaugų teikėjui.

Norint naudoti ovpn failą, vartotojas turi turėti savo įrenginyje įdiegtą OpenVPN kliento programinę įrangą ir importuoti ovpn failą į kliento programinę įrangą. Kai failas bus importuotas, vartotojas gali prisijungti prie VPN serverio tiesiog spustelėdamas mygtuką kliento programinėje įrangoje.

## Konfigūruojamas OVPN failas

Norėdami sukonfigūruoti OpenVPN naudodami ovpn failą, atlikite šiuos veiksmus:

1. Įdiekite OpenVPN kliento programinę įrangą savo įrenginyje.
2. Atidarykite OpenVPN kliento programinę įrangą ir spustelėkite mygtuką Importuoti, kad importuotumėte ovpn failą.
3. Eikite į katalogą, kuriame išsaugojote ovpn failą, ir pasirinkite jį.
4. Kliento programinė įranga importuos failą ir sąsajoje parodys konfigūracijos nustatymus.
5. Jei reikia, įveskite savo VPN prisijungimo kredencialus.
6. Kai ovpn failas bus importuotas ir įvesti prisijungimo kredencialai, spustelėkite mygtuką Prisijungti, kad užmegztumėte ryšį su VPN serveriu.
7. Palaukite, kol bus sukurtas ryšys. Užmezgę ryšį, galėsite naudotis internetu taip, lyg būtumėte prisijungę prie VPN serverio vietos.

ovpn faile yra visi būtini konfigūracijos nustatymai, reikalingi saugiam VPN ryšiui užmegzti. Todėl svarbu, kad ovpn failas būtų saugus, nes jame yra slaptos informacijos, pvz., VPN serverio adresas, autentifikavimo informacija ir šifravimo raktai.

## Kaip atidaryti OVPN failą?

Norėdami atidaryti ovpn failą, įrenginyje turėsite įdiegti OpenVPN kliento programinę įrangą. Štai ovpn failo atidarymo veiksmai:

1. Atsisiųskite ir įdiekite OpenVPN kliento programinę įrangą, pvz., OpenVPN GUI, Tunnelblick arba OpenVPN Connect.
2. Išsaugokite ovpn failą savo kompiuteryje.
3. Atidarykite OpenVPN kliento programinę įrangą ir spustelėkite mygtuką Importuoti, kad importuotumėte ovpn failą.
4. Eikite į katalogą, kuriame išsaugojote ovpn failą, ir pasirinkite jį.
5. Kliento programinė įranga importuos failą ir sąsajoje parodys konfigūracijos nustatymus.
6. Jei reikia, įveskite savo VPN prisijungimo kredencialus.
7. Kai ovpn failas bus importuotas ir įvesti prisijungimo kredencialai, spustelėkite mygtuką Prisijungti, kad užmegztumėte ryšį su VPN serveriu.

Užmezgę ryšį, galėsite naršyti internete naudodami VPN serverio vietos IP adresą. Atminkite, kad tikslūs ovpn failo atidarymo veiksmai gali skirtis priklausomai nuo jūsų naudojamos OpenVPN kliento programinės įrangos.

## Nuorodos
* [OpenVPN](https://en.wikipedia.org/wiki/OpenVPN)


