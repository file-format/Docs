{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PDF/VT failo formatas",
  "description": "Sužinokite apie PDF / VT failo formatą ir API, kurios gali kurti ir atidaryti PDF / VT failus.",
  "linktitle": "PDF/VT",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf-v-ltt"
}
},
  "lastmod": "2019-09-10"
}

# Kas yra PDF/VT? #

PDF/VT, 2010 m. rugpjūčio mėn. paskelbtas kaip [ISO 16612-2](https://www.iso.org/standard/46428.html) kaip standartas, sukurtas taip, kad įgalintų kintamų dokumentų spausdinimą (VDP) įvairiose aplinkose. Standartas sudaro kintamos informacijos ir operacijų spausdinimą kaip standarto pagrindą. Kintamųjų duomenų spausdinimas naudojamas, kai dalis informacijos kiekvienam turinio gavėjui skiriasi. Operacijų spausdinimas apima sąskaitas faktūras, ataskaitas ir kitus dokumentus, kuriuose atsiskaitymo informacija sujungiama su rinkodaros informacija. Dėl to patobulintas vaizdų, teksto ir kitų tipų turinio apdorojimas. Naudojant dokumento dalies metaduomenų (DPM) koncepciją, PDF/VT leidžia patikimai ir dinamiškai valdyti didelės apimties operacijų išvesties (HVTO) spausdinimo duomenų puslapius. PDF/VT failus galima atidaryti Adobe Acrobat Viewer nepridedant jokio kito komponento.

## Dokumento dalies hierarchija Nr.

Dokumento dalies (DPart) hierarchija yra tarsi dokumento dalių mazgų medžio struktūra, pagrįsta visais dokumento puslapiais. Šio medžio elementai vadinami DPart mazgais. Kiekviename vidiniame mazge yra kiti DPart mazgai ir kiekvienas lapo mazgas nurodo vieną ar daugiau puslapių gavėjui. Iš esmės DPart hierarchija nurodo PDF / VT failo dokumentų arba dokumentų dalių seką ir ryšį. DPart mazgų medžio struktūra lengvai atspindi vidinį PDF / VT dokumento turinį, nes joje gali būti antrinių dokumentų daugeliui gavėjų ir kiekviena dokumento dalis atitinka vieno gavėjo puslapius. DPart hierarchija reikalinga PDF / VT failuose.

## Dokumento dalies metaduomenys (DPM) Nr.

Dokumento dalies metaduomenys (DPM) yra susieti su kiekvienu dokumento dalies hierarchijos mazgu ir gali būti naudojami informacijai apie konkretaus gavėjo antrinį dokumentą ir jo dalis perduoti. Visų pirma, DPM gali turėti informacijos apie ypatybes arba informaciją apie gavėjus užkoduota forma.

## Atitikties lygiai ##

PDF/VT suteikiamas šiais trimis atitikties lygiais. Visi jie pagrįsti [PDF](/pdf/) 1.6.

* „PDF/VT-1“ – jis pagrįstas PDF/X-4 ir jame yra visi ištekliai, reikalingi PDF dokumentui pateikti.

* `PDF/VT-2` – skirti keistis keliais failais, PDF/VT-2 dokumentai gali nurodyti išorinius išvesties tikslus, išorinį turinį arba abu. PDF / VT dokumentas ir visi su juo susiję PDF failai ir išoriniai išvesties tikslai bendrai vadinami PDF / VT-2 failų rinkiniu. Acrobat 9 ir palaiko šią funkciją.

* „PDF/VT-2s“ – palaiko tiesioginę PDF/VT-2 transliaciją. Tai leidžia apdoroti segmentuotas duomenų dalis.


## Nuorodos Nr.

* [PDF/VT – Vikipedija](https://en.wikipedia.org/wiki/PDF/VT)

* [ISO 16612-2 Graphic Technology](https://www.iso.org/standard/46428.html)


