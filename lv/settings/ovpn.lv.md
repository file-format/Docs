{
  "date": "2023-03-21",
  "keywords": [
"ovpn fails",
"kas ir ovpn fails",
"kā atvērt ovpn failu",
"failu",
"ovpn faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "OVPN faila formāts — OpenVPN konfigurācijas fails",
  "description": "Uzziniet par OVPN formātu un API, kas var izveidot un atvērt OVPN failus.",
  "linktitle": "OVPN",
  "menu": {
    "docs": {
      "identifier": "settings-ovpn-lv",
      "parent": "settings"
}
},
  "lastmod": "2023-03-21"
}

## Kas ir OVPN fails?

Ovpn fails ir konfigurācijas fails, ko izmanto OpenVPN, populāra atvērtā pirmkoda VPN (virtuālā privātā tīkla) programmatūra. Tajā ir iestatījumi un norādījumi, kas nepieciešami, lai OpenVPN klients izveidotu savienojumu ar VPN serveri.

Atkarībā no VPN pakalpojumu sniedzēja ovpn faila saturs var mainīties, taču parasti tajā ir šāda informācija:

- VPN servera IP adrese vai resursdatora nosaukums
- Porta numurs, kas jāizmanto VPN savienojumam
- Izmantojamais protokols (TCP vai UDP)
- Izmantojamie šifrēšanas un autentifikācijas algoritmi
- lietotāja sertifikāta un privātās atslēgas failu atrašanās vieta
- Jebkuri papildu iestatījumi vai norādījumi, kas attiecas uz VPN pakalpojumu sniedzēju.

Lai izmantotu ovpn failu, lietotāja ierīcē ir jābūt instalētai OpenVPN klienta programmatūrai un pēc tam jāimportē ovpn fails klienta programmatūrā. Kad fails ir importēts, lietotājs var izveidot savienojumu ar VPN serveri, vienkārši noklikšķinot uz pogas klienta programmatūrā.

## OVPN faila konfigurēšana

Lai konfigurētu OpenVPN, izmantojot ovpn failu, rīkojieties šādi:

1. Instalējiet savā ierīcē OpenVPN klienta programmatūru.
2. Atveriet OpenVPN klienta programmatūru un noklikšķiniet uz pogas Importēt, lai importētu ovpn failu.
3. Pārlūkojiet direktoriju, kurā saglabājāt ovpn failu, un atlasiet to.
4. Klienta programmatūra importēs failu un interfeisa iekšpusē parādīs konfigurācijas iestatījumus.
5. Ja nepieciešams, ievadiet savus VPN pieteikšanās akreditācijas datus.
6. Kad ovpn fails ir importēts un pieteikšanās akreditācijas dati ir ievadīti, noklikšķiniet uz pogas Savienot, lai izveidotu savienojumu ar VPN serveri.
7. Pagaidiet, līdz tiek izveidots savienojums. Kad savienojums ir izveidots, varat izmantot internetu tā, it kā būtu izveidots savienojums ar VPN servera atrašanās vietu.

Ovpn failā ir visi nepieciešamie konfigurācijas iestatījumi, kas nepieciešami droša VPN savienojuma izveidei. Tāpēc ir svarīgi saglabāt ovpn failu drošībā, jo tajā ir ietverta sensitīva informācija, piemēram, VPN servera adrese, autentifikācijas informācija un šifrēšanas atslēgas.

## Kā atvērt OVPN failu?

Lai atvērtu ovpn failu, ierīcē būs jābūt instalētai OpenVPN klienta programmatūrai. Tālāk ir norādītas darbības, lai atvērtu ovpn failu:

1. Lejupielādējiet un instalējiet OpenVPN klienta programmatūru, piemēram, OpenVPN GUI, Tunnelblick vai OpenVPN Connect.
2. Saglabājiet ovpn failu savā datorā.
3. Atveriet OpenVPN klienta programmatūru un noklikšķiniet uz pogas Importēt, lai importētu ovpn failu.
4. Pārlūkojiet direktoriju, kurā saglabājāt ovpn failu, un atlasiet to.
5. Klienta programmatūra importēs failu un interfeisā parādīs konfigurācijas iestatījumus.
6. Ja nepieciešams, ievadiet savus VPN pieteikšanās akreditācijas datus.
7. Kad ovpn fails ir importēts un pieteikšanās akreditācijas dati ir ievadīti, noklikšķiniet uz pogas Savienot, lai izveidotu savienojumu ar VPN serveri.

Kad savienojums ir izveidots, varat pārlūkot internetu, izmantojot VPN servera atrašanās vietas IP adresi. Ņemiet vērā, ka precīzās darbības, lai atvērtu ovpn failu, var atšķirties atkarībā no izmantotās OpenVPN klienta programmatūras.

## Atsauces
* [OpenVPN](https://en.wikipedia.org/wiki/OpenVPN)


