{
  "date": "2021-08-10",
  "keywords": [
".ova fails",
"faila formātā",
"kas ir .ova fails",
"failu",
"faila paplašinājums"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet, kas ir .ova faila formāts un API, kas var izveidot un atvērt ova failus.",
  "title": "OVA faila formāts — atveriet virtuālās ierīces failu",
  "linktitle": "OVA",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-ov-lva"
}
},
  "lastmod": "2022-01-03"
}

## Kas ir OVA fails?

OVA (Open Virtual Appliance) fails ir OVF direktorijs, kas saglabāts kā arhīvs, izmantojot .tar arhivēšanas formātu. Tas ir virtuālās ierīces pakotnes fails, kurā ir faili programmatūras izplatīšanai, kas darbojas virtuālajā mašīnā. OVA pakotnē ir ietverts [.ovf](/disc-and-media/ovf/) deskriptora fails, sertifikātu faili, neobligāts [.mf](/programming/mf/) fails, kā arī citi saistītie faili. OVA failiem ir multivides veids kā lietojumprogramma/ovf.

## OVA faila formāts

Kā minēts, OVA fails ir arhīva fails, kas tiek izveidots, izmantojot OVF direktoriju TAR faila formātā. Pats fails tiek saglabāts kā binārs fails. Lielākā daļa virtualizācijas platformu, piemēram, VMware, Microsoft, Oracle un Citrix, var instalēt virtuālās ierīces no OVF faila, kas ir deskriptora fails ar detalizētu informāciju par attēlu, kas jāielādē virtuālajā mašīnā.

## OVA faila priekšrocības

* OVA faili ir saspiesti, kas ļauj ātrāk lejupielādēt.

* vSphere Client pārbauda OVA failu pirms tā importēšanas un nodrošina tā saderību ar paredzēto mērķa serveri. Ja ierīce nav saderīga ar atlasīto resursdatoru, to nevar importēt un tiek parādīts kļūdas ziņojums.

* OVA var iekapsulēt daudzpakāpju lietojumprogrammas un vairāk nekā vienu virtuālo mašīnu.


## Atsauces

* [OVA File Formats and Templates](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-AE61948B-C2EE-436E-BAFB-3C7209088552.html)
* [OVF File Format Specifications](https://products.conholdate.app/viewer/view/3XKCLQbwAw/open-virtualization-format-specification-dsp0243_1-1-0.pdf)

