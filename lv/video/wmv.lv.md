{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WMV faila formāts",
  "description": "Uzziniet par WMV failu formātu un API, kas var izveidot un atvērt WMV failus.",
  "linktitle": "WMV",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-wm-lvv"
}
},
  "lastmod": "2019-09-16"
}

## Kas ir WMV fails?

Uzlaboto sistēmu formāts (ASF) ir digitāls multivides konteiners, kas galvenokārt paredzēts multivides straumju glabāšanai un pārsūtīšanai. Microsoft Windows Media Video (WMV) ir saspiests video formāts, un Microsoft Windows Media Audio (WMA) ir saspiests audio formāts kopā ar papildu metadatiem ASF konteinerā, ko izstrādājusi Microsoft. Kad WMV vai WMA faili ir kodēti ar Windows Media Video un Windows Media Audio kodekiem, tie tiek attēloti ar paplašinājumu .asf. WMV saspiež lielus failus, lai nodrošinātu labāku pārraides ātrumu tīklā, vienlaikus saglabājot video kvalitāti. WMV ir īpaši izstrādāts darbam visās Windows ierīcēs. Pēc Kinofilmu un televīzijas inženieru biedrības (SMPTE) standartizācijas WMV tagad tiek uzskatīts par atvērta standarta formātu.

## Vēsture ##

With the help of Microsoft proprietary codecs new compressed video format was developed in 1999 known as WMV7 which was based on MPEG-4 Part 2. Uzlabojumi tika pievienoti vēl divās versijās, ti, WMV8 un 9. Microsoft 2003. gadā SMPTE standartizācijai iesniedza 9^^th^^ WMV versiju, kas galu galā tika standartizēta 2006. gadā kā SMPTE 421M, kas pazīstama arī kā VC-1. WMV ideja bija izstrādāt multivides formātu, ko varētu atbalstīt visa Microsoft atbalstītā aparatūra un programmatūra. Turklāt vēl viens svarīgs mērķis bija pārraidīt video straumes internetā optimālā scenārijā. Pēc SMPTE standartizācijas WMV kļuva arī par Blu-ray disku video formātu.

## Faila formāta specifikācijas

### Konteiners

Parasti WMV tiek iesaiņots ASF konteinerā, bet turklāt Matroska vai AVI konteiners to var arī atbalstīt ar attiecīgi .mkv un .avi paplašinājumiem.

### Windows Media Video 9

Lai gan Windows Media Video 9 sērijā ir pieejami dažādi audio un video kodeki digitālo mediju autorēšanai un atskaņošanai, WMV-9 kodeks ir jaunākais un labākais video kodeks, jo tas var sasniegt optimālu saspiešanu ar ļoti zemu bitu pārraides ātrumu, ti, 160x. 120 ar 10 Kb/s līdz 1920 x 1080 ar ātrumu 4–8 Mb/s dažādiem HD video.

### Kodeka struktūra

WMV-9 ir 8 bitu 4:2:0 iekšējais krāsu formāts. Tāpat kā visi citi populārie video saspiešanas standarti MPEG-1 un H.261, WMV-9 izmanto uz blokiem balstītu kustības kompensācijas un telpiskās pārveidošanas shēmu. Kopumā mēs varam teikt, ka šie standarti veic kustības kompensāciju pa blokiem no iepriekšējā rekonstruētā kadra, izmantojot 2-D lielumu, ko sauc par kustības vektoru (MV), lai signalizētu par telpisko nobīdi. Pašreizējais bloks tiek veidots, prognozējot vērtības no tāda paša izmēra iepriekšējā rekonstruētā kadra, kuru kustības vektors nobīda no pašreizējās pozīcijas. Galu galā atlikušo kļūdu aprēķina kā starpību starp paredzēto bloku ar kustību kompensāciju un faktisko bloku. Šo atlikušo kļūdu pārveido, izmantojot lineāru enerģiju sablīvējošu transformāciju, pēc tam kvantizē un kodē entropiju.

Quantized transform coefficients are entropy decoded, de-quantized, and inverse transformed to produce an approximation of the residual error on the decoder side, which is then added to the motion-compensated prediction to generate the reconstruction. The high-level description of the codec is shown in the following image.

Pārējā sadaļā tiks apspriesti jaunie WMV-9 uzlabojumi, kas to atšķir no pārējiem video kodēšanas risinājumiem, piemēram, MPEG standartiem. WMV-9 ir iekšējie (I), prognozētie (P) un divvirzienu prognozētie (B) kadri. Iekšējie kadri ir tie, kas tiek kodēti neatkarīgi un nav atkarīgi no citiem kadriem. Paredzamie kadri ir kadri, kas ir atkarīgi no viena kadra pagātnē. Paredzētā kadra dekodēšana var notikt tikai pēc tam, kad ir atkodēti visi atsauces kadri pirms pašreizējā kadra, sākot no jaunākā (I) kadra. B kadri ir kadri, kuriem ir divas atsauces — viena laika pagātnē un viena laika nākotnē. B kadri tiek pārsūtīti pēc to atsaucēm, kas nozīmē, ka B kadri tiek sūtīti nepareizi, lai nodrošinātu, ka to atsauces ir pieejamas dekodēšanas laikā. B kadri WMV-9 netiek izmantoti kā atsauce nākamajiem kadriem. Tādējādi B kadri tiek novietoti ārpus dekodēšanas cilpas, ļaujot B kadru dekodēšanas laikā izmantot īsceļus bez novirzes vai ilgtermiņa vizuāliem artefaktiem. Iepriekš minētā I, P un B kadru definīcija attiecas gan uz progresīvām, gan rindpārlēces secībām.

Video kodeku veiktspēja tiek salīdzināta ar to ātruma izkropļojumu (RD) diagrammu. Tā ir 2-D līkne, kas parāda saspiešanas radītos traucējumus noteiktā bitu pārraides ātrumā.

WMV-9 ir atrisinājis šo problēmu, ieviešot dažādas tālāk uzskaitītās metodes:

1. Adaptīvā bloka izmēra transformācija

2. Ierobežotas precizitātes transformācijas komplekts

3. Kustības kompensācija

4. Kvantēšana un dekvantēšana

5. Uzlabota entropijas kodēšana

6. Cilpas filtrēšana

7. Uzlabota B rāmja kodēšana

8. Interlace kodēšana

9. Pārklāšanās izlīdzināšana

10. Zemas cenas instrumenti

11. Izbalēšanas kompensācija

## Atsauces

* [https://bytescout.com/blog/2018/02/windows-media-video-format.html](https://bytescout.com/blog/2018/02/windows-media-video-format.html )

* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)


