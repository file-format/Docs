{
  "date" : "2020-08-20",
  "keywords" :[ "fichier eot", "format de fichier eot", "qu'est-ce qu'un fichier eot", "fichier", "exemple eot", "extension de fichier eot","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - Format de fichier de police TrueType",
  "description":"En savoir plus sur le format de fichier EOT et les API pour créer et ouvrir des fichiers EOT.",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Qu'est-ce qu'un fichier EOT ?

Un fichier avec l'extension .eot est une police OpenType intégrée dans un document. Ceux-ci sont principalement utilisés dans les fichiers Web tels qu'une page Web. Il a été créé par Microsoft et est pris en charge par les produits Microsoft, y compris le fichier de présentation PowerPoint [.pps](/fr/presentation/pps). Le fichier n'est pas d'usage principal et est une sorte de document d'accompagnement avec le document principal ou la page Web. Semblable aux polices OTF, EOT prend en charge les contours Postscript et TrueType pour les glyphes. Les fichiers EOT sont plus petits car ils sont compressés à l'aide de la compression LZ. EOT utilise un outil Microsoft pour créer une police à partir de polices TTF/OTF existantes.

## Bref historique

La police EOT a été soumise au W3C en 2007 dans le cadre de CSS3, mais en raison de ses exigences d'installation permanente sur un système distant, elle a été rejetée. Il a été soumis à nouveau en mars 2008, mais le W3C a finalement choisi [Web Font Format](/fr/font/woff/) (WOFF) qui a alors été normalisé.

## Format de fichier EOT

Les détails du format de fichier EOT peuvent être trouvés sur [page de soumission W3](https://www.w3.org/Submission/EOT/#FileFormat) et élabore la structure utilisée par ce format de police. L'EOT se compose d'une seule structure EMBEDDEDFONT qui fournit suffisamment d'informations de base sur le nom de la police et les caractères pris en charge. Le conditionnement de ces informations permet aux agents utilisateurs d'éviter de décompresser, décompresser ou installer la police si elle est déjà présente sur la machine.

### Structure EMBEDDEDFONT
La structure EMBEDDEDFONT a subi trois révisions, avec ajout de données supplémentaires à la fin de la structure à chaque révision. La dernière révision de la structure EMBEDDEDFONT est illustrée ci-dessous.

|Type de données|Nom de l'entrée|Description|
---|---|---|
|unsigned long|EOTSize|Longueur totale de la structure en octets (y compris les données de chaîne et de police)|
|unsigned long|FontDataSize|Longueur de la police OpenType (FontData) en octets|
|unsigned long|Version|Numéro de version de ce format - 0x00020002|
|unsigned long|Drapeaux|Drapeaux de traitement|
|byte[10]|FontPANOSE|La valeur PANOSE pour cette police - Voir http://www.microsoft.com/typography/otspec/os2.htm#pan|
|byte|Charset|Sous Windows, ceci est dérivé de TEXTMETRIC.tmCharSet. Cette valeur spécifie le jeu de caractères de la police. DEFAULT_CHARSET (0x01) n'indique aucune préférence. - Voir http://msdn2.microsoft.com/en-us/library/ms534202.aspx|
|byte|Italic|Si le bit pour ITALIC est défini dans OS/2.fsSelection, la valeur sera 0x01 - Voir http://www.microsoft.com/typography/otspec/os2.htm#fss|
|unsigned long|Weight|La valeur de poids pour cette police - Voir http://www.microsoft.com/typography/otspec/os2.htm#wtc|
|unsigned short|fsType|Indicateurs de type qui fournissent des informations sur l'intégration des autorisations - Voir http://www.microsoft.com/typography/otspec/os2.htm#fst|
|unsigned short|MagicNumber|Numéro magique pour le fichier EOT - 0x504C. Utilisé pour vérifier la corruption des données.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (bits 0-31) - Voir http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (bits 32-63) - Voir http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (bits 64-95) - Voir http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (bits 96-127) - Voir http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|CodePageRange1|CodePageRange1 (bits 0-31) - Voir http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (bits 32-63) - Voir http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment - Voir http://www.microsoft.com/typography/otspec/head.htm|
|unsigned long|Réservé1|Réservé - doit être 0|
|unsigned long|Réservé2|Réservé - doit être 0|
|unsigned long|Réservé3|Réservé - doit être 0|
|unsigned long|Réservé4|Réservé - doit être 0|
|unsigned short|Padding1|Remplissage pour maintenir l'alignement long. La valeur de rembourrage doit toujours être définie sur 0x0000.|
|unsigned short|FamilyNameSize|Nombre d'octets utilisés par le tableau FamilyName|
|byte|FamilyName[FamilyNameSize]|Tableau de caractères UTF-16 d'une longueur de FamilyNameSize octets. Il s'agit de la chaîne de la famille de polices en anglais trouvée dans le tableau des noms de la police (nom ID = 1) - Voir http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding2|La valeur de remplissage doit toujours être définie sur 0x0000.|
|unsigned short|StyleNameSize|Nombre d'octets utilisés par StyleName|
|byte|StyleName[StyleNameSize]|Tableau de caractères UTF-16 d'une longueur de StyleNameSize octets. Il s'agit de la chaîne de la sous-famille de polices en anglais trouvée dans le tableau des noms de la police (nom ID = 2) - Voir http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding3|La valeur de remplissage doit toujours être définie sur 0x0000.|
|unsigned short|VersionNameSize|Nombre d'octets utilisés par VersionName|
|bytes|VersionName[VersionNameSize]|Tableau de caractères UTF-16 d'une longueur de VersionNameSize octets. Il s'agit de la chaîne de version en anglais trouvée dans le tableau des noms de la police (nom ID = 5) - Voir http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding4|La valeur de remplissage doit toujours être définie sur 0x0000.|
|unsigned short|FullNameSize|Nombre d'octets utilisés par le FullName|
|byte|FullName[FullNameSize]|Tableau de caractères UTF-16 d'une longueur de FullNameSize octets. Il s'agit de la chaîne de nom complet en anglais trouvée dans le tableau des noms de la police (nom ID = 4) - Voir http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding5|La valeur de remplissage doit toujours être définie sur 0x0000.|
|unsigned short|RootStringSize|Nombre d'octets utilisés par le tableau RootString|
|byte|RootString[RootStringSize]|Tableau de caractères UTF-16 d'une longueur de RootStringSize octets.|
|unsigned long|RootStringCheckSum|Valeur de la somme de contrôle de la chaîne racine. Voir l'algorithme pour traiter RootStringChecksum ci-dessous.|
|unsigned long|EUDCCodePage|Valeur de page de code nécessaire pour la prise en charge des polices EUDC.|
|unsigned short|Padding6|La valeur de remplissage doit toujours être définie sur 0x0000.|
|unsigned short|SignatureSize|Nombre d'octets utilisés par le tableau Signature. Actuellement réservé et doit être défini sur 0x0000.|
|byte|Signature[SignatureSize]|Actuellement réservé. Si SignatureSize est 0x0000, il n'y a pas de longueur pour ce tableau.|
|unsigned long|EUDCFlags|Drapeaux de traitement pour la police EUDC. Les valeurs typiques peuvent être TTEMBED_XORENCRYPTDATA et TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|Nombre d'octets utilisés par le tableau Signature.|
|byte|EUDCFontData[EUDCFontSize]|Nombre d'octets utilisés pour les données de police EUDC. Si EUDCFontSize est 0x00000000, ce tableau n'a pas de longueur.|
|byte|FontData[FontDataSize]|Les données de police pour ce fichier EOT. Les données peuvent être compressées ou cryptées XOR comme indiqué par les indicateurs de traitement.|

## Références

* [Format de fichier EOT](https://www.w3.org/Submission/EOT/)
* [OpenType intégré](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [Incorporation de polices](https://en.wikipedia.org/wiki/Font_embedding)

