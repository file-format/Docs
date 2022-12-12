{
  "date" : "2021-07-29",
  "keywords" :[ "pes fájl", "pes fájlformátum", "mi az a pes fájl", "fájl", "pes példa", "pes fájlkiterjesztés", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PES fájlformátum - Brother PE hímzésformátum",
  "description":"További információ a PES fájlformátumról és az API-król, amelyek PES-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "PES",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## Mi az a PES Embroidery fájl?

A PES hímzőfájl egy tervfájl, amely utasításokat tartalmaz a hímző-/varrógépekhez. A Brother Industries fejlesztette ki a hímzőgépeihez, de később általános fájlformátummá formálták. A varrógépek a PES fájlokat használják a minták szöveten történő varrására vonatkozó utasítások olvasásához. Ezek a fájlok két célt szolgálnak; először tervezési információkat nyújt a Brother Industries által fejlesztett PE-Design alkalmazáshoz, másodszor pedig tervezési nevet, színeket és hímzőgép kódokat, például "stop", "jump" és "trim".

## PES fájlformátum - További információ

A PES-fájlt a rendszer bináris fájlformátumban menti a lemezre. Több olyan szakaszt tartalmaz, amelyek előre meghatározott módszerrel tárolják a varrási információkat. A PES fájlformátum a következő.

* Verzióadatok – Verzióinformációkat ad meg, és bármilyen érték lehet: "#PES0001", "#PES0020", "#PES0030", "#PES0040", "#PES0050", "#PES0055", "#PES0060"
* PEC keresési érték – 4 bájtos kisvégű egész szám közvetlenül a verzióadatok után, és a tervezési részleteket tartalmazó PEC szakasz keresési értékét jelenti.
* PSE szakasz – A Brother PE-Design-ra vonatkozó tervezési információkat tartalmaz, és más varrási alkalmazások is lehetnek
* PCE Section – Bárhol lehet a PSE fájlban, de a PEC Seek Value hivatkozik rá.

## A PES fájlt használó varrógép típusa

A PES fájlokat elsősorban a Brother varrógépekhez használt PE-Design szoftver hozza létre. Néhány más gép, amely támogathatja a PES fájlokat, többek között a Babylock és a Bernina otthoni hímzőgépek.

## Hogyan lehet PSE fájlokat konvertálni?

A PE-Design szoftveralkalmazás [konvertálja a PSE-fájlt](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl =pes+file) más formátumokra, például .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd vagy .xxx. Ezt a PE-Design alkalmazással lehet megtenni a fájl megnyitásával és a konvertálási formátum kiválasztásával.

## Hivatkozások

* [PE tervezés – használati útmutató](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)

